<template>
  <v-app dark>
    <v-main>
      <v-container>
        <Header />
        <Breadcrumbs />
        <Nuxt />
      </v-container>
     </v-main>
    
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

