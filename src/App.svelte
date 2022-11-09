<script>
  import { Router, Route, Link } from 'svelte-navigator';

  import Home from './index.svelte';
  import About from './About.svelte';
</script>

<Router>
  <!-- <nav>
    <Link to="/">Home</Link>
    <Link to="about">About</Link>
  </nav> -->
  <div>
    <Route path="/">
      <Home />
    </Route>
    <Route path="about" component={About} />
  </div>
</Router>
