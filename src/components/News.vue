<template>
	<div>
		<button @click="getList">点击获取新闻</button>
		<ul>
			<li v-for="item,key in list">{{item.TITLE}}</li>
		</ul>
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
				var api='http://app.gd.gov.cn/xxts/pushinfo_json.php';
				this.$http.jsonp('http://www.gd-info.gov.cn/ApiFindToArticleJsonp.action?',{ params:{
                        index:1,
                        siteid:'sdq',
                        topicid:'sdgs',
                    },callback: 'fn1'}).then(result=>{
					//console.log(result);
					this.list=result.body.data.list;
					console.log(this.list);
				},err=>{
					console.log(err)
				})
			}
		}
	}
</script>

<style>
</style>