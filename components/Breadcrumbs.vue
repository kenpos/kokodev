<template>
    <div>
    <li property="itemListElement" typeof="ListItem">
      <nuxt-link property="item" typeof="WebPage" to="/">
          <v-icon to="/" small>mdi-home</v-icon>
      </nuxt-link>
      <meta property="position" content="1" />
    </li>
    <li
      v-for="(crumb, index) in crumbs"
      :key="index"
      property="itemListElement"
      typeof="ListItem"
    >
      <nuxt-link property="item" typeof="WebPage" :to="crumb.path">
        <span property="name">{{
          $route.fullPath === crumb.path && breadcrumb !== null ? breadcrumb : crumb.breadcrumb
        }}</span>
      </nuxt-link>
      <meta property="position" :content="index + 2" />
    </li>
    </div>
</template>

<script>
export default {
  props: {
    breadcrumb: {
      type: String,
      default: null,
    },
  },
  computed: {
    crumbs() {
      const fullPath = this.$route.fullPath
      const params = fullPath.startsWith('/')
        ? fullPath.substring(1).split('/')
        : fullPath.split('/')
      const crumbs = []
      let path = ''
      
      params.forEach((param, index) => {
        path = `${path}/${param}`
        const match = this.$router.match(path)
        if (match.name !== null) {
          crumbs.push({
            breadcrumb: param.replace('/-/g', ' '),
            ...match,
          })
        }
      })
      return crumbs
    },
  },
}
</script>

<style scoped>
li {
  display: inline;
}
li:after {
  content: ' » ';
  display: inline;
  font-size: 0.9em;
  color: #aaa;
  padding: 0 0.0725em 0 0.15em;
}
li:last-child:after {
  content: '';
}
</style>