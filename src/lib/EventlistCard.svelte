<script>
    import { IconPlayerPlayFilled, IconRotateClockwise2 } from "@tabler/icons-svelte";
	import IconButton from "./IconButton.svelte";
    export let eventlist;

    let wow = false;

    console.log(eventlist)
</script>


<div class="card-container">
    <div class="card main" style="--image-url: url('{eventlist.image}'); --bg: {!eventlist.completed ? "linear-gradient(#00000000, #000000bb)" : "linear-gradient(#ffffff00, #ffffffbb)"}">
        {#if eventlist.completed}
            <div class="wowbutton">
                    <span on:click={() => wow = !wow }>{wow ? "😮" : "😐"}</span>
            </div>
        {/if}
        <div class="content" style="--titlecolor: {!eventlist.completed ? "#fff" : "#000"}">
            {#if !eventlist.completed}
                <IconButton title="Dive in" bgcolor="black" color="white">
                        <IconPlayerPlayFilled slot="icon" />
                </IconButton>
            {:else}
                <IconButton title="Relive" bgcolor="white" color="black">
                    <IconRotateClockwise2 slot="icon" />
                </IconButton>
            {/if}
            <p class="title">{eventlist.title}</p>
        </div>
    </div>
</div>

<style>
    .card-container {
        position: relative;
        margin-bottom: 16px;
        display: block;
    }

    .card {
        border-radius: 8px;
        box-shadow: 0 4px 8px #ccc;
        height: 200px;
        max-width: 400px;
        width: 100%;
    }
    
    .main {
        position: relative;
        justify-content: end;
        background-image: var(--image-url);
        background-size:     cover;                      /* <------ */
        background-repeat:   no-repeat;
        background-position: center center;   
    }

    .main:before {
        border-radius: 8px;
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: var(--bg);
        z-index: 2;

    }

    .content {
        z-index: 3;
        padding: 16px;
        color: var(--titlecolor);
        left: 0;
        bottom: 0;
        position: absolute;
    }

    .wowbutton {
        z-index: 3;
        position: absolute;
        display: inline-block;
        top: 0;
        right: 0;
        padding: 8px;
        padding-left: 16px;
        padding-bottom: 12px;
        font-size: 35px;
        background-color: #00000099;
        border-top-right-radius: 8px;
        border-bottom-left-radius: 99px;
    }

    .title {
        font-size: 1.5rem;
        font-weight: bold;
        margin: 0;
        margin-top: 8px;
    }
</style>