<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="Connect?"
      subtitle="Follow for important updates?"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>Connect with us</h3>
          <p>
            Due to the busy schedule I am not always available to individually respond to emails.
            However, you can follow me on major social media channels.
            </P>
          
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
               Linkedin
              </p>
              
              <figure class="image is-1by1">
              <a href="https://ie.linkedin.com/in/jinishrajan/">
              
                <opti-image
                  :src="require('~/assets/uploads/li.png').src"
                  :srcset="
                    require('~/assets/uploads/li.png').srcSet
                  "
                   />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Twitter
              </p>
             
              <figure class="image is-1by1">
                <a href="https://twitter.com/connectjinish/">
              
                <opti-image
                  :src="require('~/assets/uploads/tw.png').src"
                  :srcset="
                    require('~/assets/uploads/tw.png').srcSet
                  "
                   />
              </figure>
            </article>
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
