<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="A bit of my hostory and my Future goals"
      subtitle="These are just facts, to know me better, go through my journey in my blog entries"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>Schooling</h3>
          <p>
            <strong>
              I completed my schooling from Seventh-Day-Adventist Higher Secondary School, starting from a failure in std. 3, ending as a School Topper when  I completed in highschool
            </strong>
          </p>
          <p>
            Heyy, I'm not a nerd if you think so after the last satement. I was an overall achiever, proof, I was the champion in the inter-zonal Swimming Competition, with maximum number of 
            Gold medals(Gold in all the competitions). Though, I was an excellent swimmer, but am even more of a physicist. I was a state topper(top 1%) and selected for national campaigns 
            held by International Association of Physics Teacher.
          </p>

        <p>
          Physics was love, but maths was her father. So, as usual, I had a good bonding with mathematics and as a result developed excellent mathematical solving aptitude.
          I was always promoted to think critically before acting by my parents.<strong>I am and will always remain indebted to my parents for the rich upbringing provided by them.</strong>
          This skill helped me sove several daily problems creatively, and of course, I was easily scoring good at the school exams(always was good with memory ;).
          Not bragging, but I literally ranked 2600 from 1.2 million students. I got admitted to the Best Mechanical Engineering College in India. 
        </p>

          <h3>College - Part 1 - Undergraduate</h3>
          <p>
            Mechanical Engineering was an obvious choice, given my love for application-based physics. I had a break-up as the courses started becoming all theory and bored me to death.
            But then, in the third semester, the courses again became application based. I started enjoying them and then, I finally went on my first date with the subject - my first research Project.
            that was an out of the world experience. So, I'll be proposing soon. 
          </p>
          <quote-card />
          <h3>College - Part 2 - Postgraduate</h3>
          <p>
            <strong>Work-In-Progress</strong>
          </p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                My Hobbies/Interests/Fetishes/Desires/.....
              </p>
              <p class="subtitle">
                Sooo Cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Other Cool Things
              </p>
              <p class="subtitle">
                Just as cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                All the cool
              </p>
              <p class="subtitle">
                that is all
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
