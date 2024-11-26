<script>
    import LogoContainer from "../molecules/LogoContainer.svelte";
</script>

<div class="infinite-carrousel">
    <LogoContainer />
    <LogoContainer />
</div>

<style>
    .infinite-carrousel {
        white-space: nowrap;
    }
    .infinite-carrousel:hover :global(.logo-container) {
        animation-play-state: paused;
    }
    .infinite-carrousel::before,
    .infinite-carrousel::after {
        position: absolute;
        z-index: 10;
        content: "";
        height: 3vw;
        min-height: 30px;
        width: 15%;
        background: linear-gradient(
            to right,
            var(--accent2-primary),
            transparent
        );
        left: 0;
    }
    .infinite-carrousel::after {
        left: unset;
        right: 0;
        transform: rotateZ(180deg);
    }
</style>