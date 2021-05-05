<script>
  import { Router, Link, Route } from "svelte-routing";
  import Contacto from "./views/contacto.svelte";
  import Detalle from "./views/detalle.svelte";
  import Home from "./views/home.svelte";
</script>

<div>
	<h1>App</h1>
	<Router>
		<nav>
			<Link to="/">Home</Link>
			<Link to="/Detalle">Detalle</Link>
			<Link to="/Contacto">Contacto</Link>
		</nav>

		<Route path="/">
			<Home></Home>
		</Route>
		<Route path="/Detalle">
			<Detalle></Detalle>
		</Route>
		<Route path="/Contacto">
			<Contacto></Contacto>
		</Route>
	</Router>
</div>
<style>
  h1 {
    color: #00fff2;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
</style>
