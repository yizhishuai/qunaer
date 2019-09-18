<template>
	<city-header></city-header>
	<city-search></city-search>
</template>
<script>
import CityHeader from '@/pages/city/components/Header'
import CitySearch from '@/pages/city/components/Search'
export default{
	name:'City',
	components:{
		CityHeader,
		CitySearch
	}
}
</script>
<style scoped>
	
</style>