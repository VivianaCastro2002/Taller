<template>
    <button >Random Manga</button>
    <button >Random Anime</button>
    <button >Random Country</button>
    <button >Random Anime Recomendations</button>

    <div v-if="randomManga">
        <h3>Random Manga</h3>
        <p>{{ randomManga }}</p>
    </div>

    <div v-if="randomAnime">
        <h3>Random Anime</h3>
        <p>{{ randomAnime }}</p>
    </div>

    <div v-if="countriesPopulation">
        <h3>Countries Population</h3>
        <p>{{ countriesPopulation }}</p>
    </div>

    <div v-if="animeRecomendations">
        <h3>Anime Recomendations</h3>
        <p>{{ animeRecomendations }}</p>
    </div>
</template>
<script>
export default {
    data() {
        return {
            randomManga: null,
            randomAnime: null,
            countriesPopulation: null,
            animeRecomendations: null
        };
    },
    methods: {
        async fetchRandomManga(){
            try {
                const response = await fetch('https://api.jikan.moe/v4/random/manga');
                const data = await response.json();
                this.randomManga = data;
            } catch (error){
                console.error("Error fetching random manga:", error);
            }
        },
        async fetchRandomAnime(){
            try {
                const response = await fetch('https://api.jikan.moe/v4/random/anime');
                const data = await response.json();
                this.randomAnime = data;
            } catch (error){
                console.error("Error fetching random Anime:", error);
            }
        },

}
</script>
