<script>
  let m = {
    x: 0, 
    y: 0
  }

  function handleMouseMove(e) {
    m.x = e.clientX;
    m.y = e.clientY;
  }
</script>
<style>
div {
width: 100%;
height: 100px;
}
</style>

<h3>Dom Events</h3>
<ul>  
  <li>I can listen to any event on any element using the <code>on:</code> directive</li>
</ul>

Example:

<div on:mousemove={handleMouseMove}>
  <p>The mouse position is {m.x} x {m.y}</p>
</div>