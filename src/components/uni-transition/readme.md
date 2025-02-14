### Transition 过渡动画

元素的简单过渡动画，组件名：`uni-transition`

### 使用方式

引用组件 

```javascript
import uniTransition from "@/components/uni-transition/uni-transition.vue"
export default {
    components: {uniTransition}
}
```

使用组件

```html
<button type="primary">fade</button>
<uni-transition :mode-class="['fade']" :styles="{'width':'100px','height':'100px';'backgroundColor':'red'}" :show="show" @change="change" />
```

```javascript
import uniTransition from "@/components/uni-transition/uni-transition.vue"
export default {
		components: {
			uniTransition
		},
		data() {
			return {
				show: false,
			}
		},
		onLoad() {},
		methods: {
			open(mode) {
				this.show = !this.show
			},
			change() {
				console.log('触发动画')
			}
		}
	}
```

### 属性说明

|属性名		|类型	|默认值	|说明					|
|---	|---	|---					|---|
|show		|Boolean|false	|控制组件显示或隐藏，	|
|modeClass	|Array	|-		|过渡动画类型			|
|duration	|Number	|300	|过渡动画持续时间		|
|styles		|Object	|-		|组件样式，同 css 样式，注意带’-‘连接符的属性需要使用小驼峰写法如：`backgroundColor:red`	|

#### modeClass 类型说明说明
**格式为** ：`['fade','slide-top']`

|属性名			|说明			|
|---			|---			|
|fade			|渐隐渐出过渡	|
|slide-top		|由上至下过渡	|
|slide-right	|由右至左过渡	|
|slide-bottom	|由下至上过渡	|
|slide-left		|由左至右过渡	|
|zoom-in		|由小到大过渡	|
|zoom-out		|由大到小过渡	|

**注意** 

组合使用时，同一种类型相反的过渡动画如（slide-top、slide-bottom）同时使用时，只有最后一个生效

### 事件说明

|事件称名	|说明				|返回值			|
|---		|---				|---			|
|click		|点击组件触发		|-				|
|change		|过渡动画结束时触发	| e = {detail:true}	|
