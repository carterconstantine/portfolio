<script>
    let { title } = $props()
</script>

<h1>{title}</h1>

<style>
    h1 {
        text-align: center;
        font-size: clamp(3rem, 4rem, 5rem)
    }
</style>