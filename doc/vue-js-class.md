

```html
<div v-bind:class="{ active: isActive }"></div>
```

```html
v-if="range(pageStart, pageEnd).shift() != 1"
v-if="range(pageStart, pageEnd).pop() != pageLast"
v-bind:class="{ active: isActive(n) }"
```

```html
<div class="btn-toolbar" role="toolbar" aria-label="page group" v-if="pageStart > 0">
	<div class="btn-group btn-group-xs" role="group" aria-label="preview page">
		<button type="button" class="btn" v-on:click="search(pageStart)" v-if="range(pageStart, pageEnd).shift() != 1"><span class="sr-only">이전</span><span class="glyphicon glyphicon-menu-left"></span></button>
	</div><!-- /btn-group -->
	<div class="btn-group btn-group-xs" role="group" aria-label="page number" >
		<button type="button" class="btn" v-on:click="search(n)" v-for="n in range(pageStart, pageEnd)" v-bind:class="{ active: isActive(n) }">{{ n }}</button>										
	</div>
	<!-- /btn-group -->
	<div class="btn-group btn-group-xs" role="group" aria-label="next page">
		<button type="button" class="btn" v-on:click="search(pageEnd)" v-if="range(pageStart, pageEnd).pop() != pageLast"><span class="sr-only">다음</span><span class="glyphicon glyphicon-menu-right"></span></button>
	</div><!-- /btn-group -->
</div><!-- /btn-toolbar -->
```


## 출처
- https://vuejs.org/v2/guide/class-and-style.html