<template>
	<div>
		<ul>
			<li>
				<nuxt-link exact to="/">Home</nuxt-link>
			</li>
			<li>
				<nuxt-link to="/projects">Projects</nuxt-link>
			</li>
		</ul>
	</div>
</template>


<script>
	export default{

	}
</script>

<style lang="scss" scoped>
   div{
   	display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    ul {
     padding-left: 0;
     li{
      display: inline-block;
      margin-right: 30px;
      font-size: 20px;
      padding-top: 20px;
      font-weight: 500;
     }
    }
   }

   .nuxt-link-active {
  border-bottom: 2px solid;
}
</style>