<script lang="ts">
    import UILayout from "./UILayout.svelte";
    let messages = $state("");

    function showMessage() {
        messages = "Hello, World!";
    }
</script>

<UILayout title="Hello, World">
    <div class="card">
        <input class="card" type="text" bind:value={ messages } placeholder="Push the Button." />
    </div>
    
    <button class="card" onclick={ showMessage }>
        Click Me
    </button>

</UILayout>

<style>
    .card {
        background-color: white;
        border-radius: 18px;
        padding: 20px 24px;
        margin-bottom: 16px;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.03);
        font-size: 1.1rem;
        font-weight: 500;
        color: #1c1c1e;
    }

    input {
        max-width: 100%;
        border: 1px solid rgba(0, 0, 0, 0.05);
    }

    button {
        width: 100%;
        text-align: start;
        color: #ff3e00;
    }

</style>
