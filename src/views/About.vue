<template>
  <div class="about">
    <div >
      <img class= "image" src="../assets/michael-bader-eyq7H7gO0EY-unsplash.jpg" alt="" />
      <h3 class="d-flex justify-content-start"><span style="font-family:'Poppins', sans-serif;">ABOUT US:<br />Who we are? <br/> What we do? </span></h3>
    </div>

<div class="bg"></div>
<div class="bg bg2"></div>
<div class="bg bg3"></div>
<div class="content">
  <h1 style="font-family: 'Poppins', sans-serif; ">Who We Are?</h1>
  <span style="font-family: 'Poppins', sans-serif; "> We are a diverse co-operation with interest in oil and gas. We have extensive experience with various fossil fuels power stations. Our specialty is upgrading outdated controls in auxiliary systems.
  </span>
</div>

<div class="content">
  <h1 style="font-family: 'Poppins', sans-serif; ">What We Do?</h1>
  <span style="font-family: 'Poppins', sans-serif; "> With this experience, we can offer the highest quality control system programming while delivering faster working results than other outside or in-house developers.
  </span>
</div>

    <div class="footer-basic">
      <div class="page-content page-container" id="page-content">
      <div class="padding">
        <div class="row container d-flex justify-content-center">
            <div class="col-sm-6">
                <div class="divider divider-rounded divider-center"><img
                class="rounded-circle"
                style="width: 40px; height: 42px; border-radius: 50%;"
                src="../assets/location2.png"
            /></div>
                <p style="font-family: 'Poppins', sans-serif">For what reason would it be advisable for me to think about business content? That might be little bit risky to have crew member like them.</p>
            </div>
        </div>
      </div>
    </div>
        <footer>
             <div class="social-icons">
          <a href="#"
            ><li> <span class="dot"><i class="fa fa-instagram"><b-icon-instagram></b-icon-instagram></i></span> </li></a>
          <a href="#"
            ><li> <span class="dot"><i class="fa fa-twitter"><b-icon-twitter></b-icon-twitter></i></span> </li></a>
          <a href="#"
            ><li> <span class="dot"><i class="fa fa-facebook"><b-icon-facebook></b-icon-facebook></i></span> </li></a>
          <a href="#"
            ><li> <span class="dot"><i class="fa fa-linkedin"><b-icon-linkedin></b-icon-linkedin></i></span> </li></a>
        </div>
            <ul>
         <li class="list-inline-item" style="color: #004c4c; font-family: 'Poppins', sans-serif">Design</li>
          <li class="list-inline-item" style="color: #004c4c; font-family: 'Poppins', sans-serif">Create</li>
          <li class="list-inline-item" style="color: #004c4c; font-family: 'Poppins', sans-serif">Survey</li>
          <li class="list-inline-item" style="color: #004c4c; font-family: 'Poppins', sans-serif">Project</li>
          <li class="list-inline-item" style="color: #004c4c; font-family: 'Poppins', sans-serif">Build</li>
        </ul>
        <p class="copyright" style="color: #004c4c; font-family: 'Poppins', sans-serif">Llcdex Services Limited © 2022</p>
        </footer>
    </div>
  </div>
</template>

<script> </script>

<style scoped>
 .footer-basic {
  padding:40px 0;
  background-color:#ffffff;
  color:#4b4c4d;
}

.footer-basic ul {
  padding:0;
  list-style:none;
  text-align:center;
  font-size:18px;
  line-height:1.6;
  margin-bottom:0;
}

.footer-basic li {
  padding:0 10px;
}

.footer-basic ul a {
  color:inherit;
  text-decoration:none;
  opacity:0.8;
}

.footer-basic ul a:hover {
  opacity:1;
}

.footer-basic .social {
  text-align:center;
  padding-bottom:25px;
}

.footer-basic .social > a {
  font-size:24px;
  display:inline-block;
  text-align:center;
  margin:0 8px;
  color:inherit;
  opacity:0.75;
}

.footer-basic .social > a:hover {
  opacity:0.9;
}

.footer-basic .copyright {
  margin-top:15px;
  text-align:center;
  font-size:13px;
  color:#aaa;
  margin-bottom:0;
}

.divider.divider-rounded {
     color: #004c4c
 }

 .divider.divider-center {
     text-align: center
 }

 .divider {
     position: relative;
     overflow: hidden;
     margin: 35px 0;
     color: #004c4c;
     width: 100%
 }

 .divider.divider-center:before {
     left: -50% !important;
     right: 0;
     margin-left: -20px
 }

 .divider.divider-center.divider-short:before,
 .divider.divider-center:before,
 .divider:after {
     content: '';
     position: absolute;
     width: 100%;
     top: 8px;
     left: 30px;
     height: 0;
     border-top: 1px solid #004c4c
 }

 .divider.divider-rounded i {
     width: 40px;
     height: 40px;
     line-height: 40px;
     background-color: #f5f5f5;
     border-radius: 50%
 }

 .divider i {
     position: relative;
     width: 18px;
     height: 18px;
     line-height: 1;
     font-size: 18px !important;
     text-align: center
 }

 .divider.divider-border.divider-center:before,
 .divider.divider-border.divider-short:before,
 .divider.divider-border:after,
 .divider.divider-rounded.divider-center:before,
 .divider.divider-rounded.divider-short:before,
 .divider.divider-rounded:after {
     top: 19px;
     left: 40px
 }

 .divider.divider-center:after {
     left: 50% !important;
     right: 0;
     margin-left: 20px;
 }

 @media (max-width:991.98px) {
     .padding {
         padding: 1.5rem
     }
 }

 @media (max-width:767.98px) {
     .padding {
         padding: 1rem
     }
 }

 .padding {
     padding-left: 15rem;
     padding-top: 6rem;
     padding-bottom: 6rem;
 }

.bg {
  animation:slide 3s ease-in-out infinite alternate;
  background-image: linear-gradient(-60deg, #1ea1a1 50%, #004c4c 50%);
  bottom:0;
  left:-50%;
  opacity:.5;
  position:fixed;
  right:-50%;
  top:0;
  z-index:-1;
}

.bg2 {
  animation-direction:alternate-reverse;
  animation-duration:4s;
}

.bg3 {
  animation-duration:5s;
}

.content {
  background-color:rgba(255,255,255,.8);
  border-radius:.25em;
  box-shadow:0 0 .25em rgba(0,0,0,.25);
  box-sizing:border-box;
  left:50%;
  padding:10vmin;
  text-align:center;
  top:70%;
  transform:translate(-50%, -50%);
  margin-top: 200px;
  margin-left: 0px;
  position: relative;
}

h1 {
  font-family:monospace;
}

@keyframes slide {
  0% {
    transform:translateX(-25%);
  }
  100% {
    transform:translateX(25%);
  }
}

.image {
   position: relative;
   width: 100%;
   height: 550px;
   }

h3 {
   position: absolute;
   top: 350px;
   left: 0;
   width: 100%;
}

h3 span {
   color: white;
   font: bold 34px/65px Helvetica, Sans-Serif;
   letter-spacing: -1px;
   background: rgb(0, 0, 0); /* fallback color */
   background: rgba(0, 0, 0, 0.7);
   padding: 20px;
}
h3 span.spacer {
   padding:0 5px;
}

@media (max-width: 700px) {
  .image {
   position: relative;
   width: 100%;
   height: 400px;
   }
.content {
  background-color:rgba(255,255,255,.8);
  border-radius:.25em;
  box-shadow:0 0 .25em rgba(0,0,0,.25);
  box-sizing:border-box;
  left:50%;
  padding:10vmin;
  text-align:center;
  top:70%;
  transform:translate(-50%, -50%);
  margin-top: 200px;
  margin-left: 0px;
  position: relative;
}
.padding {
     padding-left: 6rem;
     padding-top: 6rem;
 }
h3 {
   position: absolute;
   top: 300px;
   left: 0;
   width: 100%;
}

h3 span {
   color: white;
   font: bold 24px/35px Helvetica, Sans-Serif;
   letter-spacing: -1px;
   background: rgb(0, 0, 0); /* fallback color */
   background: rgba(0, 0, 0, 0.7);
   padding: 20px;
}
h3 span.spacer {
   padding:0 5px;
}
}
.dot {
    height: 50px;
    width: 50px;
    background-color: rgba(255,255,255,.8);;
    border-radius: 50%;
    display: inline-block
}

.social-icons {
    list-style: none;
    display: inline-flex;
    right: 16px;
    position: relative
}

.social-icons li {
    padding: 10px
}

.social-icons li i {
    line-height: 50px;
    position: relative;
    font-size: 30px;
    color: #004c4c;
}
 </style>
