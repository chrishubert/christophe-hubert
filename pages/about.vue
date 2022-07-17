<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About Us"
      subtitle="Why are we doing that?"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>The pain points of product manager journey</h3>
          <p>
            There are a few reasons why becoming a product is difficult. First,
            you have to be able to sell yourself. You have to be able to
            convince people that you're worth their money. Second, you have to
            be able to stand out from the competition. There are a lot of
            products out there, and you have to be able to make yours stand out.
            Finally, you have to be able to keep up with the trends. Things are
            always changing, and you have to be able to change with them.
          </p>

          <h3>Helping a fellow Product Manager</h3>

          <p>
            I firmly believe that, as a Product Manager, one of the most
            important things you can do is to help those around you. Whether
            it’s your team, your colleagues, or your customers, your help will
            always be greatly appreciated.
            <br />
            By building a strong community of Product Managers, ready to mentor,
            we will be able to build better products together!
          </p>

          <quote-card
            quote="A product manager is only as good as the team that surrounds them."
            author="Christophe Hubert"
          />
          <h3>Our Projects</h3>
          <p>
            We focus on advanced Routing Optimization for vehicles and for
            warehousing
          </p>
          <p>
            Routing optimization is the process of finding the best route for a
            given network. <strong>It is a complex problem</strong> that
            involves finding the shortest path between two nodes, while also
            taking into account the constraints of the network.
          </p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Routing Optimization
              </p>
              <p class="subtitle">
                Provide the best route for multiple couriers
              </p>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Picking Optimization
              </p>
              <p class="subtitle">
                Most efficient routes in warehouse
              </p>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Courier Mobile Application
              </p>
              <p class="subtitle">
                Track and assign tasks to couriers
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
