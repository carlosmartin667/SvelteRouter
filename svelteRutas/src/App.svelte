<script>
  import { Router, Link, Route } from "svelte-routing";
  import Contacto from "./views/contacto.svelte";
  import Detalle from "./views/detalle.svelte";
  import Home from "./views/home.svelte";
</script>

<div>
  <Router>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <Link to="/">Home</Link>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon" />
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-item nav-link" href="#"
              ><Link to="/Detalle">Detalle</Link></a
            >
          </li>
          <li class="nav-item">
            <a class="nav-item nav-link" href="#"
              ><Link to="/Contacto">Contacto</Link></a
            >
          </li>
        </ul>
      </div>
    </nav>
    <div class="container ">
      <br />
      <Route path="/">
        <Home />
      </Route>
      <Route path="/Detalle">
        <Detalle />
      </Route>
      <Route path="/Contacto">
        <Contacto />
      </Route>
    </div></Router
  >
</div>
