<template>
    <div id="mint"
         className="min-h-screen h-full w-full overflow-hidden flex flex-col items-center justify-center bg-brand-background ">
        {{wallets}}
        <div className="relative w-full h-full flex flex-col items-center justify-center">
            <div className="flex flex-col items-center justify-center h-full w-full px-2 md:px-10">
                <div className="relative z-1 md:max-w-3xl w-full bg-gray-900/90 filter backdrop-blur-sm py-4 rounded-md px-2 md:px-10 flex flex-col items-center">
                    <button v-if="wallet"
                            className="absolute right-4 bg-indigo-600 transition duration-200 ease-in-out font-chalk border-2 border-[rgba(0,0,0,1)] shadow-[0px_3px_0px_0px_rgba(0,0,0,1)] active:shadow-none px-4 py-2 rounded-md text-sm text-white tracking-wide uppercase">
                        Disconnect
                    </button>

                    <h1 className="font-coiny uppercase font-bold text-3xl md:text-4xl bg-gradient-to-br  from-brand-green to-brand-blue bg-clip-text text-transparent mt-3">
                        {{paused ? 'Paused' : 'Public Sale'}}
                    </h1>
                    <h3 className="text-sm text-pink-200 tracking-widest">
                        {{wallet?.accounts[0]?.address
                ? wallet?.accounts[0]?.address.slice(0, 8) +
                  '...' +
                  wallet?.accounts[0]?.address.slice(-4)
                : ''}}
                    </h3>

                    <div className="flex flex-col md:flex-row md:space-x-14 w-full mt-10 md:mt-14">
                        <div className="relative w-full">
                            <div className="font-coiny z-10 absolute top-2 left-2 opacity-80 filter backdrop-blur-lg text-base px-4 py-2 bg-black border border-brand-purple rounded-md flex items-center justify-center text-white font-semibold">
                                <p>
                                    <span className="text-brand-pink">{{totalMinted}}</span> /{{' '}}
                                    {{maxSupply}}
                                </p>
                            </div>

                            <img src="/images/13.jpg"
                                 className="object-cover w-full sm:h-[320px] md:w-[320px] rounded-md" />
                        </div>

                        <div className="flex flex-col items-center w-full px-4 mt-16 md:mt-0">
                            <div className="font-coiny flex items-center justify-between w-full">

                                <input className="flex items-center justify-center flex-1 grow text-center font-bold text-brand-pink text-base md:text-lg w-40 h-10"
                                       v-model="mintAmount"
                                        />

                            </div>

                            <p style="font-family: auto;" className="text-sm text-pink-200 tracking-widest mt-3">
                                Max Mint Amount: {{maxMintAmount}}
                            </p>

                            <div className="border-t border-b py-4 mt-16 w-full">
                                <div className="w-full text-xl font-coiny flex items-center justify-between text-brand-yellow">
                                    <p>Total</p>

                                    <div className="flex items-center space-x-3">
                                        <p>
                                            <!-- {{totalCount}} -->
                                            {{Number.parseFloat(price * mintAmount/(10**18)).toFixed(8)}}
                                            ETH
                                        </p>{{' '}}
                                        <span className="text-gray-400">+ GAS</span>
                                    </div>
                                </div>
                            </div>

                            <button v-show="wallet"
                                    className='font-coiny mt-12 w-full px-6 py-3 rounded-md text-2xl text-white  mx-4 tracking-wide uppercase'
                                    :disabled="isMinting || paused"
                                    onClick={publicMintHandler}>
                                {{isMinting ? 'Minting...' : 'Mint'}}
                            </button>

                            <button v-show="!wallet"
                                @click="toWallet"
                                    className="font-coiny mt-12 w-full bg-gradient-to-br from-brand-purple to-brand-pink shadow-lg px-6 py-3 rounded-md text-2xl text-white hover:shadow-pink-400/50 mx-4 tracking-wide uppercase">
                                Connect Wallet
                            </button>

                        </div>
                    </div>

                    <div v-show="status && status.message"
                         className="border rounded-md text-start h-full px-4 py-4 w-full mx-auto mt-8 md:mt-4">
                        <p className="flex flex-col space-y-2 text-white text-sm md:text-base break-words ...">
                            {{status.message}}
                        </p>
                    </div>

                    <!-- {/* Contract Address */} -->
                    <div className="border-t border-gray-800 flex flex-col items-center mt-10 py-2 w-full">
                        <h3 className="font-coiny text-2xl text-brand-pink uppercase mt-6">
                            Contract Address
                        </h3>
                        <a href="https://goerli.etherscan.io/address/0xeD5eFf8f176e8C827bEB1b548167b97051899bCf#readContract"
                           target="_blank"
                           rel="noopener noreferrer"
                           class="text-gray-400 mt-4"><span style="font-family: auto;" class="break-all ...">0xeD5eFf8f176e8C827bEB1b548167b97051899bCf</span></a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
// import { ethers } from "https://cdn.ethers.io/lib/ethers-5.2.esm.min.js";
// import { init } from '@web3-onboard/vue'
import { useOnboard,init } from '@web3-onboard/vue'
// import  ethers  from 'ethers'
// import { ethers } from "ethers";
import injectedModule from '@web3-onboard/injected-wallets'

import walletConnectModule from '@web3-onboard/walletconnect'
import coinbaseModule from '@web3-onboard/coinbase'
import fortmaticModule from '@web3-onboard/fortmatic'


import { reactive, ref, defineEmits, defineProps, computed } from 'vue'
export default {
    name: 'mint',
    setup () {
        const mintAmount = ref(1);  //薄荷（铸币）数量
        const maxMintAmount = ref(5000000000000000);  //最大薄荷（铸币）数量
        const totalMinted = ref(3640009268);  //已经开采量
        const maxSupply = ref(100000000000);   //最大供给
        // const price = ref(100000000);   //单价
        const price = ref(100);   //单价
        const paused = ref(false);   

        const isMinting = ref(false);
        const status = ref({ message: '' });

const injected = injectedModule();
const walletConnect = walletConnectModule()
const coinbaseWallet = coinbaseModule()
const infuraKey = 'ababf9851fd845d0a167825f97eeb12b'
const rpcUrl = `https://mainnet.infura.io/v3/${infuraKey}`
const web3Onboard = init({
//   wallets: [injected],
  wallets: [injected,walletConnect,coinbaseWallet],
  chains: [
    {
      id: '0x1',
      token: 'ETH',
      label: 'Ethereum Mainnet',
      rpcUrl
    }
  ]
})
const { wallets, connectWallet, disconnectConnectedWallet, connectedWallet } = useOnboard({
  // ... other options
  connect: {
    autoConnectLastWallet: true
  }
})
    const connect = async () => connectWallet()

        // 去钱包购买
        const toWallet = () => {

            connect();
            // const ethersProvider = new ethers.providers.Web3Provider(connectedWallet.provider, 'any')
            return
          if (connectedWallet) {
  // if using ethers v6 this is:
  // ethersProvider = new ethers.BrowserProvider(wallet.provider, 'any')
  const ethersProvider = new ethers.providers.Web3Provider(connectedWallet.provider, 'any')
  // ..... do stuff with the provider
}
        }

        // 总价
        const totalCount = computed(() => {
            console.log(price, 9999, mintAmount);
            let upDowm = Number.parseFloat(price * mintAmount / (10 ** 18)).toFixed(8)
            return upDowm || '';
        })
        return {
            mintAmount,
            totalMinted,
            maxSupply,
            maxMintAmount,
            price
            ,paused
            ,toWallet
            // ,wallet
            , isMinting,
            status,
            wallets 
        }
    }
}
</script>

<style  scoped>
/* @import "./css/globals.css"; */
@import "./css/style.css";
/* @import "./css/owl.carousel.min.css";
@import "./css/lightbox.min.css"; */
</style>