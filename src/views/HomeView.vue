<template>
    <div id="home">
        <!-- Topbar Start -->
        <div class="container-fluid bg-primary py-3 d-none d-md-block">
            <div class="container">
                <div class="row">
                    <div class="col-md-6 text-center text-lg-left mb-2 mb-lg-0">
                        <div class="d-inline-flex align-items-center">
                            <a class="text-white pr-3"
                               href="https://discord.gg/Zn3UpPGHWz"
                               target="_blank">FAQ</a>
                            <span class="text-white">|</span>
                            <a class="text-white px-3"
                               href="https://discord.gg/Zn3UpPGHWz"
                               target="_blank">Help</a>
                            <span class="text-white">|</span>
                            <a class="text-white pl-3"
                               href="">White Paper (soon)</a>
                        </div>
                    </div>
                    <div class="col-md-6 text-center text-lg-right">
                        <div class="d-inline-flex align-items-center">
                            <a class="text-white px-3"
                               href="https://discord.gg/Zn3UpPGHWz"
                               target="_blank">
                                <i class="fab fa-discord"></i>
                            </a>
                            <a class="text-white px-3"
                               href="https://twitter.com/Pepecoinsarb"
                               target="_blank">
                                <i class="fab fa-twitter"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Topbar End -->

        <!-- Navbar Start -->
        <div class="container-fluid position-relative   nav-bar p-0">
            <div class="container-lg position-relative   p-0 px-lg-3"
                 style="z-index: 9">
                <nav class="navbar navbar-expand-lg bg-white navbar-light shadow p-lg-0">
                    <a href="./home"
                       class="navbar-brand d-block d-lg-none">
                        <h1 class="m-0 display-4 text-primary">
                            <span class="text-secondary">PEPE</span>
                        </h1>
                    </a>
                    <button type="button"
                            class="navbar-toggler"
                            data-toggle="collapse"
                            data-target="#navbarCollapse">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse justify-content-between"
                         id="navbarCollapse">
                        <div class="navbar-nav ml-auto py-0">
                            <a href="home"
                               class="nav-item nav-link active">Home</a>
                            <a href="#us"
                               class="nav-item nav-link">About US</a>
                            <a href="#tokenomics"
                               class="nav-item nav-link">Tokenomics</a>
                        </div>
                        <a href="home"
                           class="navbar-brand mx-5 d-none d-lg-block">
                            <h1 class="m-0 display-4 text-primary">
                                <img src="@/assets/img/apsobg.png"
                                     width="80"
                                     height="80" />
                            </h1>
                        </a>
                        <div class="navbar-nav mr-auto py-0">
                            <a href="#roadmap"
                               class="nav-item nav-link">Road Map</a>
                            <a href="#meme"
                               class="nav-item nav-link">Meme</a>
                            <a href="#friends"
                               class="nav-item nav-link">Our Friends</a>
                        </div>
                    </div>
                </nav>
            </div>
        </div>
        <!-- Navbar End -->
        <!-- Cover Start -->
        <div class="container-fluid p-0 mb-5 pb-5">
            <div id="header-carousel"
                 class="carousel slide"
                 data-ride="carousel">
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <img class="w-100 "
                             id="img1"
                             src="@/assets/img/apsocover.png"
                             alt="Image" />
                        <img class="w-100 "
                             id="img2"
                             src="@/assets/img/apsomobile2.png"
                             alt="Image" />
                        <div class="carousel-caption d-flex flex-column align-items-center justify-content-center">
                            <div class="p-3"
                                 style="max-width: 900px">

                                <h1 class="display-3 text-white mb-md-4">
                                    The Meme NFT on ARB Chain
                                </h1>
                                <a href="#us"
                                   class="btn btn-primary py-md-3 px-md-5 mt-2">About PEPE NFT</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Cover End -->

        <!-- About Start -->
        <div class="container-fluid py-5">
            <div class="container py-5">
                <div class="row justify-content-center">
                    <div class="col-lg-7">
                        <h1 class="section-title position-relative text-center mb-5"
                            id="us">
                            About PEPE 
                        </h1>
                    </div>
                </div>
                <div class="row">
                    <div class="col-lg-4 py-5">
                        <h4 class="font-weight-bold mb-3 Team">The Genesis</h4>
                        <p class="text-justify">
                            The most memeable memecoin in existence in arb chain. The dogs have had their day, it’s time for ArbPepe to take reign </p>
                
                        <!-- <a href="" class="btn btn-primary mt-2">Read our White Paper (soon)</a>            -->
                        <span
                           class="btn btn-primary mt-2">
                           <a href="https://opensea.io/collection/arbpepes/drop">Go to mint page</a> 
                        </span>
                    </div>
                    <div class="col-lg-4"
                         style="min-height: 400px">
                        <div class="position-relative h-100 rounded overflow-hidden">
                            <div class="container py-5">
                                <img class="position-relative w-100 h-auto"
                                     src="@/assets/img/apsobg.png" />
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-4 py-5">
                        <h4 class="font-weight-bold mb-3">The Project</h4>
                        <p class="text-justify">
                            Pepe is tired of watching everyone play hot potato with the endless derivative ShibaCumGMElonKishuTurboAssFlokiMoon Inu coins. The Inu’s have had their day. It’s time for the most recognizable meme in the world to take his reign as king of the memes.
                        </p>
    
                    </div>
                </div>
            </div>

        </div>
        <!-- About End -->

        <!-- Tokenomics Start -->

        <div class="container-fluid my-5 py-5 px-0">
            <div class="container py-5">
                <h1 class="section-title position-relative text-center mb-5"
                    id="tokenomics">
                    TOKENOMICS
                </h1>
                <div class="row  m-0">
                    <div class="col-md-6 px-0"
                         style="min-height: 500px">
                        <div class="position-relative  h-100">
                            <img class="position-absolute w-100 h-100"
                                 id="tok1"
                                 src="@/assets/img/tokenomics.png"
                                 style="object-fit: cover" />
                            <img class="position-absolute w-100 h-100"
                                 id="tok2"
                                 src="@/assets/img/tokenomics2.png"
                                 style="object-fit: cover" />

                            <span></span>

                        </div>
                    </div>
                    <div class="col-md-6 py-5 py-md-0 px-0">
                        <div class="h-100 d-flex flex-column align-items-left justify-content-center bg-primary p-5">

                            <h3 class="font-weight-bold  text-white mt-3 mb-4">
                                Distribution :
                            </h3>
                            <p class="text-white mb-4">

                            <h5 class="text-white text-left mb-4 ">
                                80% : NFT holder Airdrop
                           <br/> A pourcentage will be burn fortnightly. </h5>

                            <h5 class="text-white text-lg-left mb-4 ">
                                10% : Marketing <br> &emsp; To help the project grow..</h5>

                            <h5 class="text-white mb-4 ">
                                5% : Liquidity <br> &emsp; To help the project grow.
                            </h5>

                            <h5 class="text-white mb-4">
                                5% : Team Token
                            </h5>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Tokenomics End -->
        <!-- Road Map Start -->
        <div class="container-fluid py-5">
            <div class="container py-5">
                <div class="row">
                    <div class="col-lg-6">
                        <h1 class="section-title position-relative mb-5"
                            id="roadmap">ROAD MAP</h1>
                    </div>
                    <div class="col-lg-6 mb-5 mb-lg-0 pb-5 pb-lg-0"></div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <div class="owl-carousel service-carousel">
                            <div class="service-item">
                                <div class="service-img mx-auto">
                                    <img class="rounded-circle w-100 h-100 bg-light p-3"
                                         src="@/assets/img/apsobg.png"
                                         style="object-fit: cover" />
                                </div>
                                <div class="position-relative text-center bg-light rounded p-4 pb-5"
                                     style="margin-top: -75px">
                                    <h5 class="font-weight-semi-bold mt-5 mb-3 pt-5">
                                        STARTER
                                    </h5>
                                    <p>
                                    <h5 class="text-muted text-left mb-3">
                                        <i class="fa fa-check text-primary mr-3"></i>Website Launch
                                    </h5>
                                    <h5 class="text-muted text-left mb-3">
                                        <i class="fa fa-check text-primary mr-3"></i>Markrting Campaign
                                    </h5>
                                    <h5 class="text-muted text-left mb-3">
                                        <i class="fa fa-check text-primary mr-3"></i>Airdrop Campaign
                                    </h5>
                                    </p>
                                    <h5 class=" text-decoration-none text-secondary">More To Be Revealed Soon...</h5>
                                </div>
                            </div>
                            <div class="service-item ">
                                <div class="service-img  mx-auto">
                                    <img class="rounded-circle w-100 h-100 bg-light p-3"
                                         src="@/assets/img/apsobg.png"
                                         style="object-fit: cover" />
                                </div>
                                <div class="position-relative text-center bg-light rounded p-4 pb-5"
                                     style="margin-top: -75px">
                                    <h5 class="font-weight-semi-bold  mt-5 mb-3 pt-5">
                                        BOOSTER
                                    </h5>
                                    <p>
                                    <h5 class="text-muted text-left mb-3">
                                        <i class="text-primary mr-3"></i> Minting NFT
                                    </h5>
                                    <h5 class="text-muted text-left mb-3">
                                        <i class="text-primary mr-3"></i> AIRDROP $ArbPepe.
                                    </h5>
                                    <h5 class="text-muted text-left mb-3">
                                        <i class="text-primary mr-3"></i>REVEAL NFT
                                    </h5>

                                    </p>
                                    <h5 class=" text-decoration-none text-secondary">More To Be Revealed Soon...</h5>
                                </div>
                            </div>
                            <div class="service-item">
                                <div class="service-img mx-auto">
                                    <img class="rounded-circle w-100 h-100 bg-light p-3"
                                         src="@/assets/img/apsobg.png"
                                         style="object-fit: cover" />
                                </div>
                                <div class="position-relative text-center bg-light rounded p-4 pb-5"
                                     style="margin-top: -75px">
                                    <h5 class="font-weight-semi-bold mt-5 mb-3 pt-5">
                                        GROWN
                                    </h5>
                                    <p>
                                    <h5 class="text-muted text-left mb-3">
                                        <i class="text-primary mr-3"></i>DEX & CEX
                                    </h5>
                                    <h5 class="text-muted text-left mb-3">
                                        <i class="text-primary mr-3"></i>Animal Shelter
                                    </h5>
                                    <h5 class="text-muted text-left mb-3">
                                        <i class="text-primary mr-3"></i>Token Supply:210,000,000,000,000,000
                                    </h5>
                                    </p>
                                    <H5 class="   text-secondary">More To Be Revealed Soon... </h5>
                                </div>
                            </div>

                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Road Map End -->
        <!-- Meme Start -->
        <div class="container-fluid my-5 py-5 px-0">
            <div class="container py-5">
                <div class="row justify-content-center m-0">
                    <div class="col-lg-5">
                        <h1 class="section-title position-relative text-center mb-5"
                            id="meme">
                            WOOFY MEME
                        </h1>
                    </div>
                </div>
                <div class="row m-0 portfolio-container">
                    <div class="col-lg-4 col-md-6 p-0 portfolio-item">
                        <div class="position-relative overflow-hidden">
                            <img class="img-fluid w-100"
                                 src="@/assets/img/meme1e.png"
                                 alt="" />
                            <a class="portfolio-btn"
                               href="/img/meme1.png"
                               data-lightbox="portfolio">
                                <i class="fa fa-plus text-primary"
                                   style="font-size: 60px"></i>
                            </a>
                        </div>
                    </div>
                    <div class="col-lg-4 col-md-6 p-0 portfolio-item">
                        <div class="position-relative overflow-hidden">
                            <img class="img-fluid w-100"
                                 src="@/assets/img/meme2e.png"
                                 alt="" />
                            <a class="portfolio-btn"
                               href="/img/meme2.png"
                               data-lightbox="portfolio">
                                <i class="fa fa-plus text-primary"
                                   style="font-size: 60px"></i>
                            </a>
                        </div>
                    </div>
                    <div class="col-lg-4 col-md-6 p-0 portfolio-item">
                        <div class="position-relative overflow-hidden">
                            <img class="img-fluid w-100"
                                 src="@/assets/img/meme3e.png"
                                 alt="" />
                            <a class="portfolio-btn"
                               href="/img/meme3.png"
                               data-lightbox="portfolio">
                                <i class="fa fa-plus text-primary"
                                   style="font-size: 60px"></i>
                            </a>
                        </div>
                    </div>
                    <div class="col-lg-4 col-md-6 p-0 portfolio-item">
                        <div class="position-relative overflow-hidden">
                            <img class="img-fluid w-100"
                                 src="@/assets/img/meme4e.png"
                                 alt="" />
                            <a class="portfolio-btn"
                               href="/img/meme4.png"
                               data-lightbox="portfolio">
                                <i class="fa fa-plus text-primary"
                                   style="font-size: 60px"></i>
                            </a>
                        </div>
                    </div>
                    <div class="col-lg-4 col-md-6 p-0 portfolio-item">
                        <div class="position-relative overflow-hidden">
                            <img class="img-fluid w-100"
                                 src="@/assets/img/meme5e.png"
                                 alt="" />
                            <a class="portfolio-btn"
                               href="/img/meme5.png"
                               data-lightbox="portfolio">
                                <i class="fa fa-plus text-primary"
                                   style="font-size: 60px"></i>
                            </a>
                        </div>
                    </div>
                    <div class="col-lg-4 col-md-6 p-0 portfolio-item">
                        <div class="position-relative overflow-hidden">
                            <img class="img-fluid w-100"
                                 src="@/assets/img/meme6e.png"
                                 alt="" />
                            <a class="portfolio-btn"
                               href="/img/meme6.png"
                               data-lightbox="portfolio">
                                <i class="fa fa-plus text-primary"
                                   style="font-size: 60px"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Meme End -->

       
        <!-- Footer Start -->
        <div class="container-fluid footer bg-light py-5"
             style="margin-top: 90px">
            <div class="container text-center py-5">
                <div class="row">
                    <div class="col-12 mb-4">
                        <a href="home"
                           class="navbar-brand m-0">
                            <h1 class="m-0 mt-n2 display-4 text-primary">
                                <span class="text-secondary">PEPE </span>
                            </h1>
                        </a>
                    </div>
                    <div class="col-12 mb-4">
                        <a class="btn btn-outline-secondary btn-social mr-2"
                           href="https://twitter.com/Pepecoinsarb"
                           target="_blank"><i class="fab fa-twitter"></i></a>
                        <a class="btn btn-outline-secondary btn-social mr-2"
                           href="https://discord.gg/Zn3UpPGHWz"
                           target="_blank"><i class="fab fa-discord"></i></a>

                    </div>

                    <div class="col-12">
                        <p class="m-0">
                            &copy; PEPE Coin 2023 . All Rights Reserved
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <!-- Footer End -->

        <!-- Back to Top -->
        <a href="#"
           class="btn btn-secondary px-2 back-to-top"><i class="fa fa-angle-double-up"></i></a>
    </div>
</template>

<script>

export default {
    setup () {


        return {}
    },
    mounted () {
        // $(".service-carousel, .team-carousel").owlCarousel()
        // setTimeout(()=>{
            this.load()
        // },10000)
    },
    methods: {
        aa(){

        },
        load() {
                    (function ($) {
            "use strict";

            // Smooth scrolling on the navbar links
            $(".navbar-nav a").on('click', function (event) {
                if (this.hash !== "") {
                    event.preventDefault();

                    $('html, body').animate({
                        scrollTop: $(this.hash).offset().top - 45
                    }, 1500, 'easeInOutExpo');

                    if ($(this).parents('.navbar-nav').length) {
                        $('.navbar-nav .active').removeClass('active');
                        $(this).closest('a').addClass('active');
                    }
                }
            });


            // Back to top button
            $(window).scroll(function () {
                if ($(this).scrollTop() > 100) {
                    $('.back-to-top').fadeIn('slow');
                } else {
                    $('.back-to-top').fadeOut('slow');
                }
            });
            $('.back-to-top').click(function () {
                $('html, body').animate({ scrollTop: 0 }, 1500, 'easeInOutExpo');
                return false;
            });


            // Modal Video
            $(document).ready(function () {
                var $videoSrc;
                $('.btn-play').click(function () {
                    $videoSrc = $(this).data("src");
                });
                console.log($videoSrc);

                $('#videoModal').on('shown.bs.modal', function (e) {
                    $("#video").attr('src', $videoSrc + "?autoplay=1&amp;modestbranding=1&amp;showinfo=0");
                })

                $('#videoModal').on('hide.bs.modal', function (e) {
                    $("#video").attr('src', $videoSrc);
                })
            });


            // Service and team carousel
            $(".service-carousel, .team-carousel").owlCarousel({
                autoplay: false,
                smartSpeed: 1500,
                margin: 30,
                dots: false,
                loop: true,
                nav: true,
                navText: [
                    '<i class="fa fa-angle-left" aria-hidden="true"></i>',
                    '<i class="fa fa-angle-right" aria-hidden="true"></i>'
                ],
                responsive: {
                    0: {
                        items: 1
                    },
                    576: {
                        items: 1
                    },
                    768: {
                        items: 2
                    },
                    992: {
                        items: 3
                    }
                }
            });


            // Product carousel
            $(".product-carousel").owlCarousel({
                autoplay: false,
                smartSpeed: 1500,
                margin: 30,
                dots: false,
                loop: true,
                nav: true,
                navText: [
                    '<i class="fa fa-angle-left" aria-hidden="true"></i>',
                    '<i class="fa fa-angle-right" aria-hidden="true"></i>'
                ],
                responsive: {
                    0: {
                        items: 1
                    },
                    576: {
                        items: 2
                    },
                    768: {
                        items: 3
                    },
                    992: {
                        items: 4
                    }
                }
            });


            // Portfolio isotope and filter
            var portfolioIsotope = $('.portfolio-container').isotope({
                itemSelector: '.portfolio-item',
                layoutMode: 'fitRows'
            });

            $('#portfolio-flters li').on('click', function () {
                $("#portfolio-flters li").removeClass('active');
                $(this).addClass('active');

                portfolioIsotope.isotope({ filter: $(this).data('filter') });
            });


            // Testimonials carousel
            $(".testimonial-carousel").owlCarousel({
                autoplay: true,
                smartSpeed: 1500,
                dots: true,
                loop: true,
                items: 1
            });

        })(jQuery);
        }
    },
}
</script>

<style scoped>
@import "./style.css";
</style>