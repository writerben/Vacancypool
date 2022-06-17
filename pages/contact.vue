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
        
        
        <form name="contact" method="POST" data-netlify="true">
  <p>
    <label>Your Name: <input type="text" name="name" /></label>
  </p>
  <p>
    <label>Your Email: <input type="email" name="email" /></label>
  </p>
  <p>
    <label>Your Role: <select name="role[]" multiple>
      <option value="Nurse">Nurse</option>
      <option value="Doctor">Doctor</option>
      <option value="Health Care Assistan">Health Care Assistant</option>
      <option value="Other">Other Healthcare</option>
    </select></label>
  </p>
  <p>
    <label>Message: <textarea name="message"></textarea></label>
  </p>
  
  <p>
    <label>
      <span>Add file:</span>
      <input name="file" type="file"/>
    </label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>

            
          
    
          
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
