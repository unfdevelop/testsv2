<script>
	import Block from './blocks.svelte';
	let blocks =[{color: "red", visible: true},{color: "green", visible: true},{color: "blue", visible: true}];
	let showElem = i => {
		blocks.forEach(el=> el.visible=true);
		blocks[i].visible = false;
	}
</script>
<style>
	.components{
		display: flex;
		flex-wrap: wrap;
		justify-content: space-around;
	}
	.elem1{
		box-sizing: border-box;
		border:1px solid black;
		width: 100px;
		height: 100px;
	}
	.items{
	  display:flex;
	  justify-content: space-between;
	  flex-wrap: wrap;
	  width: 320px;
	}
</style>
<div class="components">


	<div class="comp comp2">
		<div class="items">
			<Block {...blocks[0]} on:click={(e) => showElem(0)} />
			<Block {...blocks[1]} on:click={(e) => showElem(1)} />
			<Block {...blocks[2]} on:click={(e) => showElem(2)} />
		</div>
	</div>
</div>