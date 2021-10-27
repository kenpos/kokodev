<template>
  <v-app dark>
    <v-main>
      <v-container>
        <Header />
        <Breadcrumbs />
        <v-row :align="align" no-gutters style="height: 150px;">
          <v-col cols="12" sm="6" md="9">
            <v-card class="pa-2" outlined tile>
              <Nuxt />
            </v-card>
          </v-col>

          <v-col cols="6" md="3">
            <Category />
          </v-col>
        </v-row>
      </v-container>
      <Foter />
    </v-main>
  </v-app>
</template>
