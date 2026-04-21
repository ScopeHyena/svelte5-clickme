<script lang="ts">
    let messages = $state("");

    function showMessage() {
        messages = "Hello, World!";
    }
</script>

<main>
    <input type="text" bind:value={ messages } placeholder="push the button." />
    <button onclick = { showMessage }>
        Click Me
    </button>
</main>

<style>
    main {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        max-width: 200px;
        margin: 2rem;
    }

    input, button {
        padding: 0.5rem;
        font-size: 1rem;
    }
</style>
