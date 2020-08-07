<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="Who are we?"
      subtitle="Why did we create this web?"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>About Us</h3>
          <p>
            <strong>
              Information needs to be shared. Ignorance is not an excuse
            </strong>
          </p>
          <p>
            We strongly  believe that information needs to be shared. 
            If you have some time and willingness to do some research, you can find the information.
            When you gather enough information, you are informed. 
            When you are informed you get a direction!
          </p>

          <h3>Little bit of History</h3>
          <p>
            Back in 2011, I was trying hard to find a job in Europe. The author's
             background was nursing and had NMBI (Nurisng regulatroy body in Ireland) decision letter.
             However, due to recession there was not enough recruitment. There were many
             agents who pretend to be the saviours offering jobs in Ireland. But there was a catch. They need money!
             Not 'little' money, but huge sum!
          </p>
             
           <p>
            However, I kept on searching. I have contacted employers in the UK, Ireland,
            Australia and Newzealand.  At last, I have got a reply from an employer
            from Ireland.  They wrote to me that they will do an interview in India soon.
            I have attended their interview, got selected,
            rest everything went well. Within 6 months I came to Ireland.
           </p>
          <quote-card />
          <h3>Did I pay anything?</h3>
          <p>
            The recruiter was a nursing home. As it was during the peak of recession, HSE did
            not have any recruitement campaign. So I did pay for my expenses, such as flight
            ticket, and cost of green card (1000 euro). No payment to any agencies. Not a single penny. 
          </p>
          
          <h3>How did I progress through my career?</h3>
          <p>
             I worked in the Nursing home for 2 years and then moved to a teaching hospital.
             I worked as staff nurse in ICU, then became a Clinical Nurse Manager 1 (CNM1) followed by
             CNM2 and CNM3. I currently work as the Quality Manager for Clinical Audit at the same 
             Hospital.
          </p>
          
          <h3>Did I study anything?</h3>
          <p>
            During this period I completed a post graduate Diploma in Cardiovascular nursing, followed by a
            Masters in Cardiovascular Nursing from Trinity College Dublin. 
            I have completed several short term courses such as foundation course in ICU, chronic illness
            foundation course, leadership and management etc. Currently I am doing Masters in Healthcare Leadership
            at Irish Management Insititue. 
            I have also secured a seat for MBA at UCD Michael Smurfit Business school for the class of 2021.
          </p>
          <h3>Why did I start Vacancypool?</h3>
           
          <p>
            I started Vacancypool website to  give information to people who are
            looking for a career in Europe or elsewhere. I wanted to share my experinces
            and learning to all of you.
            I will be contented if anyone find it useful. 
    
          </p>
           
           <h2>What else I do?</h2>
           <p>
           <UL>
              <LI>I do write some blogs here and there.
              <LI>I run a malayalam news paper for Irish Malayalees named Irishvartha.
              <LI>
              <LI> I do occasional vlogs
              <LI>I support my 4 year old girl with her youtube channel Irishkid
              <LI>I play Piano and guitar if I get any spare time! I play guitar for the Choir Zamar
              </UL>
           </p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Cool stuff I do
              </p>
              <p class="subtitle">
                Blogging & Vogging 
              </p>
              <figure class="image is-1by1">
              
                <opti-image
                  :src="require('~/assets/uploads/contact-person.jpg').src"
                  :srcset="
                    require('~/assets/uploads/contact-person.jpg').srcSet
                  "
                   />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Learning
              </p>
              <p class="subtitle">
                Coding & astropysics 
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Creativity
              </p>
              <p class="subtitle">
                Music creation & Irishvartha
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
