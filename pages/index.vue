<template>
  <main>
  	<div class="background">
  		<app-masthead />
  	</div>
  	<div class="headings">
       <h1>Hello, I'm Teona Mushambadze</h1>	
       <h2>Front End Engineer</h2>
       <p>with a passion for Vue and graphic design, Tech geek, VR Photographer, Introvert, Life long learner, Curious cats (='.'=)</p>
  	</div>
  	<div class="links">
  	  <div class="home__links"><a href="https://github.com/highflyer910" aria-label="Github" rel="noopener"><font-awesome-icon :icon="['fab', 'github']" aria-hidden="true" /></a></div>
	  <div class="home__links"><a href="https://twitter.com/highflyer910" aria-label="Twitter" rel="noopener"><font-awesome-icon :icon="['fab', 'twitter']" aria-hidden="true" /></a></div>
	  <div class="home__links"><a href="https://codepen.io/highflyer/" aria-label="Codepen" rel="noopener"><font-awesome-icon :icon="['fab', 'codepen']" aria-hidden="true" /></a></div>
	  <div class="home__links"><a href="https://dev.to/highflyer910/" aria-label="Dev.to" rel="noopener"><font-awesome-icon :icon="['fab', 'dev']" aria-hidden="true" /></a></div>
	  <div class="home__links"><a href="https://www.behance.net/highflyer910" aria-label="Behance" rel="noopener"><font-awesome-icon :icon="['fab', 'behance']" aria-hidden="true"/></a></div>
  	</div>
  </main>
</template>

<script>
import AppMasthead from '~/components/AppMasthead.vue';

export default {
  transition: 'tweakOpacity',
	components:{
		AppMasthead
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

main {
width: 100vw;
height: calc(100vh - 100px);	
display: grid;
grid-template-columns: repeat(5, 1fr);
grid-template-rows: repeat(5, 1fr);
grid-column-gap: 0px;
grid-row-gap: 0px;
}

.background { 
	grid-area: 1 / 3 / 6 / 6;  
	padding-top: 70px;
	margin-right: 10px;
}
.headings { 
	grid-area: 2 / 1 / 4 / 3; 
	color: #3F3D56;
  padding-left: 35px;

}

p{
	padding-top: 13px;
}

h1{
	font-size: 3rem;
}

h2{
	font-size: 2rem;
}
.links { 
	grid-area: 3 / 1 / 6 / 3; 
	font-size:2em;
  margin-left: 30px;
  margin-top: 150px;
}

.home__links{
  display: inline;
  letter-spacing: 7px;
  border-radius: 1em;
  transition: .2s ease;
}

a {
  text-decoration: none;
  color: #3F3D56;
  margin: 10px;
}

a:hover{
  color: #6b6894;
}

</style>
