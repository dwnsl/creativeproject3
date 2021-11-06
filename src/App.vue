<template>
<div id="app">
  <div class="header">
    <h1>Air Jordan Shoe History</h1>
  </div>
  <div class="content">
    <router-view />
  </div>
  <div class="footer">
    <a href="https://github.com/dwnsl/creativeproject3">My Git Hub</a>
  </div>
</div>
</template>

<style>
html {}

body {
  margin: 50px 100px;
  font-family: 'Bellota Text', cursive;
}

#app {}



.content {
  min-height: 500px;
}

.footer {
  padding: 30px;
  background-color: #eee;
}
</style>
