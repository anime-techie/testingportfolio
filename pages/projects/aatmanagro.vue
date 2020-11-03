<template>
  <div>
    <Header/>
    <div class="main_page">
      <div class="section">
          <div class="sec_text_content">
            <div class="section_head">
              <h1 class="section_head_text section_head_megatext">Aatmanagro: E-Commerce for Vedic Agriproducts</h1>
              <h5 class="section_head_subtext">Aatmanagro is an ecommerce startup that focuses on organic dietary foods starting with different varities of honey and ghee.
The goal of aatmanagro is to provide access to each of its customer to seamless buying experience.</h5>
            </div>
          </div>
          <img src="../../assets/img/aatmanagro/screenshots.png" alt="Scarlott Project" class="land_img">
          <div class="project_details">
            <div class="details_grp">
              <div class="grp_label">PLATFORM</div>
              <div class="grp_answer">Web</div>
            </div>
            <div class="details_grp">
              <div class="grp_label">TECHNOLOGIES</div>
              <div class="grp_answer">Python, Django, Vue.js, PostgreSQL</div>
            </div>
            <div class="details_grp">
              <div class="grp_label">PROJECT DURATION</div>
              <div class="grp_answer">5 Months</div>
            </div>
          </div>
      </div>
      <div class="section right-section">
          <img src="../../assets/img/aatmanagro/challenges.png" alt="Scarlott Project" class="land_img">
          <div class="sec_text_content">
            <div class="section_head">
                  <h1 class="section_head_text">Project Challenges</h1>
            </div>
            <ul class="section_head_subtext challenges_list">
                    <li>The client was looking to create his ecommerce on wordpress as it offers comphrehnsive cms and seo functionalities.
                    </li>
                    <li>Asyncdata.io needed to create a website that would be comprehensive and able to accumulate a lot of data. Yet easy to navigate through for all the users.
                    </li>
                    <li>Website should have an attractive yet simple elegant design and UX. This meant we had to develop pages from scratch.
                    <li>Client also required a custom admin panel to show customer statistics in graph format.
                    </li>
                  </ul>
          </div>
      </div>
      <div class="section project_solutions_sec">
          <div class="sec_text_content">
            <div class="section_head">
                  <h1 class="section_head_text">Solutions</h1>
            </div>
            <ul class="section_head_subtext challenges_list">
                    <li>ASyncdata created a prototype of UI/UX of figma .
                    </li>
                    <li>Client after approving the prototype the development was started.
                    </li>
                    <li>Couple of days within project and knowing clients new demand we found there is not a specific plugin to address his demand, this prompted us to do some custom development.
                    </li>
                    <li>Api's where integarted of client's social media handles.
                    </li>
                    <li>Custom admin panel was required to show pie and hologram charts after fetching data from database which we successfully implemented with 3D.js
                    </li>
                    <li>Shiprocket APi was integrated to solve client's shipping needs.</li>
            </ul>
          </div>
          <img src="../../assets/img/aatmanagro/solutions.png" alt="Scarlott Project" class="land_img">
      </div>
      <div class="project_details sec_results">
          <div class="sec_text_content">
              <div class="section_head">
                    <h1 class="section_head_text">Results</h1>
              </div>
            </div>
              <div class="section_head_subtext challenges_list">
                     Client on seeing the end product and our commitment to our deadlines and professional and feedback ethos become a client for further development.
 Seemless buying experience was achieved on the project.
              </div>
      </div>
      <otherprojects />
      <letusknow/>
    </div>
    <Footer/>
  </div>
</template>

<script>
import Header from '~/components/Header';
import Footer from '~/components/Footer';
import letusknow from '~/components/let-us-know-sec';
import otherprojects from '~/components/other-projects';
export default {
  components:{
    Header,
    Footer,
    letusknow,
    otherprojects
  },
  mounted () {
    this.$nextTick(() => {

                          this.$gsap.from('.sec_text_content div', {duration: 1, ease: "power2.out", y:-20, opacity: 0.0, delay: 0.5});
    })
  }
}
</script>

<style scoped>
  .project_details{
    width: 80%;
    border-radius: 5px;
    background:var(--lightBlue);
    display: flex;
    padding: 5%;
    align-items: center;
    justify-content: space-evenly;
    margin: 0% 10%; 
  }
  .details_grp{
    display:flex;
    flex-direction: column;
    justify-content: space-evenly;
    margin: 0 5px;
  }
  .grp_label{
    color: var(--linkBlue);
    font-weight: 700;
  }
  .grp_answer{
    color: var(--mid-black);
    margin-top: 5px;
  }

  .challenges_list{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 70%;
  }
  .sec_results{
    flex-direction: column;
    align-items: flex-start;
  }
</style>




