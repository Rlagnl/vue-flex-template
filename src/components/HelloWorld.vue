<template>
	<div class="hello">
		<h1 @click="onclick">{{ computedMsg }}</h1>
		<p>
			For a guide and recipes on how to configure / customize this project,
			<br />check out the
			<a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
		</p>
		<h3>Installed CLI Plugins</h3>
		<ul>
			<li>
				<a
					href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel"
					target="_blank"
					rel="noopener"
				>babel</a>
			</li>
			<li>
				<a
					href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint"
					target="_blank"
					rel="noopener"
				>eslint</a>
			</li>
		</ul>
		<h3>Essential Links</h3>
		<ul>
			<li>
				<a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a>
			</li>
			<li>
				<a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a>
			</li>
			<li>
				<a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a>
			</li>
			<li>
				<a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a>
			</li>
			<li>
				<a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a>
			</li>
		</ul>
		<h3>Ecosystem</h3>
		<ul>
			<li>
				<a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a>
			</li>
			<li>
				<a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a>
			</li>
			<li>
				<a
					href="https://github.com/vuejs/vue-devtools#vue-devtools"
					target="_blank"
					rel="noopener"
				>vue-devtools</a>
			</li>
			<li>
				<a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a>
			</li>
			<li>
				<a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a>
			</li>
		</ul>
	</div>
</template>

<script lang='ts'>
import {Vue, Component, Prop} from 'vue-property-decorator';

@Component({
	watch: {
		count: {
			handler: function (val, oldval) {
				console.log('watch: ' + val)
      },
      // 对象内部的属性监听，也叫深度监听
			deep: true
		}
	}
})
export default class App extends Vue {
  // 父类传参
  @Prop(String) msg!: String;
  // data可以声明成类属性形式
	private count: number = 0
	// computed属性
	get computedMsg(): string {
		return this.msg + ' >>> click me: ' + this.count
	}
	// method方法
	private onclick(): void {
		this.count++
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
	margin: 40px 0 0;
}
ul {
	list-style-type: none;
	padding: 0;
}
li {
	display: inline-block;
	margin: 0 10px;
}
a {
	color: #42b983;
}
</style>
