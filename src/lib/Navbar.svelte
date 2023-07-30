<script>
    import { page } from '$app/stores';

    $: console.log($page.route)

    import { IconLayoutList, IconHome, IconUser, IconUsersGroup } from "@tabler/icons-svelte"
</script>

<div class="navbar">
    <a class={$page.route.id === "/" ? "active" : ""}  href="/"><IconHome /></a>
    <a class={$page.route.id === "/eventlist" ? "active" : ""} href="/eventlist"><IconLayoutList /></a>
    <a class={$page.route.id === "/groups" ? "active" : ""} href="/groups"><IconUsersGroup /></a>
    <a class={$page.route.id === "/profile" ? "active" : ""} href="/profile"><IconUser /></a>
</div>

<style>
    .navbar {
        background-color: #333;
        overflow: hidden;
        position: fixed;
        bottom: 0;
        width: 100%;
        display: flex;
        justify-content: space-evenly;
        padding-bottom: 8px;
        z-index: 99;
    }

    .navbar a {
        float: left;
        display: block;
        color: #f2f2f2;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        font-size: 17px;
    }

    /* Add a color to the active/current link */
    .navbar a.active {
        color: orangered;
    }
</style>