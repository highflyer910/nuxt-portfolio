<template>
  <main>
    <section>
    	<h1>Projects</h1>
     <div v-for="project in githubProjects" :key="project.id" class="project">
       <h3><a :href="project.html_url">{{project.name}}</a></h3>
       <p class="stars">🟊 {{project.stargazers_count}}</p>
       <p>{{project.homepage}}</p>
       <p>{{project.description}}</p>
     </div>
    </section>
    <aside>
      <app-projectpic />
      <h3>About</h3>
      <p></p>
    </aside>
  </main>
</template>

<script>
import AppProjectpic from '~/components/AppProjectpic.vue';
import {mapState} from 'vuex'

export default {
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
main {
width: 80vw;
margin: 2% 8%;	
display: grid;
grid-template-columns: 2fr 1fr;
grid-template-rows: 1fr;
grid-column-gap: 50px;
grid-row-gap: 0px;
}

section{ 
	grid-area: 1 / 1 / 2 / 2;
	background-color: white;
	color: #3F3D56;
	padding: 40px;
  a{
    color: #FF6584;
  }
}
aside { 
	grid-area: 1 / 2 / 2 / 3;
  h3{
  text-align: center;
 }
}

.project{
  margin-bottom: 30px;
}
</style>
