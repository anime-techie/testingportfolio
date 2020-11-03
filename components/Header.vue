<template>
    <header class="header">
        <script
            src="https://code.jquery.com/jquery-3.5.1.min.js"
            integrity="sha256-9/aliU8dGd2tb6OSsuzixeV4y/faTqgFtohetphbbj0="
            crossorigin="anonymous">
        </script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.5.1/gsap.min.js"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.5.1/ScrollTrigger.min.js"></script>
        <nuxt-link to="/">
                <Logo />
        </nuxt-link>
        <ContactForm />
        <NavMenuMobile />
        <div class="nav-items">
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
        </div>
    </header>
    
</template>

<script>
import ContactForm from '~/components/contact-us';
import NavMenuMobile from '~/components/nav-menu-mobile';
export default {
    components:{
    ContactForm,
    NavMenuMobile
  },
    mounted () {
    this.$nextTick(() => {
            $("body").css({"position": "static", "overflow": "auto"});
            function contact_form_open(){
                                    $('.contact-form').addClass("form-open");
                                    $('.overlay').addClass("overlay-open");
                                    $("body").css({"position": "sticky", "overflow": "hidden"});
            }
            function form_close(){
                                    $('.contact-form').removeClass("form-open");
                                    $('.overlay').removeClass("overlay-open");
                                    $("body").css({"position": "static", "overflow": "auto"});
            }
            $('.nav-items #contact-us, .nav-menu-mobile #contact-us').click(function(){
                                    contact_form_open();
                          });
            $('.flex-sec').click(function(){
                                    contact_form_open();
                          });
            $('#nav-menu-icon').click(function(){
                            $('.overlay').addClass("overlay-open");
                            $('.nav-menu-mobile').addClass("nav-mobile-open");
                            $("body").css({"position": "sticky", "overflow": "hidden"});
            });
            
                        $('.close-btn').click(function(){
                            if($('.nav-menu-mobile').hasClass("nav-mobile-open")){
                                $('.contact-form').removeClass("form-open");
                            }
                            else
                            form_close();
                        });
                        $('.overlay').click(function(){
                            $('.nav-menu-mobile').removeClass("nav-mobile-open");
                            form_close();
                            });

                        // TOGGLE PROJECTS
                        
    })
  }
}
</script>>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Aleo:wght@300;400;700&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Monoton&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Maven+Pro:wght@400;500;600;700;800;900&display=swap');
    :root{
        --main-black: #000;
        --mid-black: #565C5F;
        --mid-grey: #64707D;
        --back-grey: #FAFBFD;
        --light-stroke: #E2E4E5;
        --linkBlue: #2F80ED;
        --lightBlue: #EAEFFF;
        --primary-grad: linear-gradient(270deg, #EB5757 0.21%, #F2994A 100%);
        font-size: 18px;
        font-family: 'Aleo', 'Times New Roman', Times, serif;
    }
    .main_page {
        background: var(--back-grey);
    }
    a{
        text-decoration: none !important;
    }
    .primary-btn{
        padding: 15px 10%;
        background: var(--primary-grad);
        font-size: 0.78rem;
        border-radius: 4px;
        font-weight: 700;
        color: white;
        text-align: center;
        border-width: 0 !important;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .primary-btn:hover{
        cursor: pointer;
    }
    .secondary-btn:hover{
        cursor: pointer;
        transition: 0.3s;
        background: var(--primary-grad);
        background-clip: text;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        border-color: #F2994A;
    }
    .secondary-btn{
        font-size: 0.78rem;
        border: solid;
        padding: 15px 10%;
        background: var(--back-grey);
        border-color: var(--light-stroke);
        border-width: 1px;
        border-radius: 4px;
        -webkit-border-radius: 4px;
        -moz-border-radius: 4px;
        font-weight: 700;
        color: var(--mid-grey);
        text-align: center;
        transition: 0.3s;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .btn-grp{
        display: grid;
        grid-template-columns: 1fr 0.1fr 1fr;
        width: 60%;
    }
   .header{
       position: fixed;
       z-index: 10;
       width :100%;
       height:10vh;
       padding: 0% 5%;
       display:flex;
       justify-content: space-between;
       align-items : center;
       background-color: #fff;
       box-shadow: 0 1px 10px rgba(0,0,0, 0.25);
   }
   .nav-items{
       list-style : none;
       padding: 0;
       margin: 0;
       display :flex;
       justify-content : space-around;
       align-items : center;
       width : 50%;
       font-size: 0.78rem;
   }
   .nav-menu-side li{
       width: fit-content;
   }
   #nav-menu-icon{
       cursor: pointer;
   }
   .nav-items li a, .nav-menu-side li a{
       text-decoration: none;
       font-weight: 400;
       color: var(--mid-black);
       transition: 1s;
       cursor: pointer;
   }
   .nav-items .header_active a, .nav-menu-side .header_active a{
       font-weight: 700;
       color: var(--main-black);
       transition: 1s;
   }
   .nav-items .header_active .bottom-line, .nav-menu-side .header_active .bottom-line{
       transform: scaleX(1);
       transition: 1s;
   }
   .nav-items li .bottom-line, .nav-menu-side li .bottom-line{
       height: 2px;
       width: 100%;
       background: var(--primary-grad);
       transform: scaleX(0);
       transform-origin: 0% 50%;
       transition: 1s;
   }
   .nav-items li:hover .bottom-line{
       transform: scaleX(1);
       transition: 1s;
   }

   .section{
       height: 100vh;
       padding: 5vw 5vw;
       display: flex;
       align-items: center;
       justify-content: space-between;
       flex-wrap: wrap;
   }
   .right-section {
       text-align: right;
    }
   .land_img {
       z-index: 0;
       height: 100%;
       max-width: 45%;
       transform: translateY(10vh);
    }
   
   .small_section{
       height: 60vh !important;
       background: url(../assets/img/page_header.png) !important;
   }
   .white_section{
       background: white;
    }
  .right-section svg {
      width: 40%;
      height: auto;
    }
   .section_head_megatext{  
    font-size: 2.67rem !important;
    }
    .name-title{
    font-family: 'Monoton', cursive;
    font-size: 2.67rem;
    background: var(--primary-grad);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    }
   .sec_text_content{
       max-width: 55%;
       height: 80%;
       display: flex;
       flex-direction: column;
       justify-content: space-evenly;
   }
   .section_head{
       max-width: 700px;
   }
   .section_head_text{
       font-size: 2rem;
       line-height: 122.66%;
       letter-spacing: 0.03em;
       font-weight: 700;
       color: var(--main-black);
   }
   .section_head_subtext{
       font-size: 1rem;
       line-height: 1.5rem;
       letter-spacing: 0.05em;
       font-weight: 400;
       color: var(--mid-black);
       margin-top: 10px;
   }
   .statistics{
       width: 100%;
       display: grid;
       grid-template-columns: 1fr 0.05fr 1fr 0.05fr 1fr 0.05fr 1fr;
       text-align: center;
       justify-content: center;
       align-items: center;
   }
   .stat_num{
       color: var(--mid-grey);
       font-family: 'Maven Pro', sans-serif;
       font-weight: 900;
   }
   .stat_text{
       color: var(--mid-grey);
       font-size: 0.78rem;
       font-weight: 400;
       line-height: 1.5rem;
       letter-spacing: 0.05em;
   }
   .divider{
       width: 3px;
       height: 60%;
       border-radius: 10px;
       background: var(--primary-grad);
   }

/* PROJECTS */
    .project_title{
    color: var(--main-black);
    font-size: 1rem;
    font-weight: 700;
    }
    .project_subtitle{
    color: var(--mid-grey);
    font-size: 0.78rem;
    font-weight: 400;
    line-height: 25px;
    }
    .open_project{
    color: var(--mid-grey);
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 0.67rem;
    font-weight: 400;
    }

    /* PORTFOLIO PAGE */
.portfolio_section{
  padding: 7vw 5vw;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.portfolio_section a{
  width: 46%;
  height: 110vh;
  text-decoration: none;
}

.project_card{
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}
.portfolio_section a:nth-child(2){
  margin-top: 25vh;
}
.portfolio_section a:nth-child(4){
  margin-top: 25vh;
}
.project_shots{
  width: 100%;
  height: auto;
  border-radius: 4px;
  -webkit-border-radius: 4px;
  -moz-border-radius: 4px;
  background: var(--lightBlue);
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 5%;
  max-height: 500px;
  overflow: hidden;
}
.project_card:hover{
  cursor: pointer;
}
.project_card:hover .project_shots img{
  transform: scale(1.05, 1.05);
  transition: 0.7s;
}
.project_shots img{
  width: 100%;
  transition: 0.7s;
}

/* SERVICES SECTION */
.services_section{
  height: 80vh;
  display: flex;
  justify-content: center;
}
.services_card_grp{
  display: flex;
  height: 100%;
  width: fit-content;
  justify-content: space-between;
  flex-wrap: wrap;
}
.service_card{
  width: 50%;
  padding: 5vw 5vw;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  transition: 0.4s;
}
.nav-comp{
    display: none;
}
.other_projects{
    margin: 7vw 5vw;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100vh;
  }
.portfolio_section_small{
    display: flex;
    justify-content: space-between;
    height: 80%;
    width: 100%;
  }
  .portfolio_section_small a{
    width: 32%;
    margin: 0;
    height: 100%;
    text-decoration: none;
  }
  /* ABOUT US PAGE */
  .about_intro{
        width: 100%;
        height: 90%;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
    }
    .detail_info_section{
        height: 120vh;
        padding: 7vw 5vw;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .process_card_grp{
        display:flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    .process_card{
        width: 46%;
        height: 40%;
        display: flex;
        justify-content: space-between;
        overflow: hidden;
    }
    .location_grp{
        height: 100%;
        width: 100%;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        flex-wrap: wrap;
    }
    .location_card{
        height: 100%;
        width: 20%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: flex-start;
    }
    .tech_artwork{
        padding: 5vw 5vw;
        display: flex;
        justify-content: center;
    }
    .tech_artwork svg {
        z-index: 1;
        width: 80vw;
        height: auto;
        transform: translateY(-30vh);
    }
/* RESPONSIVE DESIGN */
@media only screen and (max-width: 768px) {
    :root{
        font-size: 12px;
    }
    .header>:nth-child(4){order:2}
    .header>:nth-child(5){order:1}
    .header>:nth-child(6){order:3}
    .section{
        flex-direction: column;
        flex-flow: column-reverse;
        width: 100%;
        height: 80vh;
        justify-content: space-evenly;
    }
    .section>:nth-child(1){order: 1;}
    .section>:nth-child(2){order: 3;}
    .section>:nth-child(3){order: 2;}
    .small_section{
        height: 40vh !important;
    }
    .nav-items{
        display: none;
    }
    .nav-comp{
        display: initial;
    }
    
    .section>div{
        max-width: 100%;
    }
    .section>svg{
        height: 30%;
        max-width: 100vw;
        transform: translateY(0px);
    }
    .sec_text_content{
        height: 50%;
    }
    .btn-grp{
        width: 100%;
    }
    .right-section{
        flex-flow: column;
    }
    .right-section svg{
        width: 100%;
    }
    .services_section{
        height: 120vh;
    }
    .service_card{
        width: 100%;
    }
    .land_img{
        transform: translateY(0);
    }
    .portfolio_section a, .portfolio_section_small a{
        height: 70vh;
        margin: 0;
    }
    .process_card{
        width: 100%;
        height: 25%;
        margin-top: 20px !important;
    }
    .location_card{
        width: 40%;
        height: 40vh;
    }
    .about_intro{
        justify-content: center;
    }
    
    .tech_artwork>svg{
        transform: translateY(0);
    }
    .other_projects{
        justify-content: space-evenly;
    }
    .project_solutions_sec{
        height: fit-content;
    }
}
</style>