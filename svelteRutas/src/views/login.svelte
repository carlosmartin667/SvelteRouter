<script>
  import { user } from "../stores/stores";
  import { navigate } from "svelte-routing";
  let email = "",
    password = "";

  const procesarFormulario = () => {
    if (!email.trim() || !password.trim()) {
      console.log("campos vacios");
      return;
    }

    user.setUser({
      displayName: email,
      uid: Date.now(),
    });

    email = "";
    password = "";

    console.log($user);
    navigate("/Detalle", { replace: true });
  };
</script>

<div>
  <div class="alert alert-primary" role="alert">Login</div>
  <form on:submit|preventDefault={procesarFormulario}>
    <div class="input-group mb-3">
      <div class="input-group-prepend">
        <span class="input-group-text" id="basic-addon1">Email</span>
      </div>
      <input
        type="text"
        class="form-control"
        placeholder="Email"
        aria-label="Username"
        aria-describedby="basic-addon1"
        bind:value={email}
      />
    </div>
    <div class="input-group mb-3">
      <div class="input-group-prepend">
        <span class="input-group-text" id="basic-addon1">Password</span>
      </div>
      <input
        type="text"
        class="form-control"
        placeholder="Password"
        aria-label="Username"
        aria-describedby="basic-addon1"
        bind:value={password}
      />
    </div>
    <button type="submit" class="btn btn-outline-primary">Acceder</button>
  </form>
</div>
