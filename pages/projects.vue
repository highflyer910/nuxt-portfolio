<template>
  <main class="projects-page">
    <section>
    	<h1 class="title">Projects</h1>
     <div v-for="project in githubProjects" :key="project.id" class="project">
       <h3><a :href="project.html_url">{{project.name}}</a></h3>
       <p class="stars">🟊 {{project.stargazers_count}}</p>
       <p>{{project.homepage}}</p>
       <p>{{project.description}}</p>
     </div>
    </section>
    <aside>
      <div class="background">
        <app-projectpic />
      </div>
      <h3>About</h3>
      <p>
        I am Teona, a self-taught Front-End Engineer with 2+ years of experience. Deeply in love with Vue and graphic design. 🙃 Tech geek, VR Photographer, Introvert, Life long learner, Curious cat 🐱<br/>
        You can find more about me at <a href="https://highflyer910.github.io">my portfolio</a>.
      </p>
    </aside>
  </main>
</template>

<script>
import AppProjectpic from '~/components/AppProjectpic.vue';
import {mapState} from 'vuex'

export default {
  transition: 'tweakOpacity',
  components: {
    AppProjectpic
  },
  computed: {
    ...mapState([
     'githubProjects',
      ])     
    }
  }

</script>

<style lang="scss" scoped>
.tweakOpacity-enter-active, .tweakOpacity-leave-active {
      transition: opacity .35s ease-out;
}
.tweakOpacity-enter, .tweakOpacity-leave-active {
      opacity: 0;
}

.projects-page {
max-width: 1200px;  
width: 90vw;
margin: auto;	
display: grid;
grid-template-columns:2fr 1fr;
grid-column-gap: 3.2rem;
grid-template-areas: 
     "section" "aside";
}

section{ 
	grid-area: 1 / 1 / 2 / 2;
	background-color: #eee;
	color: #3F3D56;
	padding: 2.4rem;
  margin-top: 2rem;
  a{
    color: #FF6584;
  }
  .title{
    margin-bottom: 1.5rem;
    text-align: center;
  }
}
aside { 
	grid-area: 1 / 2 / 2 / 3;
  .background {
  width: 450px;
  margin: 20px;
  padding-top: 1rem;
  }
  h3{
  text-align: center;
  padding-bottom: 15px;
 }
}

.project{
  margin-bottom: 30px;
}


@media screen and (max-width: 768px) {
   .projects-page{
    grid-tremplate-columns: 2fr 1fr;
    width: 100%;
    margin: 10px auto;
  aside{
    padding: 0;   
    }
  }
}

@media (max-width: 500px) {
  .projects-page{
    grid-template-areas: 
     "aside"
     "section"
  }
}
</style>
