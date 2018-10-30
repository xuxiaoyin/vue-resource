<template>
	<div>
		<ul>
			<li v-for="item in list">
				{{item.title}}
			</li>
		</ul>
		<button @click="getList()">点击获取数据</button>
	</div>
</template>

<script>
export default{
	data(){
		return{
			list:[]
		}
	},
	methods:{
		getList(){
			var api='http://www.phonegap100.com/appapi.php?a=getPortalList&catid=20&page=1';
			this.$http.get(api).then(response => {
		    // get body data
		    console.log(response)
		    this.list=response.body.result
			  }, response => {
			    // error callback
			     console.log(response)
			  });
		}
	},
	mounted(){
		this.getList();
	}
}
</script>

<style>
</style>