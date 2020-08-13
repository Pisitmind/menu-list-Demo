<template>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <div class="home">
    <div class="img-home-zoom">
        <router-link to="/about">
          <img alt="Stu-logo" class="responsive" src="https://image.freepik.com/free-photo/wooden-board-empty-table-top-blurred-background_1253-1584.jpg"/>
        </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>
<style>
.img-home-zoom img {
  transition: transform 1s, filter 2s ease-in-out;
  border-radius: 2%;
  filter: blur(2px);
  transform: scale(1);
}

.img-home-zoom:hover img {
  filter: blur(0);
  transform: scale(.9);
}

.responsive {
  padding: 0 6px;
  float: center;
  width: 70%;
  height: auto;
}
.text {
  color: rgb(53, 45, 45);
  font-size: 20px;
  position: center;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
}

@media only screen and (max-width: 700px) {
  .responsive {
    width: 80%;
    max-width: 400px;
    margin: 6px 0;
  }
}

@media only screen and (max-width: 500px) {
  .responsive {
    width: 100%;
    max-width: 400px;
  }
}
</style>
