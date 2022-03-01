<template>
  <div id="app">
    <h2 style="font-family: 'Poppins', sans-serif; color: #004c4c">Projects</h2>

    <!-- Bar containing all sort inputs -->
  <div id="sort-bar" style="font-family: 'Poppins', sans-serif; ">
    <select name="sortBy" id="select" v-model="sortBy">
      <option value="alphabetically" style="font-family: 'Poppins', sans-serif; ">Alphabetically</option>
      <option value="duration" style="font-family: 'Poppins', sans-serif; ">Duration</option>
    </select>
    <button v-on:click="ascending = !ascending" class="sort-button">
      <i v-if="ascending" class="fa fa-sort-up"></i>
      <i v-else class="fa fa-sort-down"></i>
    </button>
    <input type="number" v-model="maxDuration" id="duration-in">
    <input type="text" v-model="searchValue" placeholder="Search Project" id="search-in">
    <i class="fa fa-search"></i>
  </div>

  <!-- Where the array of projects get rendered as cards -->
  <div id="project-container">
    <div class="card" v-for="project in filteredProjects" :key="project.title">
      <img :src= "project.img" class="project-image">
      <div class="content">
        <h1 class="project-title" style="font-family: 'Poppins', sans-serif; ">
          {{ project.title }}
        </h1>
        <p style="font-family: 'Poppins', sans-serif; ">
          {{ project.description }}
        </p>

        <h3 style="font-family: 'Poppins', sans-serif; ">
          Duration:
        </h3>
        <p style="font-family: 'Poppins', sans-serif; ">
          {{project.duration}} Years
        </p>

      </div>

    </div>
  </div>

  <div class="page-content page-container" id="page-content">
      <div class="pad">
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
    <div class="footer-basic">
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

<script>
export default {
  data () {
    return {
      ascending: true,
      sortBy: 'alphabetically',
      searchValue: '',
      maxCookingTime: null,
      projects: [
        { title: 'Prestige Home Building', description: 'The proposed buildings would generally be modern in design', duration: 7, img: require('../assets/ashkan-forouzani-v31lgBn5114-unsplash.jpg') },
        { title: 'Living Well Remodeling', description: 'The proposed buildings would generally be modern in design', duration: 2, img: require('../assets/josue-isai-ramos-figueroa-qvBYnMuNJ9A-unsplash.jpg') },
        { title: 'Five-star Construction', description: 'The proposed buildings would generally be modern in design', duration: 5, img: require('../assets/lance-anderson-QdAAasrZhdk-unsplash.jpg') },
        { title: 'Hotel Transvager', description: 'The proposed buildings would generally be modern in design', duration: 4, img: require('../assets/michael-bader-eyq7H7gO0EY-unsplash.jpg') },
        { title: 'Skyline Structures', description: 'The proposed buildings would generally be modern in design', duration: 6, img: require('../assets/luca-bravo-SRjZtxsK3Os-unsplash.jpg') },
        { title: 'Rendo Condos', description: 'The proposed buildings would generally be modern in design', duration: 3, img: require('../assets/jamar-penny-ZgmGq_eFmUs-unsplash.jpg') },
        { title: 'Hotel Pensava', description: 'The proposed buildings would generally be modern in design', duration: 5, img: require('../assets/viktor-jakovlev-H0vuplqoX0c-unsplash.jpg') },
        { title: 'Trageti Lodges', description: 'The proposed buildings would generally be modern in design', duration: 4, img: require('../assets/scott-webb--udZnjsCzsE-unsplash.jpg') }
      ]
    }
  },
  computed: {
    filteredProjects () {
      let tempProjects = this.projects

      // Process search input
      if (this.searchValue !== '' && this.searchValue) {
        tempProjects = tempProjects.filter((item) => {
          return item.title
            .toUpperCase()
            .includes(this.searchValue.toUpperCase())
        })
      }

      // Show sorted array in descending or ascending order
      if (!this.ascending) { tempProjects.reverse() }
      return tempProjects
    }
  }
}
</script>

<style scoped>
#app {
  background: #fff;
  border-radius: 4px;
  padding: 20px;
  transition: all 0.2s;
}
h2 {
  font-weight: bold;
  margin-bottom: 15px;
}

h3 {
  font-weight: 600;
  font-size: 16px;
}

#project-container {
  display: flex;
  flex-wrap: wrap;
}
.pad {
     padding-left: 15rem;
     padding-top: 6rem;
     padding-bottom: 6rem;
 }
.card {
  border-radius: 5px;
  box-shadow: rgba(0, 0, 0, 0.3) 0 5px 10px;
  margin: 20px;
  width: 45%;
  margin-left: 32px;
}

.content {
  padding: 30px;
}

.project-title {
  font-size: 18px;
  font-weight: 600;
}

.project-image {
  width: 100%;
  max-height: 400px;
  padding: -10px -10px;;
}

#sort-bar {
  width: 100%;
  height: 50px;
  margin: 10px;
  background: linear-gradient(to right, #1EA1A1  0%, #004c4c 100%);
  display: flex;
  flex-wrap: wrap;
  padding: 10px;
  border-radius: 25px;
}

@media (max-width: 700px) {
#sort-bar {
  width: 100%;
  height: 50px;
  margin: 10px;
  background: linear-gradient(to right, #1EA1A1  0%, #004c4c 100%);
  display: flex;
  flex-wrap: wrap;
  padding: 10px;
  border-radius: 25px;
}

.pad {
     padding-left: 6rem;
     padding-top: 6rem;
 }

.card {
  border-radius: 5px;
  box-shadow: rgba(0, 0, 0, 0.3) 0 5px 10px;
  margin: 20px;
  width: 100%;
  margin-left: 32px;
}

.content {
  padding: 30px;
}

.sort-button {
  background-color: #1EA1A1;
  border: none;
  height: 100%;
  width: 50px;
}

#select {
  background-color: #1EA1A1;
  border: none;
  font-size: 11px;
  font: bold;
  color: white;
}
}

@media (width: 900px -702px) {
 .card {
  border-radius: 5px;
  box-shadow: rgba(0, 0, 0, 0.3) 0 5px 10px;
  margin: 20px;
  width: 100%;
  margin-left: 32px;
}
}

.sort-button {
  background-color: #1EA1A1;
  border: none;
  height: 100%;
  width: 50px;
}

.hover {
    background-color: rgba(0,0,0, 0.2);
    cursor: pointer;
  }

  #sort-label {
    font-size: 12px;
  }

#ascending-icon {
  height: 100%;
  width: 30px;
}

#select {
  background-color: #1EA1A1;
  border: none;
  color: white;
}

  #duration-in {
    width: 30px;
    margin-right: 10px;
  }

  #search-in {
    margin-right: 10px;
  }

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
     padding: 6rem
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
    color: #004c4c;}

</style>
