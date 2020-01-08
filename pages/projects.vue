<template>
  <main>
    <section>
    	<h1>Projects</h1>
    </section>
    <aside></aside>
  </main>
</template>

<script>
export default {
 
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
	padding: 30px;
}
aside { 
	grid-area: 1 / 2 / 2 / 3; 
}
</style>
