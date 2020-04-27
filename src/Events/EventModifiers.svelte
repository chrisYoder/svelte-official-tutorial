<script>
  let modifierSyntax = `on:event|modifier|modifier2`;

  const handleClick = () => {
    alert("No more alerts after this one");
  };
</script>

<style>
</style>

<h3>Event Modifiers</h3>
<ul>
  <li>DOM events can have modifiers that alter their behavior</li>
  <li>The modifiers include:
    <ol>
      <li><code>preventDefault</code> calls <code>event.preventDefault()</code> before running the handler. It is useful for client side form submission which typically refreshes the page.</li>
      <li><code>stopPropagation</code> calls <code>event.stopPropagation()</code> which prevents the event reaching the next element</li> 
      <li><code>passive</code> improves scrolling performance on touch/wheel events. Svelte adds this automatically where it is safe to do so.</li> 
      <li><code>capture</code> fires the handler during the capture phase instead of the bubbling phase
        <ul>
          <li>capture phase: The browswer checks to see if the elements outermost ancestor(<code>html</code>) has an <code>onclick</code> event handler registered to it for the caputring phase. If so, then it runs it.Then it repeats the process until it reaches the element that was actually clicked on</li>
          <li>bubbling phase: The browser  The browser checks to see if the element that was actually clicked on has an <code>onclick</code> event handler registered on it for the bubbling phase, and runs it if so. Then it moves on to the next immediate ancestor element and does the same thing, then the next one, and so on until it reaches the <code>html</code> element.</li>
        </ul>
      </li> 
      <li><code>once</code> removes the handler after the first time it runs</li>
      <li><code>self</code> event handler only triggers if <code>event.target</code> is the element itself.</li>
    </ol>
  </li>
  <li>You can chain more than one modifier together</li>
  <li>Syntax: <code>{modifierSyntax}</code></li>
</ul>

Example: 

<button on:click|once={handleClick}>Click Me</button>