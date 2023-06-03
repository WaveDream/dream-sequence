<script>
  import "../app.css";
  import "@fontsource/jura"
</script>


<slot />

<div id="navbar" class="flex w-screen h-[52px] opacity-50 bg-slate-900"></div>

<style lang="postcss">
#navbar {
    position: fixed;
    top: 0;
    left: 0;
}
</style>