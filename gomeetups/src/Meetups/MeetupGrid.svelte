<script>
    import MeetUpItem from "./MeetUpItem.svelte";

    export let meetups;
</script>

<style>
    #meetups {
        margin-top: 5rem;
    }
</style>

<section id="meetups">
    {#each meetups as meetup}
        <MeetUpItem
            id={meetup.id}
            title={meetup.title}
            subtitle={meetup.subtitle}
            description={meetup.description}
            imageUrl={meetup.imageUrl}
            email={meetup.contactEmail}
            address={meetup.address} 
            isFav={meetup.isFavorite}
            on:toogleFavorite />
    {/each}
</section>
