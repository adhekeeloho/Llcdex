<template>
  <div class="about">
    <div >
      <img class= "image" src="../assets/michael-bader-eyq7H7gO0EY-unsplash.jpg" alt="" />
      <h2 class="d-flex justify-content-start"><span>ABOUT US:<br />Who we are? <br/> What we do? </span></h2>
    </div>
  </div>
</template>

<script> </script>

<style scoped>
.image {
   position: relative;
   width: 100%;
   height: 550px;
   }

h2 {
   position: absolute;
   top: 350px;
   left: 0;
   width: 100%;
}

h2 span {
   color: white;
   font: bold 34px/65px Helvetica, Sans-Serif;
   letter-spacing: -1px;
   background: rgb(0, 0, 0); /* fallback color */
   background: rgba(0, 0, 0, 0.7);
   padding: 20px;
}
h2 span.spacer {
   padding:0 5px;
}

@media (max-width: 700px) {
  .image {
   position: relative;
   width: 100%;
   height: 400px;
   }

h2 {
   position: absolute;
   top: 300px;
   left: 0;
   width: 100%;
}

h2 span {
   color: white;
   font: bold 24px/35px Helvetica, Sans-Serif;
   letter-spacing: -1px;
   background: rgb(0, 0, 0); /* fallback color */
   background: rgba(0, 0, 0, 0.7);
   padding: 20px;
}
h2 span.spacer {
   padding:0 5px;
}
}
 </style>
