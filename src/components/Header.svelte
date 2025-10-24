<script>
  import Logo from "@/components/Logo.svelte"
  import Button from "@/components/Button.svelte"
</script>

<div class="header">
  <Logo />
  <Button>Start Game</Button>
</div>

<style lang="scss">
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>
