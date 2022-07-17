<template>
  <footer class="site-footer">
    {{ $siteConfig.siteName }} &copy; {{ new Date().getFullYear() }} - All
    Rights Reserved
    <br />
    You can reach us on
    <a href="https://twitter.com/chrishubert_pm">
      <font-awesome-icon :icon="['fab', 'twitter']" />
    </a>
    ,
    <a href="https://www.linkedin.com/in/hubertchristophe/">
      <font-awesome-icon :icon="['fab', 'linkedin']" />
    </a>
    , and
    <a href="https://www.youtube.com/channel/UCIR5Vxs1dnMFvRp1pcdsUPw">
      <font-awesome-icon :icon="['fab', 'youtube']" />
    </a>
    <br />
    Made with <span style="color: #e25555;">&#9829;</span> with Nuxt.js and
    Netlify
  </footer>
</template>

<script>
export default {
  name: 'SiteFooter'
}
</script>

<style scoped>
footer {
  background: #eee;
  padding: 20px 10px;
  text-align: center;
  transition: 0.5s ease all;
}
</style>
