<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="A breif Intro"
      subtitle="These are just facts, to know me better, go through my journey in my blog entries(W.I.P)"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>Schooling</h3>
          <p>
            <strong>
            <ul>
              <li> 10th Standard - Seventh Day Advantist Higher Secondary School </li>
              <li> 12th Standard - Seventh Day Adventist Higher Secondary School </li> 
            </ul>
            </strong>
          </p>
          <h3>Undergraduate College</h3> 
          <p>
            <strong> Indian Institute of Technology, Delhi - Department of Mechanical Engineering</strong>
          </p>
          
          <h3> Work Experience </h3>
            <strong> Reliance Industries Pvt. Ltd. - Jamnagar Branch, Manufacturing Division</strong>

          <h4>My Interests</h4>
          <p>
            I am primarily interested in working in the field of Fluid Dynamics, Computational Mechanics and Multi-scale Fluid Structure interactions.
            I am also interested and have done several projects in the field of Web Development. I am currently working on learning Android App Development.
            I enjoy developing Data-driven sites using Python based Django Framework. I have several web apps deployed on Heroku, exploring differnt aspects of Pyhton libraries, ranging from AI and Ml based Face Detection to State Management for Business WorkFlows and cloud based Business Management Solutions.
            I am also interested in computer architecture and am currently learning the system architecture developments independently.
            For a brief description on my Mechancial projects, you can see my resume or my linkedin profile. For detailed descriptions, I'll soon be posting all the project(both Core Mechanical and Web-Development) journeys on my blog.
            Blogging is something I have started sometime back and will take significant amount of time to update the blogs in all the categories.
          </p>

          <strong> Please go through the <a href="https://rutvik-solanki.ml">portofio</a> to get a brief idea of my projects and my interests</strong>
          <strong>It is always Fun to talk to someone regarding my work or my area of interests. You can contact me through the form, or can mail me directly.</strong>

        </div>


        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                stay tuned...
              </p>
              <p class="subtitle">
                coming soon
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                stay tuned...
              </p>
              <p class="subtitle">
                coming soon
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                stay tuned...
              </p>
              <p class="subtitle">
                coming soon
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>
