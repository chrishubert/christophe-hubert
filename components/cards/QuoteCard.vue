<template>
  <div class="card quote-card">
    <div class="card-content">
      <span class="title">“{{ quote }}”</span>
      <br />
      <span class="subtitle">
        ~ <span>{{ author }}</span>
      </span>
    </div>
    <footer class="card-footer">
      <div class="card-footer-item">
        <span>
          Share on
          <a
            target="_blank"
            :href="
              'http://twitter.com/share?text=' +
                quote +
                '&url=' +
                $siteConfig.domain +
                $nuxt.$route.path +
                '&via=christophehubert_pm'
            "
          >
            <font-awesome-icon :icon="['fab', 'twitter']" /> Twitter
          </a>
        </span>
      </div>
      <div class="card-footer-item">
        <span>
          Share on
          <a
            target="_blank"
            :href="
              'https://www.facebook.com/sharer/sharer.php?u=' +
                $siteConfig.domain +
                $nuxt.$route.path
            "
          >
            <font-awesome-icon :icon="['fab', 'facebook']" /> Facebook
          </a>
        </span>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  props: {
    quote: {
      type: String,
      default:
        'Service to others is the rent you pay for your room here on Earth.'
    },
    author: { type: String, default: 'Unknown' }
  }
}
</script>
