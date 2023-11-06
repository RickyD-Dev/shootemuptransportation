<script>
    import { onMount } from "svelte";

    let userScrolledDown = false;

    let userOpenedMobileNav = false;

    function handleScroll() {
        if (window.scrollY > 250) {
            userScrolledDown = true;
        } else {
            userScrolledDown = false;
        }
    }

    function handleMobileNav() {
        userOpenedMobileNav = !userOpenedMobileNav;
    }

    onMount(() => {
        window.addEventListener('scroll', handleScroll);

        document.getElementById("contactButton5").onclick = function () {
            location.href = "/contact";
        };

        return () => {
            window.removeEventListener('scroll', handleScroll);
        }
    });
</script>

<header class="primary-header">
    <div class={userScrolledDown ? "updated-primary-nav-wrapper" : "primary-nav-wrapper"}>
        <div class="primary-nav-container">
            <div class="logo-container">
                <a class="home-link" href="/">
                    <img src="images/shootemup_transparent_logo.png" alt="Shoot em' Up Transportation Logo">
                </a>
            </div>
            <nav class="primary-nav">
                <ul class="nav-list">
                    <li class="nav-link">
                        <a href="/#chooseUs">About Us <i class="fa-solid fa-handshake-simple"></i></a>
                    </li>
                    <li class="nav-link">
                        <a href="/#solutions">Freight Solutions <i class="fa-solid fa-globe"></i></a>
                    </li>
                    <li class="nav-link">
                        <a href="/#carrierAssets">Carrier Assets <i class="fa-solid fa-truck-fast"></i></a>
                    </li>
                    <li class="nav-link">
                        <a href="/#routes">Routes <i class="fa-solid fa-route"></i></a>
                    </li>
                    <li class="nav-link">
                        <a href="/contact">Contact Us <i class="fa-solid fa-phone-flip"></i></a>
                    </li>
                </ul>
            </nav>

            <nav class={userOpenedMobileNav ? "primary-mobile-nav--open" : "primary-mobile-nav"}>
                <ul class="nav-list">
                    <li class="nav-link">
                        <a href="/#chooseUs">About Us <i class="fa-solid fa-handshake-simple"></i></a>
                    </li>
                    <li class="nav-link">
                        <a href="/#solutions">Freight Solutions <i class="fa-solid fa-globe"></i></a>
                    </li>
                    <li class="nav-link">
                        <a href="/#carrierAssets">Carrier Assets <i class="fa-solid fa-truck-fast"></i></a>
                    </li>
                    <li class="nav-link">
                        <a href="/#routes">Routes <i class="fa-solid fa-route"></i></a>
                    </li>
                    <li class="nav-link">
                        <a href="/contact">Contact Us <i class="fa-solid fa-phone-flip"></i></a>
                    </li>
                </ul>
            </nav>
            <!-- Primary burger menu nav -->
            <button class="burger-menu-wrapper" on:click={handleMobileNav}>
                <div class={userOpenedMobileNav ? "burger-layer burger-layer__open" : "burger-layer"}></div>
                <div class={userOpenedMobileNav ? "burger-layer burger-layer__open" : "burger-layer"}></div>
                <div class={userOpenedMobileNav ? "burger-layer burger-layer__open" : "burger-layer"}></div>
            </button>
            <!-- Icons Navigation Menu -->
            <nav class={userScrolledDown ? "secondary-nav-open" : "secondary-nav-closed"}>
                <ul class="secondary-nav-list">
                    <li class="nav-link">
                        <a href="/"><i class="fa-solid fa-house"></i></a>
                        <span class="secondary-nav-item">
                            <span class="secondary-nav-content">Home</span>
                        </span>
                    </li>
                    <li class="nav-link">
                        <a href="/#chooseUs"><i class="fa-solid fa-handshake-simple"></i></a>
                        <span class="secondary-nav-item">
                            <span class="secondary-nav-content">About Us</span>
                        </span>
                    </li>
                    <li class="nav-link">
                        <a href="/#solutions"><i class="fa-solid fa-globe"></i></a>
                        <span class="secondary-nav-item">
                            <span class="secondary-nav-content">Freight Solutions</span>
                        </span>
                    </li>
                    <li class="nav-link">
                        <a href="/#carrierAssets"><i class="fa-solid fa-truck-fast"></i></a>
                        <span class="secondary-nav-item">
                            <span class="secondary-nav-content">Assets</span>
                        </span>
                    </li>
                    <li class="nav-link">
                        <a href="/#routes"><i class="fa-solid fa-route"></i></a>
                        <span class="secondary-nav-item">
                            <span class="secondary-nav-content">Routes</span>
                        </span>
                    </li>
                    <li class="nav-link">
                        <a href="/contact"><i class="fa-solid fa-phone-flip"></i></a>
                        <span class="secondary-nav-item">
                            <span class="secondary-nav-content">Contact Us</span>
                        </span>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</header>

<slot></slot>

<footer>
    <!-- FINISH ADDING FOOTER -->
    <div class="footer-wrapper">
        <div class="footer-logo-desc-container">
            <div class="footer-logo">
                <img src="images/shootemup_transparent_logo.png" alt="Shoot em' Up Transportation Logo">
            </div>
            <p class="footer-copyright">&copy; Shoot 'Em Up Transportation. All Rights Reserved.</p>
        </div>
        <div class="footer-nav-container">
            <ul class="footer-nav">
                <li class="footer-nav-item">
                    <a href="#chooseUs">Why Choose Us? <i class="fa-solid fa-handshake-simple"></i></a>
                </li>
                <li class="footer-nav-item">
                    <a href="#solutions">Freight Transportation Solutions <i class="fa-solid fa-globe"></i></a>
                </li>
                <li class="footer-nav-item">
                    <a href="#carrierAssets">Our Carrier Assets <i class="fa-solid fa-truck-fast"></i></a>
                </li>
                <li class="footer-nav-item">
                    <a href="#routes">Our Routes <i class="fa-solid fa-route"></i></a>
                </li>
                <li class="footer-nav-item">
                    <a href="#contact">Contact Us <i class="fa-solid fa-phone-flip"></i></a>
                </li>
            </ul>
        </div>
        <div class="footer-contact-container">
            <p class="primary-p">Contact Us</p>
            <p class="primary-p">Phone: (999) 999-9999</p>
            <button id="contactButton5" class="quote-button">Get a Quote</button>
        </div>
    </div>
</footer>

<style>
    .primary-header {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        background-color: transparent;
        position: relative;
        z-index: 99;
    }

    .primary-nav-wrapper {
        background-color: transparent;
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        /* position: fixed; */
        position: absolute;
        top: 0;
        transition: background-color 500ms ease-in-out;
        z-index: 2;
    }

    /* .updated-primary-nav-wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        position: fixed;
        top: 0;
        background-color: rgba(0,0,0,0.8);
        transition: background-color 500ms ease-in-out;
    } */

    .primary-nav-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        max-width: 1850px;
        position: relative;
        /* position: fixed;
        top: 0; */
        padding: 10px 1% 0px;
    }

    .logo-container {
        width: 165px;
        height: auto;
    }

    .home-link {
        display: block;
        width: 100%;
        height: 100%;
    }

    /* ---------- PRIMARY NAV STYLES ---------- */

    .primary-nav {
        display: flex;
        flex-direction: column;
        width: 100%;
    }

    .primary-mobile-nav {
        display: none;
    }

    .primary-mobile-nav--open {
        display: none;
    }

    .nav-list {
        display: flex;
        width: 100%;
        justify-content: flex-end;
        align-items: center;
        gap: 20px;
    }

    .nav-link {
        color: rgba(255, 255, 255, 0.8);
        font-size: 1.195rem;
        font-weight: 400;
        transition: color 200ms ease;
        cursor: pointer;
        position: relative;
    }

    @media screen and (max-width: 1024px) {
        .nav-link {
            font-size: 1.1rem;
        }
    }

    @media screen and (max-width: 991px) {
        .logo-container {
            width: 140px;
        }

        .primary-nav {
            display: none;
        }

        .primary-mobile-nav {
            display: flex;
            flex-direction: column;
            background-color: rgba(0, 0, 0, 0.63);
            height: 100%;
            width: 300px;
            position: fixed;
            top: 0;
            right: 0;
            transform: translateX(100%);
            transition: transform 0.5s ease-in-out;
            backdrop-filter: blur(15px);
        }

        .primary-mobile-nav--open {
            display: flex;
            flex-direction: column;
            background-color: rgba(0, 0, 0, 0.63);
            height: 100%;
            width: 300px;
            position: fixed;
            top: 0;
            right: 0;
            backdrop-filter: blur(15px);
            transform: translateX(0);
            transition: transform 0.5s ease-in-out;
        }

        .nav-list {
            flex-direction: column;
            width: 100%;
            height: 100%;
            justify-content: center;
            align-items: flex-end;
            gap: 50px;
            padding-right: 25px;
        }

        .nav-link {
            color: #fff;
            font-size: 1.25rem;
        }
    }

    /* ---------- SECONDARY NAV STYLES ---------- */

    .secondary-nav-closed {
        display: flex;
        opacity: 0;
        transition: opacity 300ms ease-in-out;
        z-index: -1;
        flex-direction: column;
        width: 100%;
        background-color: transparent;
        position: fixed;
        top: 0;
        left: 0;
        height: 35px;
    }

    .secondary-nav-open {
        display: flex;
        flex-direction: column;
        width: 100%;
        background-color: transparent;
        position: fixed;
        top: 0;
        left: 0;
        height: 35px;
        opacity: 1;
        transition: opacity 300ms ease-in-out;
        z-index: 10;
    }

    .secondary-nav-list {
        display: flex;
        background-color: transparent;
        width: 100%;
        height: 100%;
        justify-content: center;
        align-items: center;
        gap: 80px;
        padding: 5px 0px;
        transition: background-color 200ms ease-in-out;
    }

    .secondary-nav-list:hover {
        background-color: rgba(0, 0, 0, 0.8);
    }

    .secondary-nav-item {
        color: #000;
        position: absolute;
        top: 20px;
        right: -88px;
        padding: 5px;
        width: 200px;
        font-size: 1rem;
        margin-top: 15px;
        text-align: center;
        visibility: hidden;
        opacity: 0;
        transition: opacity 200ms ease-in-out;
    }

    .secondary-nav-item::after {
        width: 0;
        height: 0;
        border-bottom: 5px solid #f1f1f1;
        border-right: 5px solid rgba(0,0,0,0);
        border-left: 5px solid rgba(0,0,0,0);
        position: absolute;
        left: 48%;
        content: "";
        top: 0;
        -webkit-transform: translateY(-100%);
        -ms-transform: translateY(-100%);
        transform: translateY(-100%);
        content: "";
    }

    .nav-link:nth-child(2) .secondary-nav-item {
        right: -87px;
    }

    .nav-link:nth-child(3) .secondary-nav-item {
        right: -89px;
    }

    .nav-link:nth-child(4) .secondary-nav-item {
        right: -87px;
    }

    .nav-link:nth-child(5) .secondary-nav-item {
        right: -90px;
    }

    .secondary-nav-content {
        background-color: #f1f1f1;
        border-radius: 5px;
        padding: 5px;
    }

    .nav-link:hover .secondary-nav-item {
        visibility: visible;
        opacity: 1;
    }

    /* .nav-link:hover .secondary-nav-item .secondary-nav-content {
        
    } */

    /* ---------- BURGER MENU STYLES ---------- */

    .burger-menu-wrapper {
        display: none;
        flex-direction: column;
        height: 30px;
        width: 35px;
        position: relative;
        margin-right: 15px;
        background-color: transparent;
        border: none;
    }

    .burger-layer {
        height: 3px;
        width: 100%;
        background-color: #fff;
        border-radius: 15px;
        transition: all 280ms ease-in-out;
    }

    .burger-layer__open {
        position: relative;
        animation: fade 400ms ease-in-out forwards;
    }

    .burger-layer__open:nth-child(1) {
        top: 4px;
        transform: rotate(45deg);
    }

    .burger-layer__open:nth-child(2) {
        opacity: 0 !important;
        margin: 0 !important;
    }

    .burger-layer__open:nth-child(3) {
        bottom: 2px;
        transform: rotate(-45deg);
        margin: 0 !important;
    }

    .burger-layer:nth-child(2),
    .burger-layer:nth-child(3) {
        margin-top: 6px;
    }

    @media screen and (max-width: 991px) {
        .burger-menu-wrapper {
            display: flex;
            justify-content: center;
            align-items: center;
        }
    }

    @media screen and (max-width: 580px) {
        .burger-menu-wrapper {
            width: 30px;
        }

        .secondary-nav-list {
            gap: 35px;
        }
    }

    @keyframes fade {
        0% {
            opacity: 0;
        }

        100% {
            opacity: 1;
        }
    }

    /* ---------- FOOTER STYLES ---------- */

    footer {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 100px 0px;
        background-color: #252a33;
        width: 100%;
    }

    .footer-wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        max-width: 1400px;
    }

    .footer-logo-desc-container {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .footer-logo {
        max-width: 300px;
        width: 100%;
    }

    .footer-copyright {
        font-size: 0.7rem;
        font-weight: 400;
        color: #f1f1f1;
    }

    .footer-nav-container {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        border-left: 1px solid #f1f1f1;
        border-right: 1px solid #f1f1f1;
    }

    .footer-nav {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 10px;
    }

    .footer-nav-item {
        font-weight: 400;
    }

    .footer-contact-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
    }

    .footer-contact-container .primary-p:first-child {
        font-size: 1.4rem;
    }

    .footer-contact-container .primary-p {
        color: #f1f1f1;
        font-size: 1rem;
    }

    .quote-button {
        font-size: 1.4rem;
        color: #fff;
        border: 2px solid #fff;
        background-color: transparent;
        height: 50px;
        width: 200px;
        transition: all 200ms ease;
        cursor: pointer;
        border-radius: 5px;
        margin-top: 15px;
    }

    .quote-button:hover {
        color: #000;
        background-color: rgb(255,255,255);
        /* border: 2px solid #000; */
    }

    @media screen and (max-width: 900px) {
        .footer-wrapper {
            flex-direction: column;
            gap: 40px;
            max-width: 400px;
        }

        .footer-nav-container {
            border-left: none;
            border-right: none;
            border-top: 1px solid #f1f1f1;
            border-bottom: 1px solid #f1f1f1;
            padding: 25px 0px;
        }
    }
</style>