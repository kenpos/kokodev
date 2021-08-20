<template>
  <header>
      <div class="title">心のデブを信じろ</div>
      <nav>
          <nuxt-link to="/">Home</nuxt-link>
          <nuxt-link to="/about">About</nuxt-link>
      </nav>
  </header>
</template>


<style>
header {
	padding: 15px 30px;
	background-color: white;
	display: flex;
	justify-content: space-between;
	align-items: center;
	box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.1);
}
header .title {
	color: black;
	font-size: 24px;
	font-weight: 900;
	text-transform: uppercase;
}
nav {
	display: flex;
	align-items: center;
	margin: 0 -15px;
}
nav a {
	display: block;
	margin: 0 15px;
	color: cornflowerblue;
}
</style>