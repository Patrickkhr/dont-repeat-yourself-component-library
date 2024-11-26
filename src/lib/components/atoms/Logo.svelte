<script>
    export let source = ''
    export let alt = ''
</script>

<li>
    <img src={source} alt={alt}>
</li>

<style>
    li {
        display: inline-block;
    }
    img {
        height: 3vw;
        min-height: 30px;
        margin: 0 40px;
    }
</style>