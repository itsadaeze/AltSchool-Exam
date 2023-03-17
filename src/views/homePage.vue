<template>
  <div class="header-box">
  <header>
    <img
      alt="AltSchool logo"
      class="logo"
      src="@/assets/ada.jpg"
      width="125"
      height="125"
    />
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/counter">Counter</RouterLink>
        <a href="https://github.com/itsadaeze/AltSchool-Exam">Github</a>

      </nav>
    </div>
  </header>
  </div>
  <main>
    <!-- altschool wrapper section-->
    <div class="altschool-wrapper">
      <h3 class="welcome">
        Welcome 👋 <br />
        I'm Ugwu Adaeze(AltSchooler)
      </h3>
      <div>
   
        <p class="altschool-history">
          My journey in AltSchool has been an exicting one so far. My Tech skills has improved beyond my expectations, I am truly proud and happy to be an Altschooler. I will happily recommend it to anyone intrested in changing their lives via tech. Thank you Altchool.
        </p>
        <button class="project-btn"><RouterLink to="/counter" class="project-link">Check my Exam Project  ⬅️</RouterLink></button>

      </div>
    </div>
    
    <!-- skill/ technology used-->
    <div class="skills">
      <skills-used />
    </div>
  </main>
  <footer-section />
</template>

<script>

import skillsUsed from "@/components/skillsUsed";
import footerSection from "@/components/footerSection";


export default {
  components: {
    
    skillsUsed,
    footerSection,
   
  },
};
</script>

<style>
.header-box{
  background: #e030ab;
}
header {
  line-height: 1.5;
  max-height: 100vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1440px;
  vertical-align: center;
  background: #e030ab;
  margin: 0 auto;
}
.altschool-wrapper {
  margin-top: 30px;
}
.welcome{
  padding-left: 10px;
  color: #e030ab;
  line-height: 30px;
}
.altschool-name{
  text-align: center;
  color: #e030ab;
  font-size: 16px;
  padding-left: 0px 10px;

}
.altschool-history {
  padding:0px 10px;
  line-height:32px;
  color: #75787a;
}
.project-btn{
  padding: 16px;
  background-color: #e030ab;
  color: white;
  border: none;
  border-radius: 4px;
  margin: 10px;

}
.project-link{
  text-decoration: none;
  color: white;
}
.logo {
  margin: 0 2rem 0 0;
  width: 60px;
  height: 60px;
  padding-left: 10px;

}
.rasheed-img {
  border-radius: 50%;
  border: 1px solid white;
  width: 32px;
  height: 32px;

}
nav {
  font-size: 15px;
  margin-top: 2rem;
  display: flex;
  align-items: center;
  margin: auto 0;
  margin-right: 10px;
  width: 80%;
}

nav a.router-link-exact-active {
  text-decoration: none;
  color: white;
}

nav a.router-link-exact-active:hover {
  color: white;
  text-decoration: none;
}

nav a {
  display: inline-block;
  padding: 0 .5rem;
  border-left: 1px solid var(--color-border);
  text-decoration: none;
  color: #630802;
}

nav a:first-of-type {
  border: 0;
}
main {
  max-width: 700px;
  margin: 0 auto;
}
.about-wrapper,.project-wrapper {
    background-color: #7fb9e2;

  height: 250px;
  padding-top:10px;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  border-radius: 10px;
  margin: 30px 10px;
  padding:10px;
}
.about-project{
  width:100%;
  margin: 70px 0px;
}
.skills {
  margin-bottom: 70px;
  width: 100%;
}
@media (min-width: 768px) {

.about-project{
  display: flex;
  justify-content: space-between;
  width:100%;
}
.about-wrapper,.project-wrapper {
 width: 50%;
}

}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    justify-content: space-between;
    padding-right: calc(var(--section-gap) / 2);
    max-width: 1440px;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    justify-content: space-between;
    flex-wrap: wrap;
  }
  nav {
    font-size: 1rem;
    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
