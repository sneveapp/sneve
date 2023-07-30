<script>
	import Navbar from "../lib/Navbar.svelte";

</script>

<div class="main-container">
    <slot></slot>
</div>

<Navbar />

<style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,400;0,700;1,400;1,700&display=swap');
    
    :global(body) {
        margin: 0;
        font-family: 'Montserrat', sans-serif;
    }

    .main-container {
        padding: 8px;
        margin-top: 3rem;
        overflow: scroll;
    }

    .main-container::--webkit-scrollbar {
        display: none;
    }
</style>