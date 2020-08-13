<template>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <div class="about">
    <h1 class="linear-wipe">Photos-List</h1>
    <div class="card-ori">
      <div class="cards">
        <item
          v-for="(item, index) in photos"
          :key="index"
          :image="item.image_url[0]"
          :name="item.name"
          :like="item.votes_count"
          :discription="item.description"
          :ownername="item.user.username"
          :ownerimg="item.user.userpic_https_url"
        ></item>
      </div>
    </div>
  </div>
</template>
<script>
import item from "../components/item";
import data from "../components/data";

export default {
  components: {
    item,
  },
  created() {
    console.log(data);
  },
  computed: {
    photos() {
      return data.photos;
    },
  },
};
</script>
<style>
.card-ori {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: space-around;
  align-content: space-between;
}
.cards {
  display: flex;
  flex-direction: row;
  flex-flow: wrap;
  justify-content: space-around;
  margin: 10px auto;
  color: rgb(0, 0, 0);
}

.about {
  /* color:rgb(50, 163, 255); */
  font-family: sans-serif;
  font-size: 3vw;
}
/* @media screen and (max-width: 1024px ){
  /* .card-ori{
    display: flex;
    flex-direction: column;
  } */
/* .card-ori {
    display: flex;
    flex-direction: column; */
/* } */
@media only screen and (max-width: 375px) {
  .card-ori {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: center;
    align-content: stretch;
    width: 100%;
  }
  .cards {
    display: flex;
    flex-direction: column;
    flex-flow: wrap;
    justify-content: space-around;
    color: rgb(0, 0, 0);
    width: 90%;
    margin: 5px;
    width: 90%;
  }
}
@media only screen and (max-width: 760px) {
  /* body {
    background-color: rgb(224, 230, 173);
  } */
  .cards {
    display: flex;
    flex-direction: column;
    flex-flow: wrap;
    justify-content: space-around;
    margin: 10px;
    color: rgb(0, 0, 0);
  }

  .cards {
    display: flex;
    flex-direction: column;
    flex-flow: wrap;
    justify-content: center;
    margin: 5px;
    width: 50%;
  }
}
.linear-wipe{
font-family: Helvetica Neue, Helvetica,  sans-serif;
	font-size: 5vw;
	font-weight:  100;
	letter-spacing: 2px;
	text-align: center;
	color: #26f3af;
	background-image: -webkit-linear-gradient(92deg, #f35626, #feab3a);
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
	-webkit-animation: hue 10s infinite linear;
}

@-webkit-keyframes hue {
  from {
    -webkit-filter: hue-rotate(0deg);
  }
  to {
    -webkit-filter: hue-rotate(-360deg);
  }
}

</style>
