<script lang="ts">
  import Versions from '$lib/ElectronVersions.svelte';
  import ReactiveHash from '$lib/ReactiveHash.svelte';
  import Counter from '$lib/Counter.svelte';
  import logo from '$lib/assets/svelte-logo.png';

  const APP_VERSION = import.meta.env.VITE_APP_VERSION;
</script>

<div id="app">
  <img
    alt="Svelte logo"
    src={logo}
    width="150"
  />

  <p>
    <!-- Example how to inject current app version to UI -->
    App version: {APP_VERSION}
  </p>

  <p>
    For a guide and recipes on how to configure / customize this project,<br />
    check out the
    <a
      href="https://github.com/cawa-93/vite-electron-builder"
      target="_blank"
      rel="noreferrer"
    >
      vite-electron-builder documentation
    </a>
    .
  </p>

  <fieldset>
    <legend>Test Svelte Reactivity</legend>
    <Counter />
  </fieldset>

  <fieldset>
    <legend>Test Node.js API</legend>
    <ReactiveHash />
  </fieldset>

  <fieldset>
    <legend>Environment</legend>
    <Versions />
  </fieldset>
</div>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin: 60px auto;
    max-width: 700px;
  }
  fieldset {
    margin: 2rem;
    padding: 1rem;
  }
</style>
