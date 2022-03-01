<template>
  <div id="app">
    <div id="nav">
    <div>
      <b-navbar toggleable="lg" type="light" variant="light" class="ml-auto fixed-top" style="background: linear-gradient(to right, #1EA1A1  0%, #004c4c 100%);">

          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

          <div class="d-flex bd-highlight ">
              <img class="to" src="../src/assets/white3.png">
          </div>

              <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav class="ml-auto">
                  <b-nav-item class="let" style="font-family: 'Poppins', sans-serif; "> <router-link to="/">Home</router-link> </b-nav-item>
                    <b-nav-item class="let" style="font-family: 'Poppins', sans-serif; "> <router-link to="/about">About Us</router-link></b-nav-item>
                  <b-nav-item class="let" style="font-family: 'Poppins', sans-serif; "> <router-link to="/Services">Services</router-link></b-nav-item>
                  <b-nav-item class="let" style="font-family: 'Poppins', sans-serif; "> <router-link to="/Projects">Projects</router-link></b-nav-item>
                  <b-nav-item class="let" style="font-family: 'Poppins', sans-serif; "> <router-link to="/Contact">Contact Us</router-link> </b-nav-item>
                  </b-navbar-nav>
                  </b-collapse>
                </b-navbar>
        </div>
      </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: white;

    &.router-link-exact-active {
      color: #9ddfdf;
    }
  }
}

.let {
  padding-top: 14px 30px;
  margin-right: 30px;
  font-size: 17px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.to{
  width:140px;
  height:60px;
}
</style>
