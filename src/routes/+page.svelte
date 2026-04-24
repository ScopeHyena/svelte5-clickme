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
        display: flex;
        background-color: white;
        justify-content: center; 
        align-items: center;
        border-radius: 18px;
        padding: 20px 24px;
        margin-bottom: 16px;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.03);
        font-size: 1.1rem;
        font-weight: 500;
        color: #1c1c1e;
    }

    input.card {
        border: 1px solid rgba(0, 0, 0, 0.05);
        width: 100%;
    }

    button.card {
        width: 100%;
        background-color: #ff3e00;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.25);
        border: none;
        color: white;
    }

    button.card:active {
        color: #f2f2f7;
        transform: scale(0.99);
        background-color: #D13400;
    }
</style>
