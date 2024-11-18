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
    .logos::before,
    .logos::after {
        position: absolute;
        z-index: 10;
        content: "";
        height: 50px;
        width: 250px;
        background: linear-gradient(
            to right,
            var(--accent2-primary),
            transparent
        );
        left: 0;
    }
    .logos::after {
        left: unset;
        right: 0;
        transform: rotateZ(180deg);
    }

    /* Media Query for small-screens */
    @media (max-width: 768px) {
        .logos::before,
        .logos::after {
            width: 50px;
        }
    }
</style>