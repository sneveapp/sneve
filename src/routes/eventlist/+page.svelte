<script>
	import EventlistCard from "../../lib/EventlistCard.svelte";

    let eventlists = [
        {
            completed: false,
            title: "Working on Sneve!",
            image: "https://img.geocaching.com/waymarking/display/7feeee25-5e31-4987-9989-649412a3fd3a.jpg"
        },
        {
            completed: true,
            title: "Having dinner at Hong Hong",
            image: "https://lh3.googleusercontent.com/p/AF1QipMeaFgtx8NsRQ1P-pN97YJyLYuul_LTbChOe6TT=s1360-w1360-h1020"
        },
        {
            completed: true,
            title: "CLA Klausur",
            image: "https://alumni.ifi.lmu.de/wp-content/uploads/2012/07/3160fbaaec.jpg"
        },
        {
            completed: true,
            title: "Having dinner at Hong Hong",
            image: "https://lh3.googleusercontent.com/p/AF1QipMeaFgtx8NsRQ1P-pN97YJyLYuul_LTbChOe6TT=s1360-w1360-h1020"
        },
        {
            completed: true,
            title: "Having dinner at Hong Hong",
            image: "https://lh3.googleusercontent.com/p/AF1QipMeaFgtx8NsRQ1P-pN97YJyLYuul_LTbChOe6TT=s1360-w1360-h1020"
        }
    ]
</script>

<h1>Eventlists</h1>

{#each eventlists as eventlist}
    <EventlistCard eventlist={eventlist} />
{/each}