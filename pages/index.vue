<template>
  <main>
  	<div class="background">
  		<app-masthead />
  	</div>
  	<div class="headings">
       <h1>Hello, I'm Teona Mushambadze</h1>	
       <h2>Front End Engineer</h2>
       <p>with a passion for Vue and graphic design, Tech geek, VR Photographer, Introvert, Life long learner, Curious cat, Stargazer (='.'=)</p>
  	</div>
  	<div class="links">
  	  <div class="home__links"><a href="https://github.com/highflyer910" aria-label="Github" rel="noopener"><i class="fab fa-github-square" aria-hidden="true"></i></a></div>
	  <div class="home__links"><a href="https://twitter.com/highflyer910" aria-label="Twitter" rel="noopener"><i class="fab fa-twitter-square" aria-hidden="true"></i></a></div>
	  <div class="home__links"><a href="https://codepen.io/highflyer/" aria-label="Codepen" rel="noopener"><i class="fab fa-codepen" aria-hidden="true"></i></a></div>
	  <div class="home__links"><a href="https://dev.to/highflyer910/" aria-label="Dev.to" rel="noopener"><i class="fab fa-dev" aria-hidden="true"></i></a></div>
	  <div class="home__links"><a href="https://www.behance.net/highflyer910" aria-label="Behance" rel="noopener"><i class="fab fa-behance" aria-hidden="true"></i></a></div>
  	</div>
  </main>
</template>

<script>
import AppMasthead from '~/components/AppMasthead.vue';

export default {
	components:{
		AppMasthead
	}
 
}
</script>

<style lang="scss" scoped>

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
	padding-top: 40px;
	margin-right: 10px;
}
.headings { 
	grid-area: 1 / 1 / 4 / 3; 

	color: #3F3D56;
    padding: 35px;

}

h1{
	font-size: 3rem;
}

h2{
	font-size: 2rem;
}
.links { 
	grid-area: 4 / 1 / 6 / 3; 
	font-size: 1.4em;
    padding-top: 8px;
    padding-bottom: 8px;
    max-width: 960px;  /* compatibility large screen fallback */
    margin: auto;
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
  text-align: center;
}

a:hover{
  color: #6b6894;
}

</style>
