<template>
    <footer class="footer">
            <div class="social_section">
                <a href="http://"><img src="..\assets\svg\icon_linkedin.svg" alt="LinkedIn Profile"></a>
                <a href="http://"><img src="..\assets\svg\icon_github.svg" alt="Github Profile"></a>
                <a href="http://"><img src="..\assets\svg\icon_insta.svg" alt="Instagram Page"></a>
                <a href="http://"><img src="..\assets\svg\icon_fb.svg" alt="Facebook Page"></a>
            </div>
            <div class="copyright_statement">© aSync.data. All Rights Reserved.</div>        
    </footer>
</template>

<script>
export default {
    mounted () {
    this.$nextTick(() => {
                          
    })
  }
}
</script>



<style scoped>
    .footer{
        height: 20vh;
        width: 100%;
        padding: 1vw 5vw;
        background: var(--main-black);
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .social_section{
        width: 100%;
        display: flex;
        justify-content: space-evenly;
    }
    .social_section a{
        background: white;
        border-radius: 50%;
        padding: 15px;
        display: flex;
        justify-content: center;
        align-items: center;
        opacity: 0.4;
        transition: 0.5s;
    }
    .social_section a:hover{
        opacity: 1;
        transition: 0.5s;
    }
    .copyright_statement{
        color: var(--light-stroke);
    }

</style>
