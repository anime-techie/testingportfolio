<template>
    <div>
        <div class="overlay"></div>
        <div class="contact-form">
                <div class="page-header">
                <div class="section_head_text">Contact Form</div>
                        <img src="../assets/svg/close-btn.svg" alt="Close Button" class="close-btn">
                </div>
                <form action="submit" method="post">
                    <div class="form-grp name-grp">
                        <label for="name">Name</label>
                        <input type="text" name="" placeholder="for e.g. Alex Smith">
                    </div>
                    <div class="form-grp email-grp">
                        <label for="email">Email</label>
                        <input type="text" name="" placeholder="your-email @ valid-email-client.com">
                    </div>
                    <div class="form-grp msg-grp">
                        <label for="message">Message</label>
                        <textarea name="message" rows="10" cols="30" placeholder="let us know your requirements!"></textarea>
                        <!-- <input type="text" name=""> -->
                    </div>
                        <input type="submit" class="primary-btn" value="Send Message">
                        <div class="email-drop">or drop us an email at <a href="mailto:contact@asyncdata.io">contact@asyncdata.io</a></div>
                </form>
        </div>
    </div>
    
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
    .overlay{
        position: fixed;
        background: var(--main-black);
        opacity: 0;
        visibility: hidden;
        transition: 1s;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        z-index: 11;
    }
    .overlay-open{
        opacity: 0.4;
        visibility: visible;
    }
    .contact-form{
        width: 60vw;
        position: fixed;
        top: 0;
        bottom: 0;
        right: 0;
        transform: translateX(60vw);
        background: white;
        z-index: 13;
        box-shadow: -5px 0px 10px 0px rgba(0, 0, 0, 0.1);
        transition: 0.7s;
        padding: 5vw 5vw;
    }
    .form-open{
        transform: translateX(0);
        transition: 0.7s;
    }
    .page-header{
        display: flex;
        justify-content: space-between;
        height: 15%;
    }
    .close-btn{
        height: 50%;
        width: auto;
        padding: 10px;
        background: var(--light-stroke);
        color: white;
        border-radius: 4px;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        opacity: 0.4;
        transition: 0.4s;
    }
    .close-btn:hover{
        opacity: 1;
        transition: 0.4s;
    }

    .contact-form form{
        height: 85%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .form-grp{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 15%;
    }
    .form-grp label{
        font-size: 1rem;
        color: var(--mid-grey);
    }
    .form-grp input, .msg-grp textarea{
        background: var(--back-grey);
        border-width: 0;
        height: 80%;
        width: 100%;
        font-size: 1.34rem;
        font-family: 'Aleo', sans-serif;
        border-radius: 4px;
    }
    .form-grp input:focus, .msg-grp textarea:focus{
        outline: none;
        border: solid;
        border-width: 1px;
        border-color: var(--light-stroke);
    }
    ::placeholder{
        color: var(--mid-grey);
        opacity: 0.3;
        font-size: 1rem;
    }
    .msg-grp{
        height: 30%;
    }
    .email-drop{
        color: var(--mid-grey);
        font-size: 1rem;
    }
    .email-drop a{
        color: var(--linkBlue);
    }

    /* RESPONSIVE */
    @media only screen and (max-width: 768px) {
    .contact-form{
        width: 90vw;
        transform: translateX(90vw);
    }
    .form-open{
        transform: translateX(0);
    }
    }
    </style>
