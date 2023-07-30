<script>
    export let title;
    export let color;
    export let bgcolor;
</script>

<div class="button" style="color: {color}; background-color: {bgcolor}"><slot name="icon" /><span class="button-title">{title}</span></div>

<style>
    .button {
        padding: 4px 12px;
        border-radius: 8px;
        display: inline-flex;
        align-items: center;
        background-color: #000000;
        cursor: pointer;
        box-shadow: 0 0 10px #aeaeae;
        opacity: 85%;
    }

    .button-title {
        margin-left: 8px;
    }
</style>