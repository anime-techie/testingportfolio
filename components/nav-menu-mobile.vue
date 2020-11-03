<template>
    <div class="nav-comp">
        <img src="../assets/svg/icon_menubar.svg" alt="Menubar" id="nav-menu-icon">
        <div class="nav-menu-mobile">
            <h1>Navigation Menu</h1>
            <ul class="nav-menu-side">
                <li id="home">
                        <nuxt-link to="/">Home</nuxt-link>
                        <div class="bottom-line"></div>
                </li>
                <li id="portfolio">
                        <nuxt-link to="/portfolio">Portfolio</nuxt-link>
                        <div class="bottom-line"></div>
                </li>
                <li id="technologies">
                    <nuxt-link to="/technologies">Technologies</nuxt-link>
                    <div class="bottom-line"></div>
                </li>
                <li id="about-us">
                    <nuxt-link to="/about-us">About Us</nuxt-link>
                    <div class="bottom-line"></div>
                </li>
                <li id="contact-us">
                    <a>Contact Us</a>
                    <div class="bottom-line"></div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .nav-menu-mobile{
        z-index: 12;
        position: fixed;
        background: white;
        box-shadow: -5px 0px 10px 0px rgba(0, 0, 0, 0.1);
        width: 60vw;
        right: 0;
        top: 0;
        bottom: 0;
        display: flex;
        flex-direction: column;
        padding: 5vw 5vw;
        transform: translateX(60vw);
        transition: 0.7s;
    }
    .nav-mobile-open{
        transform: translateX(0);
        transition: 0.7s;
    }
    .nav-menu-mobile ul{
        height: 40vh;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        list-style: none;
        padding: 0;
    }
</style>