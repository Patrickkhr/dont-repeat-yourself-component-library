<script>
    import LogoContainer from "../molecules/LogoContainer.svelte";
</script>

<div class="logos">
    <LogoContainer />
    <LogoContainer />
</div>

<style>
    .logos {
        white-space: nowrap;
    }
    .logos:hover :global(.logo-container) {
        animation-play-state: paused;
    }
</style>