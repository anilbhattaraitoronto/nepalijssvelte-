<script>
    import { onMount } from "svelte";

    onMount(() => {
        fetch("https://meroapi.merohouse.com/api/posts/dranil/latest")
            .then((res) => res.json())
            .then((data) => console.log(data))
            .catch((err) => console.log(err));
    });
</script>

<style>
    main {
        text-align: center;
        padding: 1em;
        max-width: 240px;
        margin: 0 auto;
    }

    h1 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 4em;
        font-weight: 100;
    }

    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }
</style>

<main>
    <h1>Hello world!</h1>
</main>
