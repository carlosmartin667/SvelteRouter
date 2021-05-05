<script>
  import { user } from "../stores/stores";
  import { navigate } from "svelte-routing";

  console.log($user);

  const IrLoguearse = () => {
    navigate("/Login");
  };
</script>

<div class="alert alert-primary" role="alert">detalle</div>

{#if $user}
  <h1>{$user.displayName}</h1>
  <h1>{$user.uid}</h1>
{:else}
  <div class="alert alert-warning" role="alert">
    PARA VER LOS DATOS PRIMERO LOGUEARSE AQUI :
  </div>
  <button on:click={IrLoguearse()} class="btn btn-outline-danger"
    >LOGUEARSE
  </button>
{/if}
