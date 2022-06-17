<template>
  <div id="contact-page" class="page-wrapper contact-page content-page">
    <site-hero
      title="Contact Us"
      subtitle="Please direct your questions/applications below"
      image="/uploads/contact-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Get in Touch
              </p>
              <p class="subtitle">
                We are here to help you!.
              </p>
              <figure class="image is-1by1 ">
                <opti-image
                  :src="require('~/assets/uploads/contact-person.jpg').src"
                  :srcset="
                    require('~/assets/uploads/contact-person.jpg').srcSet
                  "
                />
              </figure>
              <br />
              <div class="content">
                <p>
                  <strong>
                    Job Applications/General Query
                  </strong>
                </p>
                <p>
                  If you are looking for a job in Ireland or UK, or have any
                  general queries, please use the form to submit your query.
                  Alternatevely you can email your
                  <li>General queries to info@vacancypool.com </li>
                  <li> Job applications to jobs@vacancypool.com </li>
                </p>
              </div>
            </article>
          </div>
          <div class="tile is-parent is-8">
            <article class="tile is-child box">
            
              <p>
                <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfCfQW35T1uliMOroXXdbAKg02dGgUdUx4YMMt9TD8kKWVZKw/viewform?embedded=true"
                width="640" height="1181" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
              </p>
            </article>
          </div>
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import ContactForm from '~/components/ContactForm'
export default {
  head() {
    return {
      title: `Contact | ${this.$siteConfig.siteName}`
    }
  },
  components: { ContactForm }
}
</script>
