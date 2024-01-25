<template>
  <header>
    <div>

      <div>
        <img class="header-logo" src="/src/assets/Logo_4.png" alt="Logo" />

      </div>


    </div>
  </header>

    <br>
    <div v-if="loggedIn">
      <workout-timer />
    </div>
 
  <router-view />

  <div id="capstone-app">

    <footer>
      <p>
        © 2024 Gym Buddy Inc.. All rights reserved. 
      </p>
<p>Cookie-monster policy, Privacy and Terms.</p>

    </footer>

  </div>
</template>

<script>
// import WorkoutService from './services/WorkoutService';
// import GymSessionService from './services/GymSessionService';
import WorkoutTimer from './components/WorkoutTimer.vue';


export default {
  components: {
    WorkoutTimer
  },
  data() {
    return {
      isLoggedIn: false,
    }
  },
  computed: {
    loggedIn() {
      const loggedIn = this.$store.state.loggedIn;
      console.log('Is user logged in?', loggedIn);
      return loggedIn;
    },
  },
}
</script>





<style>

#root {
  /* display: flex; */
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  height: 1009px; 
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

}

#app {

  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  /* margin: 0;
  padding: 0;
  box-sizing: border-box; */
  /*position: relative; 
  height: 100vh;
  gap: 20px; */
  /* display: grid; 
  grid-template-columns: 1fr;*/
  /* grid-template-areas: "nav"
    "view"
    "footer"; */
}

header {
  margin: 0;
  padding: 0;
  justify-content: center;
  text-align: center;
  background-color: #ddeed6;


  /* color: #fff; */
  /* box-shadow: 0 0 10px rgba(20, 20, 20, 0.589); */
  /* width: 100vw;
  box-sizing: border-box;
  position: fixed;
  top: 0;
  left: 0; */
  /* display: flex; */

}

.header-logo {
  max-width: 200px;
  display: block;
  max-height: 100%;
  margin: auto;
  padding-top: px;
  padding-bottom: 25px;
  justify-content: center;
}

h1 {
  font-size: 2rem;
}

h2 {
  font-size: 1rem;
}
/* 
#nav {
  text-align: center;
/* margin: 10px;  */
  /* font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; */
 /* background-color: rgba(238, 217, 25, 0.445);
 padding: 15px;
 width: 359px; */
 

button {
  margin: auto;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  border-radius: 75px;
  /* Adjust the border-radius as needed for rounded corners */
  background-color: rgba(189, 236, 150, 0.9);
  /* Add your desired background color */
  color: #444343;
  /* Set text color to improve visibility */
  cursor: pointer;
  box-shadow: 0 0 10px rgba(20, 20, 20, 0.589);
}

button:hover {
  background-color: #3d6e8f;
  /* Change background color on hover */
}

i {
  margin: 12px;
  padding: 12px;
}

footer {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 13px;
  background-color: #333;
  color: #fff;
  padding: 5px;
  text-align: center;
  position: relative;
  bottom: 0;
  margin-top: 0px;
  
}


/* .wrapper {
  padding: 20px;
} */
/* body {
  margin: 0;
  padding: 0;
  min-height: 100vh;
  display: flex;
  flex-direction: column;

  

 
} */

/* img {
  max-width: 200px;
  display: block;
  margin-bottom: 20px;
  border-radius: 25px;
} */


/* .banner {
  /* height: 200px;
  /* background-image: url('@/assets/banner.jpg'); */
/* background-size: cover; */





@media screen and (min-width: 600px) {
  body {
    font-size: 18px;
    /* Adjust font size for tablets */
    /* max-width: 600px; */
  }
:root{  
  min-width: 100%;
  min-height: 100%; 
}
  
}

/* Desktop styles */
@media screen and (min-width: 1200px) {
  :root{  
  min-width: 100%;
  min-height: 100%; 
}

@media print {
  .noprint {
    display: none;
  }
}
}

</style>
