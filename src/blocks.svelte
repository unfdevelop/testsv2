<script>
export let color;
export let visible;
</script>
<style>
.item{
  width: 100px;
  opacity: 0;
  height: 100px;
  border: 1px solid black;
}
.item.active{
  opacity: 1;
}
</style>
<div class="item" class:active={visible} style="background-color: {color};" on:click></div>