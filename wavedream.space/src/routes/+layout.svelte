<script>
  import "../app.css";
  import "@fontsource/ubuntu/300.css"

</script>


<slot />

<div id="navbar" class="flex w-screen h-[52px] bg-slate-900/50">
  <a href="../">
    <img id="logo" class="max-w-[50px] logo" draggable="false" src="/WaveDream_Logo_Optimized.svg" alt="WaveDream.Space" />
  </a>
</div>

<style lang="postcss">
#navbar {
    position: fixed;
    top: 0;
    left: 0;
}

#logo {
  margin-top: 8px;
  margin-left: 8px;
}
</style>