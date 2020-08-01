<script>
	import Block from './blocks.svelte';
	let blocks =[{color: "red", visible: true},{color: "green", visible: true},{color: "blue", visible: true}];
	let showElem = i => {
		blocks.forEach(el=> el.visible=true);
		blocks[i].visible = false;
	}
</script>
<style>
	.items{
	  display:flex;
	  justify-content: space-between;
	  flex-wrap: wrap;
	  width: 320px;
	}
</style>

<div class="items">
	<Block {...blocks[0]} on:click={(e) => showElem(0)} />
	<Block {...blocks[1]} on:click={(e) => showElem(1)} />
	<Block {...blocks[2]} on:click={(e) => showElem(2)} />
</div>