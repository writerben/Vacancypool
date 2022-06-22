<template>
  <div id="home-page" class="page-wrapper home-page">
    <site-hero :title="title" :subtitle="subtitle" :image="featureImage">
      <button
        v-if="$siteConfig.newsletter.on"
        class="button is-primary"
        @click="$eventBus.$emit('modal-triggered', 'newsletter-modal')"
      >
        Subscribe To Newsletter
      </button>
    </site-hero>
    <main-section theme="one-column">
    
    
    
    <div class="w-full mb-20">
      <div class="text-center" v-if="!jobs.length">
        <logo class="mx-auto pr-12" />
        <p class="status-text">Loading...</p>
      </div>
      <p v-else-if="$fetchState.error" class="status-text">
        Kindly refresh to see the latest jobs
      </p>
      <div v-else>
        <job-card-list class="mb-20" :jobs="jobs" />
        <div class="mb-28 text-center">
          <nuxt-link
            style="border: 1.5px solid #1f9e98; color: #1f9e98"
            class="rounded-lg px-9 py-6 inline-block"
            to="/jobs"
          >
            <div class="flex">
              <p class="mr-2 font-medium">Explore more jobs</p>
              <img src="~/assets/images/right_icon.svg" alt="proceed" />
            </div>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
    
    
    
    
      <template v-slot:default>
        <!-- All Posts -->
        <posts-grid />
      </template>
      
      <template v-slot:sidebar>
        Nothing here
      </template>
    </main-section>
    <news-letter-form-modal />
  </div>
</template>

<script>
import { mapState } from 'vuex'
import { setPageData } from '../helper'
import NewsLetterFormModal from '~/components/NewsLetterFormModal'

export default {
  name: 'HomePage',
  head() {
    return {
      title: `Home | ${this.$siteConfig.siteName}`
    }
  },
  components: {
    NewsLetterFormModal
  },
  computed: {
    ...mapState(['title', 'subtitle', 'featureImage'])
  },
  fetch({ store, params }) {
    setPageData(store, { slug: 'home' })
  }
}
</script>

<style>
.home-page .under-subtitle {
  border-top: none;
}
</style>
