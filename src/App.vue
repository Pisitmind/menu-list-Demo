<template>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  <div id="app">
    <div id="nav" class="header">
      <div class="menu">
      <router-link to="/" > <i class="fa fa-fw fa-home"> </i> Homepage  </router-link>
      <router-link to="/about"> <i class="fa fa-fw fa-image"></i>   PhotoList</router-link>
      </div>
    </div>
    <router-view/> <!-- content -->
  </div>
  <div class="footer">
    <p>Contact Us<a href="https://www.facebook.com/pisit.boonklod"> here</a></p>
  </div>
</template>


<style>
#app {
  font-family: "Kanit", "Nunito Sans";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
    /* background:url(https://image.freepik.com/free-photo/beautiful-clouds-blue-sky-background_34251-117.jpg); */
    background:url(http://gdj.graphicdesignjunction.com/wp-content/uploads/2012/08/minimal-background-pattern-wordpress-9.jpg);
    /* background-color:e3e2df; */
    background-size:cover;
    background-repeat: no-repeat;
    /* background-color: #bdc3c7; */
}
#nav {
  padding: 20px;
  color: black;
  font-size:2pw;
  align-items: center;
  align-self: center;
  justify-content: space-around;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
.header {
  overflow: hidden;
  background-color: #f1f1f1;
  padding: 10px 10px;
}

.menu {
  float: left;
  align-items: space-around;
  justify-content: center;
  color: black;
  text-align: center;
  /* padding: 12px; */
  text-decoration: none;
  font-size: 18px;
  line-height: 20px;
  border-radius: 4px; 
  letter-spacing:2px;
  margin: 10px;
}
.i{
  margin: 10px;
}
.footer{
  /* position: fixed; */
  padding: 10px;
  left: 0;
  bottom: 0;
  width: 100%;
  text-align: center;
  font-size: 2pw;
  justify-content: center;
  justify-items: center;
  background: #ddd;
}

</style>
