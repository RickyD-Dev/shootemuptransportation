<script>
    import { onMount } from "svelte";

    let userHoveredFTL = false;
    let userHoveredLTL = false;

    function handleHoverFlat() {
        userHoveredFTL = true;
    }

    function handleHoverAwayFlat() {
        userHoveredFTL = false;
    }

    function handleHoverStep() {
        userHoveredLTL = true;
    }

    function handleHoverAwayStep() {
        userHoveredLTL = false;
    }

    onMount(() => {
        const lightTruckload = document.getElementById('light-truckload');
        const fullTruckload = document.getElementById('full-truckload');

        lightTruckload.addEventListener('mouseover', handleHoverStep);

        lightTruckload.addEventListener('mouseout', handleHoverAwayStep);

        fullTruckload.addEventListener('mouseover', handleHoverFlat);

        fullTruckload.addEventListener('mouseout', handleHoverAwayFlat);

        document.getElementById("contactButton").onclick = function () {
            location.href = "/contact";
        };

        document.getElementById("contactButton2").onclick = function () {
            location.href = "/contact";
        };

        document.getElementById("contactButton3").onclick = function () {
            location.href = "/contact";
        };

        document.getElementById("contactButton4").onclick = function () {
            location.href = "/contact";
        };

        return () => {
            lightTruckload.removeEventListener('mouseover', handleHoverStep),
            lightTruckload.removeEventListener('mouseout', handleHoverAwayStep),
            fullTruckload.removeEventListener('mouseover', handleHoverFlat),
            fullTruckload.removeEventListener('mouseout', handleHoverAwayFlat);
        }
    });
</script>

<section class="intro-section">
    <video class="bg-hero-video" muted autoplay loop disablepictureinpicture>
        <source src="videos/pexels-fearless-dreams-5598972-1080p.mp4" type="video/webm">
    </video>
    <div class="intro-wrapper">
        <div class="intro-sub-wrapper">
            <div class="intro-heading-container">
                <h1>Delivering with Precision and Speed</h1>
            </div>
            <div class="intro-quote-button-container">
                <button id="contactButton" class="quote-button">Get a Quote</button>
            </div>
        </div>
    </div>
</section>

<section id="chooseUs" class="why-choose-us-section">
    <div class="choose-us-img-container">
        <!-- <video class="bg-container-video" muted autoplay loop disablepictureinpicture>
            <source src="videos/pexels-fearless-dreams-5598972-1080p.mp4" type="video/webm">
        </video> -->
        <img src="images/IMG_7469.jpg" alt="">
        <!-- <img src="images/7565f2d2-85a7-4e9b-a9cf-e3c58539dd4d.JPG" alt=""> -->
    </div>
    <div class="choose-us-desc-container">
        <div class="desc-wrapper">
            <div class="choose-us-heading">
                <h3 class="third-heading">Why choose us? <i class="primary-icon fa-solid fa-handshake-simple"></i></h3>
                <h2 class="secondary-heading">We've got you covered</h2>
            </div>
            <div>
                <p class="primary-p">Shoot 'Em Up Transportation was founded on April 21, 2017. We run a family owned and family driven operation where all business is in house.</p>
                <p class="primary-p">We pride ourselves in providing reliable, efficient, and cost-effective freight trucking solutions. Our team is dedicated to making your freight transportation hassle-free, allowing you to focus on your core business activities.</p>
            </div>
        </div>
    </div>
</section>

<section id="solutions" class="services-section">
    <div class="services-heading-container">

        <div class="services-sub-heading-container">
            <h1 class="third-heading">Freight Transportation Solutions <i class="primary-icon fa-solid fa-globe"></i></h1>
        </div>

        <h1 class="primary-heading">Full Truckload & LTL Freight</h1>
        <p class="primary-p">We offer FTL (Full Truckload) and LTL (Less Than Truckload) services using our flatbed and step deck trailers. We also offer tarping and ramps for transporting vehicles.</p>

    </div>

    <div class="services-container">

        <div class="services-wrapper">
            <!-- <h2 class="secondary-heading">Flatbed</h2> -->
            <div class="services-description-container">
                <h2 class="secondary-heading">FTL Freight Shipping</h2>
                <p class="primary-p">Need to reserve an entire truck for a single shipment?</p>
                <p class="primary-p">Our FTL services are suitable for large quantities of cargo that can fill an entire truck, offering quicker and direct delivery to the destination.</p>
                <button id="contactButton2" class="quote-button">Get a Quote</button>
            </div>

            <div class="services-sub-container">
                <img src="images/73e90b5a-7191-4484-bc6b-935040b9fa2e.JPG" alt="">
                <div class="services-img-shadow"></div>
            </div>
        </div>

        <div class="services-wrapper">
            <!-- <h2 class="secondary-heading">Step Deck</h2> -->
            <div class="services-sub-container">
                <img src="images/34520759-2981-44a7-b1f5-f872fdd76898.JPG" alt="">
            </div>

            <div class="services-description-container">
                <h2 class="secondary-heading">LTL Freight Shipping</h2>
                <p class="primary-p">Don't need to fill an entire truck for a single shipment?</p>
                <p class="primary-p">Our LTL services combine multiple shipments from different customers into one truck. It's cost effective and ideal for smaller shipments.</p>
                <button id="contactButton2" class="quote-button">Get a Quote</button>
            </div>
        </div>

    </div>
</section>

<section id="carrierAssets" class="carrier-assets-section">
    <div class="carrier-assets-wrapper">
        <div class="carrier-assets-desc-container">
            <div class="desc-wrapper">
                <div class="carrier-assets-heading">
                    <h3 class="third-heading">Our Carrier Assets <i class="primary-icon fa-solid fa-truck-fast"></i></h3>
                    <h2 class="secondary-heading">Flatbed</h2>
                </div>
                <div>
                    <p class="primary-p">A flatbed trailer is a simple, open trailer with a flat, unenclosed platform for hauling a wide variety of cargo.</p>
                    <p class="primary-p">We recommend this solution for transporting items like construction materials, machinery, and oversized goods, thanks to its open design and easy loading and unloading capabilities.</p>
                </div>
            </div>
        </div>
        <div class="carrier-assets-img-container">
            <img src="images/dceb0433-dc75-4933-ae8c-162c1d8c22d5.JPG" alt="">
        </div>
    </div>
    <div class="carrier-assets-wrapper">
        <div class="carrier-assets-img-container">
            <img src="images/31929e2c-b540-4ab2-87d7-2ee6b3d1097d.JPG" alt="">
        </div>
        <div class="carrier-assets-desc-container">
            <div class="desc-wrapper">
                <div class="carrier-assets-heading">
                    <h3 class="third-heading">Our Carrier Assets <i class="primary-icon fa-solid fa-truck-fast"></i></h3>
                    <h2 class="secondary-heading">Step Deck</h2>
                </div>
                <div>
                    <p class="primary-p">A step deck trailer is a specialized flatbed with two levels - a higher and a lower deck.</p>
                    <p class="primary-p">We recommend this solution for transporting tall or oversized cargo like machinery and vehicles that won't fit on regular flatbeds. The lower deck provides clearance for taller items while maintaining stability, making it versatile for various specialized loads.</p>
                </div>
            </div>
        </div>
    </div>
</section>

<section id="routes" class="route-section">
    <div class="route-desc-container">
        <div class="route-wrapper">
            <div class="route-heading">
                <h1 class="third-heading">Our Routes <i class="primary-icon fa-solid fa-route"></i></h1>
                <h1 class="primary-heading">Experienced Across the Country</h1>
            </div>
            <div class="route-p-container">
                <p class="primary-p">We generally provide our services to the southwest area including Arizona, New Mexico, Texas, Oklahoma, Arkansas, and Louisiana, however, we are capable and familiar with delivering all over the country.</p>
            </div>

            <div class="route-img-container">
                <img class="map" src="images/route-map.svg" alt="">
            </div>
        </div>
    </div>
</section>

<section id="contact" class="contact-section">
    <div class="contact-heading-container">
        <h2 class="third-heading">Have any questions? <i class="primary-icon fa-solid fa-phone-flip"></i></h2>
        <h1 class="primary-heading">Contact Us</h1>
    </div>
    <div class="contact-button-container">
        <button id="contactButton4" class="quote-button">Get in Touch</button>
    </div>
</section>

<style>
    /* ----------------- INTRO SECTION ----------------- */

    .intro-section {
        display: flex;
        flex-direction: column;
        width: 100%;
        height: 100%;
        background: url(images/IMG_7469.jpg) 50% 50%;
        background-size: cover;
        position: relative;
        /* margin-top: -160px; */
    }

    .bg-hero-video {
        display: block;
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0%;
        left: 0%;
        right: 0%;
        bottom: 0%;
        object-fit: cover;
    }

    .intro-wrapper {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: relative;
        height: 100%;
        width: 100%;
        background-color: rgba(0,0,0,0.4);
        padding: 0px 25px;
    }

    .intro-sub-wrapper {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        max-width: 1400px;
    }

    .intro-heading-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-end;
        /* margin-top: 160px; */
        width: 100%;
    }

    .intro-heading-container h1 {
        color: #fff;
        font-family: 'Inter';
        font-size: 6rem;
        font-weight: 500;
        letter-spacing: -3px;
        text-align: right;
        max-width: 665px;
    }

    .intro-quote-button-container {
        display: flex;
        justify-content: flex-end;
        width: 100%;
        padding-top: 30px;
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
    }

    .quote-button:hover {
        color: #000;
        background-color: rgb(255,255,255);
        /* border: 2px solid #000; */
    }

    @media screen and (max-width: 1024px) {
        .intro-heading-container h1 {
            font-size: 5rem;
        }

        .quote-button {
            font-size: 1.3rem;
        }
    }

    @media screen and (max-width: 580px) {
        .intro-heading-container {
            align-items: center;
        }

        .intro-heading-container h1 {
            text-align: center;
            font-size: 3rem;
            max-width: 400px;
        }

        .intro-quote-button-container {
            justify-content: center;
        }
    }

    /* ----------------- WHY CHOOSE US SECTION ----------------- */

    .why-choose-us-section {
        display: flex;
        width: 100%;
        height: 100%;
        background-color: #d2d2d2;
    }

    .choose-us-img-container {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        position: relative;
        height: 100%;
    }

    .choose-us-img-container img {
        object-fit: cover;
        object-position: 15% 100%;
        filter: brightness(0.9);
    }

    .bg-container-video {
        object-fit: cover;
        display: block;
        position: absolute;
        width: 70%;
        height: 60%;
        border-radius: 15px;
    }

    .choose-us-desc-container {
        background-color: #d2d2d2;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 80%;
        padding: 1.2rem;
    }

    .desc-wrapper {
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 100%;
        max-width: 600px;
    }

    .choose-us-heading {
        padding-bottom: 30px;
    }

    @media screen and (max-width: 380px) {
        .desc-wrapper {
            padding: 0;
        }
    }

    @media screen and (max-width: 580px) {
        .why-choose-us-section {
            height: 100% !important;
        }

        .choose-us-desc-container {
            width: 100%;
        }

        .desc-wrapper {
            padding: 0 !important;
        }
    }

    @media screen and (max-width: 1024px) {
        .why-choose-us-section {
            height: auto;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
    }

    /* ----------------- SERVICES SECTION ----------------- */

    .services-section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        padding-bottom: 100px;
        /* background-color: #1d1d1d; */
        background-color: #252a33;
        /* background: linear-gradient(#1d1d1d, #252a33); */
    }

    .services-heading-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-top: 100px;
        text-align: center;
        width: 100%;
    }

    .services-heading-container .primary-p {
        color: #f1f1f1;
        padding-top: 8px;
        max-width: 800px;
    }

    .services-heading-container .primary-heading {
        color: #fff;
    }

    .services-sub-heading-container {
        display: flex;
        width: 100%;
        justify-content: center;
    }

    .services-sub-heading-container .third-heading {
        color: #d1d1d1;
    }

    .services-sub-heading-container .primary-icon {
        color: #5b5b5b;
    }

    .services-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        gap: 50px;
        margin-top: 60px;
        padding: 0px 2rem;
        max-width: 1400px;
    }

    .services-wrapper {
        display: flex;
        justify-content: center;
        align-items: center;
        /* max-width: 700px; */
        gap: 50px;
        width: 100%;
        text-align: center;
    }

    .services-wrapper .secondary-heading {
        padding-bottom: 10px;
    }

    .services-wrapper .secondary-heading,
    .services-wrapper .primary-p {
        color: #f1f1f1;
    }

    .services-wrapper .primary-p {
        width: 100%;
        max-width: 500px;
    }

    .services-wrapper .quote-button {
        margin-top: 10px;
    }

    .services-sub-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        /* max-width: 700px; */
        position: relative;
        border-radius: 5px;
        overflow: hidden;
        margin-bottom: 1rem;
    }

    .services-sub-container img {
        position: relative;
        z-index: 2;
    }

    .services-description-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
    }

    .services-img-shadow {
        display: block;
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: #fff;
        z-index: 1;
    }

    /* .services-desc-container {
        border: 3px solid #f1f1f1;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: absolute;
        width: 100%;
        height: 100%;
        padding: 45px 25px;
        background-color: rgba(0,0,0,0.1);
        transition: background-color 200ms ease-in-out;
    } */

    /* .services-desc-container:hover {
        cursor: pointer;
        background-color: rgba(0,0,0,0.8);
    } */

    /* .show-heading {
        opacity: 1;
        font-size: 3rem;
        color: #fff;
        padding-bottom: 25px;
        text-align: center;
        transition: opacity 200ms ease-in-out;
        text-transform: none;
        font-weight: 500;
    } */

    .services-desc .secondary-heading {
        opacity: 0;
        color: #fff;
        padding-bottom: 25px;
        text-align: center;
        transition: opacity 200ms ease-in-out;
        text-transform: none;
        letter-spacing: 0;
    }

    .services-desc {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
    }

    .services-desc .primary-p {
        opacity: 0;
        color: #fff;
        font-size: 1.3rem;
        transition: opacity 200ms ease-in-out;
        text-align: center;
        width: 85%;
    }

    .show-desc {
        padding-bottom: 10px;
        font-size: 1.3rem;
        font-weight: 400;
        opacity: 1;
        color: #fff;
        transition: opacity 200ms ease-in-out;
        text-align: center;
        width: 85%;
    }

    .services-desc .quote-button {
        margin-top: 16px;
        font-size: 1.4rem;
        color: #fff;
        border: 2px solid #fff;
        background-color: transparent;
        height: 50px;
        width: 200px;
        transition: all 200ms ease;
        cursor: pointer;
        margin-top: 16px;
        opacity: 1;
        transition: all 200ms ease-in-out;
        border-radius: 5px;
    }

    .show-button {
        font-size: 1.4rem;
        color: #fff;
        border: 2px solid #fff;
        background-color: transparent;
        height: 50px;
        width: 200px;
        transition: all 200ms ease;
        cursor: pointer;
        margin-top: 16px;
        opacity: 1;
        transition: all 200ms ease-in-out;
        border-radius: 5px;
    }

    .show-button:hover {
        color: #000;
        background-color: rgb(255,255,255);
        /* border: 2px solid #000; */
    }

    @media screen and (max-width: 1024px) {
        .services-wrapper .secondary-heading {
            font-size: 2.1rem;
        }

        .services-wrapper .primary-p {
            font-size: 1.1rem;
        }
    }

    @media screen and (max-width: 804px) {
        .services-heading-container .primary-p {
            max-width: 750px;
        }

        .services-container {
            margin-top: 30px;
        }

        .services-wrapper {
            flex-direction: column;
            gap: 0;
        }

        .services-description-container {
            order: 2;
        }

        .services-wrapper .primary-p {
            max-width: 100%;
        }
    }

    @media screen and (max-width: 380px) {
        .services-heading-container .primary-heading {
            font-size: 2rem;
            max-width: 300px;
        }

        .services-heading-container .primary-p {
            padding: 8px 2.2rem;
        }

        .services-container {
            padding: 0px;
        }

        .services-wrapper .secondary-heading {
            color: #d2d2d2;
            font-size: 1.8rem;
        }

        .services-description-container {
            padding: 0px 1rem;
        }

        .services-sub-container {
            border-radius: 0;
        }
    }

    /* ----------------- OUR CARRIER ASSETS SECTION ----------------- */

    .carrier-assets-section {
        display: flex;
        flex-direction: column;
        width: 100%;
    }

    .carrier-assets-wrapper {
        display: flex;
        width: 100%;
        background-color: #d2d2d2;
    }

    .carrier-assets-desc-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
    }

    .desc-wrapper {
        display: flex;
        flex-direction: column;
        justify-content: center;
        max-width: 600px;
        padding: 1.2rem;
    }

    .carrier-assets-heading {
        padding-bottom: 30px;
    }

    .carrier-assets-img-container {
        width: 100%;
    }

    .carrier-assets-img-container img {
        object-fit: cover;
    }

    @media screen and (max-width: 804px) {
        .carrier-assets-wrapper {
            flex-direction: column;
        }

        .carrier-assets-img-container {
            order: 1;
        }

        .carrier-assets-desc-container {
            padding: 1.2rem;
        }
    }

    /* ----------------- ROUTE SECTION ----------------- */

    .route-section {
        display: flex;
        flex-direction: column;
        width: 100%;
        height: 100%;
    }

    .route-img-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: relative;
        width: 70%;
    }

    .line-container {
        display: block;
        position: absolute;
        top: 66%;
        left: 24%;
        width: 15%;
        height: auto;
        filter: hue-rotate(343deg);
        transform: rotate(203deg);
    }

    .line-container2 {
        display: block;
        position: absolute;
        top: 68%;
        left: 43%;
        width: 15%;
        height: auto;
        filter: hue-rotate(343deg);
        transform: rotate(331deg);
    }

    .line-container3 {
        display: block;
        position: absolute;
        top: 68%;
        left: 45%;
        width: 13%;
        height: auto;
        filter: hue-rotate(343deg);
        transform: rotate(46deg);
    }

    .route-desc-container {
        /* background-color: #041E42; */
        background: linear-gradient(#041E42, rgba(37, 42, 51, 0.9));
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;
        padding: 50px 0px;
    }

    .route-wrapper {
        display: flex;
        align-items: center;
        width: 100%;
        flex-direction: column;
        text-align: center;
        max-width: 1300px;
    }

    .route-heading {
        padding-top: 25px;
        text-align: center;
    }

    .route-heading .third-heading,
    .route-wrapper .primary-p {
        color: #f1f1f1;
    }

    .route-heading .primary-heading {
        color: #a9a9a9;
    }

    .route-heading .primary-icon {
        color: #315187;
    }

    .route-wrapper .primary-p {
        padding: 8px 0px;
        max-width: 800px;
        /* color: #f1f1f1; */
    }

    .map {
        stroke: red;
    }

    @media screen and (max-width: 804px) {
        .route-section {
            height: auto;
        }

        .route-heading {
            max-width: 525px;
        }

        .route-p-container {
            max-width: 700px;
            margin-bottom: 30px;
        }

        .route-img-container {
            width: 95%;
        }
    }

    @media screen and (max-width: 580px) {
        .route-heading {
            max-width: 350px;
        }

        .route-wrapper .primary-p {
            padding: 8px 1.2rem;
        }
    }

    /* ----------------- CONTACT SECTION ----------------- */

    .contact-section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        background-color: #d2d2d2;
        padding: 50px 0px;
    }

    .contact-heading-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        padding-bottom: 25px;
    }

    .contact-button-container {
        display: flex;
        width: 100%;
        justify-content: center;
        align-items: center;
    }

    .contact-button-container .quote-button {
        /* color: #041E42; */
        color: #f1f1f1;
        background-color: #041E42;
        border: 2px solid #003594;
        text-transform: uppercase;
        font-size: 1rem;
        border-radius: 5px;
    }

    .contact-button-container .quote-button:hover {
        color: #041E42;
        background-color: #f1f1f1;
    }
</style>