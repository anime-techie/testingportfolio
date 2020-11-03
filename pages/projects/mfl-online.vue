<template>
  <div>
    <Header/>
    <div class="main_page">
      <div class="section">
          <div class="sec_text_content">
            <div class="section_head">
              <h1 class="section_head_text section_head_megatext">MFL-Online: A Node Based Online Project Platform</h1>
              <h5 class="section_head_subtext">Scarlott Inc. is a startup based in New York that is building a community around micro video reviews on the latest tech and video game related products.
The platform accommodates a simple yet efficient concept of precisely structured mini blogs that inherited the very best features from Youtube, Twitch, Quora and Imgur.
              </h5>
            </div>
          </div>
          <img src="../../assets/img/mfl-online/screenshots.png" alt="Scarlott Project" class="land_img">
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
          <img src="../../assets/img/mfl-online/challenges.png" alt="Scarlott Project" class="land_img">
          <div class="sec_text_content">
            <div class="section_head">
                  <h1 class="section_head_text">Project Challenges</h1>
            </div>
            <ul class="section_head_subtext challenges_list">
                    <li>To minimize and simplify user actions while adding new videos, we had to provide users with convenient tools allowing them to edit videos right on the platform.
                    </li>
                    <li>Large volumes of video content and potentially high user load in the future required a thorough work on the platform architecture and its database structure.
                    </li>
                    <li>As every platform providing high-quality content, we had to find a way to protect users from inappropriate videos.
                    </li>
                    <li>For the marketing reasons we had to make sure that the content will be easy to find on Google and other search engines.
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
                    <li>We have created a custom video editor that generates a thumbnail storyboard for every uploaded video. This way the user can select the 30 seconds he wants to publish right on the platform.
                    </li>
                    <li>Our team decided to use Amazon S3 to store the content and Amazon Cloudfront to guarantee high access speed to the video reviews.
                    </li>
                    <li>Inappropriate videos are detected automatically. We integrated Scarlott with Amazon Rekognition which analyzes all the uploaded videos, blocks suspicious content and sends notifications to the admin.
                    </li>
                    <li>To facilitate content indexing, the platform automatically generates a unique link and SEO attributes for every video.
                    </li>
            </ul>
          </div>
          <img src="../../assets/img/mfl-online/solutions.png" alt="Scarlott Project" class="land_img">
      </div>
      <div class="project_details sec_results">
          <div class="sec_text_content">
              <div class="section_head">
                    <h1 class="section_head_text">Results</h1>
              </div>
            </div>
              <div class="section_head_subtext challenges_list">
                      Watching poorly structured and convoluted video reviews in hope to find the exact product you actually need is a rather daunting experience. Scarlott’s unique framework brings the perfect balance of entertaining yet informative content in a concise form, saving the trouble of going through hours of video reviews. It helps people to make educated consumer choices and connects people with the same interests.

Enkonix team played a key role in the development of Scarlott’s responsive web platform that consists of a web app for video reviewers and an admin panel for the business owner.

Development of the project MVP took us 5 months and covered only the first phase of the product rollout. During MVP development we have focused on the functionality related to vlogging and social networking functionality. The project architecture and database were designed to be highly scalable and ready for functionality expansion, such as integrations with third-party services.
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




