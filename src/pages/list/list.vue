<template>
	<div>
		<mt-header title="这里是标题超出的内容会自动隐藏啊哈哈哈">
			<router-link to="/" slot="left">
				<mt-button icon="back">返回</mt-button>
			</router-link>
			<mt-button icon="more" slot="right"></mt-button>
		</mt-header>
		
		<mt-navbar class="page-part" v-model="selected">
			<mt-tab-item id="1">选项一</mt-tab-item>
			<mt-tab-item id="2">选项二</mt-tab-item>
			<mt-tab-item id="3">选项三</mt-tab-item>
		</mt-navbar>
		 
		<mt-tab-container v-model="selected">
			<mt-tab-container-item id="1">
				<mt-cell v-for="n of 5" :title="'标题'+n" />
			</mt-tab-container-item>
			<mt-tab-container-item id="2">
				<mt-cell v-for="n of 6" :title="'文章'+n" />
			</mt-tab-container-item>
			<mt-tab-container-item id="3">
				<mt-cell v-for="n of 4" :title="'内容'+n" />
			</mt-tab-container-item>
		</mt-tab-container>
		
		<mt-button type="default">default</mt-button>
		<mt-button type="primary" size="normal">primary</mt-button>
		
		<mt-cell title="标题" value="说明"></mt-cell>
		<mt-cell title="标题" is-link to="https://www.baidu.com/" label="备注信息"></mt-cell>
	</div>
</template>

<script>
	export default {
		name:'List',
		data () {
			return {
				selected:'1'
			}
		}
	}
</script>

<style>
</style>