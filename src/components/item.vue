<template>
    <div class="card1" >
        <div class="row">
            <img class="owner-img" :src="ownerimg">
            <p class="owner-name">  {{ownername}}</p>
        </div>
        <!-- <div class="img-zoom"> -->
        <!-- <img id="image" class="fade" :src="image"> -->
        <img id="image"  :src="image">
        <!-- </div> -->
        <div class="container">
            <div class="like-bar" >
                    <img class="like-icon" src="https://purepng.com/public/uploads/large/heart-icon-y1k.png" >
                    <p class="vote-score"> {{like}} love </p>
                <!-- <p class="p-location"> location :</p> -->
            </div>
                    <hr>
            <p class="p-name">name: {{name}}</p>
            <p class="p-disc "> caption : {{discription}}</p>
        </div>
    </div>
</template> 
<script>

export default {
    props: {
        image: String,
        name: String,
        like: Number,
        discription : String,
        ownername : String,
        ownerimg : String
    }
}
</script>
<style scope>
.row {
    display: flex;
      padding-left: 16px;
      padding-top:  2px;
      align-items: center;
}
.like-bar {
    display: flex;
        padding-left: 16px;
        align-items: center;
        font-weight: bold;
        /* justify-content: stretch; */
        
}
.like-icon {
    width: 7%;
    height:7%;
    /* max-width: 20px;
    max-height: 20px; */
    align-items: center;
    justify-content: left;
}
.vote-score {
    padding: 5px;
}
#image {
    /* border-radius: 100%; */
    width: 90%;
    height: 60%;
}
.owner-img {
    /* width: 1.7rem;
    max-width: 100%;
    height: 1.7rem; */
    width: 7%;
    height:7%;
    border-radius: 50%;
    border-style: solid;
    border-color: rgba(238, 106, 255, 0.8);
    position: center;
  
}
.owner-name{
    text-align: left;
    padding-left: 8px;
    font-family: "Lucida Console", Courier, monospace;
    /* font-style: italic; */
    font-weight: bold;
    font-size: 1.2vw;
    align-content: center;
    color: rgb(8, 2, 36);
}
.vote-score{
    color:rgb(99, 94, 94);
    font-size: 1.2vw;
}
.p-name{
    text-align: left;
    font-weight: bold;
    font-size: 1.3pw;
}
.p-disc{
    text-align: left;
    font-weight: lighter;
    font-size: 1pw;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    font-weight: lighter;
    color:rgb(78, 73, 73);
}
.card1{
    border-radius: 2%;
    /* background-color: rgba(183, 213, 240,0.5); */
    /* background-color: rgba(255, 230, 205,0.5); */
    background-color: rgba(253, 207, 118,0.2);
    color:black;
    font-size:1vw;
    outline: 1;
    width: 600px;
    margin:10px;

    /* height: 450px ; */
}
.card1:hover {
    box-shadow: 0 6px 10px 0 rgba(0,0,0,0.5);
    transition: 0.2 s;
}
.container {
  padding: 10px;
  font-size:1.2vw;
}
.fade {
   opacity: 1;
   transition: opacity .25s ease-in-out;
   -moz-transition: opacity .25s ease-in-out;
   -webkit-transition: opacity .25s ease-in-out;
   }

    .fade:hover {
      opacity: 0.5;
      }

.img-zoom img {
  transition: transform .2s, filter 0.5s ease-in-out;
  /* filter: grayscale(100%); */
}

.img-zoom:hover img {
  /* filter: grayscale(0); */
  transform: scale(1.2);
}
/* @media only screen and (max-width: 360px) {

  body {
    background-color: lightblue;
  }
  .card1{
      padding: 5px;
  }
} */

</style>