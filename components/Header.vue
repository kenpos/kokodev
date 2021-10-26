<template>
  <header>
    <v-card color="basil">
      <v-card-title class="text-center justify-center py-6">
        <h1 class="font-weight-bold text-h2 basil--text">
          心のデブを信じろ
        </h1>
      </v-card-title>
      <v-bottom-navigation v-model="value">
        <v-btn value="home" to="/">
          <span>Home</span>
          <v-icon>mdi-home</v-icon>
        </v-btn>

        <v-btn value="profile" to="/profile">
          <span>Profile</span>
          <v-icon>mdi-account</v-icon>
        </v-btn>
      </v-bottom-navigation>

    </v-card>
  </header>
</template>