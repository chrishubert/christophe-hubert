<template>
  <div class="card quote-card">
    <div class="card-content">
      <p class="title">“{{ quote }}”</p>
      <p class="subtitle">
        ~ <span>{{ author }}</span>
      </p>
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
            >Twitter
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
            >Facebook
          </a>
        </span>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  props: {
    quote: { type: String, default: 'Good Quote' },
    author: { type: String, default: 'Unknown' }
  }
}
</script>
