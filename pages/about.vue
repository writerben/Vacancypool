<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About Us"
      subtitle="History of Vacancypool"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>About Us</h3>
       
          <p>
            At Vacancypool, we empower all our candidates to find their job to
          build their future careers in UK and Ireland. We have a dedicated
          team to assist the candidates starting from their initial interview 
        through their arrival at the new job. All our team members have a 
        healthcare background and have the expertise to advise you to 
        pursue your dream career. We offer solid support, in-depth 
        knowledge, and a personal touch.

          </p>

          <h3>Little bit of History</h3>
          
           <h2>What do we Offer?</h2>
           <p>
           <UL>
              <LI>Find perfect candidates to empolyers and perfect employers to candidates.
              <LI>Initial interview and shortlisting
              <LI> Assistance with NMBI application,  VISA application, Pick up from the Airport, Initial accomodation and food.
              </UL>
           </p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Submit Your CV 
              </p>
       
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Featured Jobs
              </p>
              <p class="subtitle">
                Featured Jobs
              </p>
              
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
               Read our blogs
              </p>
              <p class="subtitle">
                Read our Blogs
              </p>
              
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

<script>
export default {
  head: {
    title: 'About- Vacancypool',
    meta: [
      { hid: 'Vacancypool', name: 'About', content: 'Story of Vacancypool' }
    ],
  }
}
</script>
