### Grid 宫格
*已经支持在nvue页面中使用*

宫格组件，组件名：``uni-grid``，代码块： uGrid。

### 使用方式

在 ``script`` 中引用组件 

```javascript
import uniGrid from "@/components/uni-grid/uni-grid.vue"
import uniGridItem from "@/components/uni-grid-item/uni-grid-item.vue"
export default {
    components: {uniGrid,uniGridItem}
}
```

在 ``template`` 中使用组件

```html
<!-- 一般用法 -->
<uni-grid :column="3">
	<uni-grid-item>
		<text class="text">文本</text>
	</uni-grid-item>
	<uni-grid-item>
		<text class="text">文本</text>
	</uni-grid-item>
	<uni-grid-item>
		<text class="text">文本</text>
	</uni-grid-item>
</uni-grid>

<!-- 不带边框并矩形显示 -->
<uni-grid :column="3" :show-border="false"  :square="false">
	<uni-grid-item>
		<text class="text">文本</text>
	</uni-grid-item>
	<uni-grid-item>
		<text class="text">文本</text>
	</uni-grid-item>
	<uni-grid-item>
		<text class="text">文本</text>
	</uni-grid-item>
	<uni-grid-item>
		<text class="text">文本</text>
	</uni-grid-item>
	<uni-grid-item>
		<text class="text">文本</text>
	</uni-grid-item>
	<uni-grid-item>
		<text class="text">文本</text>
	</uni-grid-item>
</uni-grid>
```

### 属性说明

**uni-grid 属性说明：**

|属性名		|类型	|默认值	|说明				|
|---		|----	|---	|---				|
|column		|Number	|3		|每列显示个数		|
|showBorder	|Boolean|true	|是否显示边框		|
|borderColor|String	|#d0dee5|边框颜色			|
|square		|Boolean|true	|是否方形显示		|
|highlight	|Boolean|true	|点击背景是否高亮	|

### 事件说明
|事件名	|说明			|返回值											|
|---	|----			|---											|
|@change|点击 grid 触发	|e={detail:{index:0}}，index 为当前点击 gird 下标|

**Tips**

- 删除组件自带圆点角标效果，完全交给用户实现，示例有简单角标效果实现
- Grid 组件仅在自定义组件模式下支持
- column 属性最大值最好不要超过 5 个，如果超过，注意内容显示
- 支付宝小程序平台需要在支付宝小程序开发者工具里开启 component2 编译模式，开启方式： 详情 --> 项目配置 --> 启用 component2 编译
- 为了避免高度显示错误组件内必须要有内容

### 插件预览地址

[https://uniapp.dcloud.io/h5/pages/extUI/grid/grid](https://uniapp.dcloud.io/h5/pages/extUI/grid/grid)
