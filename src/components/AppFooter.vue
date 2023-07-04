<template>
    <div class="footer-wrapper">
        <div class="footer__top">
            <div class="container">
                <a href="#" class="footer__top__link">
                    <img src="../../public/img/buy-comics-digital-comics.png" alt=""/>
                    <span class="link-title">DIGITAL COMICS</span>
                </a>
                <a href="#" class="footer__top__link">
                    <img src="../../public/img/buy-comics-merchandise.png" alt=""/>
                    <span class="link-title">DC MERCHANDISE</span>
                </a>
                <a href="#" class="footer__top__link">
                    <img src="../../public/img/buy-comics-subscriptions.png" alt=""/>
                    <span class="link-title">SUBSCRIPTION</span>
                </a>
                <a href="#" class="footer__top__link">
                    <img src="../../public/img/buy-comics-shop-locator.png" alt=""/>
                    <span class="link-title">COMIC SHOP LOCATOR</span>
                </a>
                <a href="#" class="footer__top__link">
                    <img src="../../public/img/buy-dc-power-visa.png" alt="">
                    <span class="link-title">DC POWER VISA</span>
                </a>
            </div>
        </div>
        <div class="footer__middle">
            <div class="container">
                <div class="footer__middle__left">
                    <div class="col">
                        <div class="col">
                            <h4 class="link-title">DC COMICS</h4>
                            <ul>
                                <li><a href="#">Characters</a></li>
                                <li><a href="#">Comics</a></li>
                                <li><a href="#">Movies</a></li>
                                <li><a href="#">TV</a></li>
                                <li><a href="#">Games</a></li>
                                <li><a href="#">Videos</a></li>
                                <li><a href="#">News</a></li>
                            </ul>
                        </div>
                        <div class="col">
                            <h4 class="link-title">SHOP</h4>
                            <ul>
                                <li><a href="#">Shop DC</a></li>
                                <li><a href="#">Shop DC Collectibles</a></li>
                            </ul>
                        </div>
                    </div>
                    <div class="col">
                        <h4 class="link-title">DC</h4>
                        <ul>
                            <li><a href="#">Terms Of Use</a></li>
                            <li><a href="#">lorem Privacy Policy (New)</a></li>
                            <li><a href="#">Ad Choices</a></li>
                            <li><a href="#">Advertising</a></li>
                            <li><a href="#">Jobs</a></li>
                            <li><a href="#">Subscriptions</a></li>
                            <li><a href="#">Talent Workshops</a></li>
                            <li><a href="#">CPSC Certificates</a></li>
                            <li><a href="#">Ratings</a></li>
                            <li><a href="#">Shop Help</a></li>
                            <li><a href="#">Contact Us</a></li>
                        </ul>
                    </div>
                    <div class="col">
                        <h4 class="link-title">SITES</h4>
                        <ul>
                            <li><a href="#">DC</a></li>
                            <li><a href="#">MAD Magazine</a></li>
                            <li><a href="#">DC Kids</a></li>
                            <li><a href="#">DC Universe</a></li>
                            <li><a href="#">DC Power Visa</a></li>

                        </ul>
                    </div>
                </div>
                <div class="footer__middle__right">
                    <img class="footer-logo-img" src="../../public/img/dc-logo-bg.png" alt=""/></div>
            </div>

            <div class="footer__bot">
                <div class="container">
                    <div class="footer__bot__left">
                        <button type="button" class="btn btn-sign-up">SIGN-UP NOW!</button>
                    </div>
                    <div class="footer__bot__right">
                        <h4>FOLLOW US</h4>
                        <i class="fa-brands fa-facebook"></i>
                        <i class="fa-brands fa-twitter"></i>
                        <i class="fa-brands fa-youtube"></i>
                        <i class="fa-brands fa-pinterest"></i>
                        <i class="fa-solid fa-location-dot"></i>
                    </div>
                </div>
            </div>
            <img class="footer__bg-img" src="../../public/img/footer-bg.jpg" alt="footer background"/>
        </div>

    </div>

</template>

<script>
export default {
    name: "AppFooter"
}
</script>

<style lang="sass" scoped>
a
    text-decoration: none
    color: white
    opacity: .65

    &:hover
        opacity: 1

ul
    list-style: none

    li
        margin-top: 8px

// FOOTER TOP
.footer__top
    background-color: #0282f9
    padding: 40px

    .container
        display: flex
        justify-content: space-between

        a
            opacity: .8
            font-weight: bold

            &:hover
                opacity: 1

        .footer__top__link
            width: 100%
            display: flex
            justify-content: center
            align-items: center

            img
                height: 50%

            .link-title
                margin-left: 15px
                color: white
                white-space: nowrap

// FOOTER MIDDLE
.footer__middle

    position: relative
    height: auto

    .footer__bg-img
        position: absolute
        top: 0
        left: 0
        width: 100%
        height: 100%
        object-fit: cover
        z-index: -10

    .container
        display: flex

        .footer__middle__left
            padding: 30px 0 30px 0
            flex: 1 1 auto
            display: flex
            gap: 50px

            .col
                display: flex
                flex-direction: column
                gap: 15px

            .link-title
                color: white
                white-space: nowrap
                font-size: 24px

        .footer__middle__right
            position: relative
            z-index: -1
            height: 100%
            flex: 0 0 50%

            .footer-logo-img
                position: absolute
                transform: translate(0, -20%)
                object-fit: none
                opacity: 0.7
                height: auto
                width: 100%

// FOOTER BOT
.footer__bot
    background-color: #303030
    padding: 40px

    .container
        display: flex
        justify-content: space-between

        .btn-sign-up
            cursor: pointer
            border: 2px solid #0282f9
            padding: 15px
            color: white
            background-color: #303030
            font-size: 16px

        .footer__bot__right
            display: flex
            align-items: center
            gap: 20px
fgsdfgs
            h4
                color: #0a7bea
                font-size: 20px

            i
                cursor: pointer
                font-size: 40px
                color: white
                opacity: .5

                &:hover
                    opacity: 1

</style>