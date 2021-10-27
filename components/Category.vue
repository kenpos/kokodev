<template>
  <header>
    <v-card color="basil">
      <v-card-title class="text-center justify-center py-6">
        Category

        <v-btn block elevation="2" small value="scrap" to="/Scrap">
          <span>scrap</span>
          <v-icon>mdi-run</v-icon>
        </v-btn>

        <v-btn block elevation="2" small value="Programming" to="/Programming">
          <span>Programming</span>
          <v-icon>mdi-responsive</v-icon>
        </v-btn>

        <v-btn block elevation="2" small value="Read" to="/Read">
          <span>Read</span>
          <v-icon>mdi-book-open-page-variant</v-icon>
        </v-btn>
      </v-card-title>
    </v-card>
  </header>
</template>
