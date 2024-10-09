<template>
    <button @click="fetchRandomManga">Random Manga</button>
    <button @click="fetchRandomAnime">Random Anime</button>
    <button @click="fetchCountriesPopulation">Random Country</button>
    <button @click="fetchAnimeRecomendation">Random Anime Recomendations</button>

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

        async fetchCountriesPopulation(){
            try {
                const response = await fetch('https://countriesnow.space/api/v0.1/countries/population');
                const data = await response.json();
                this.countriesPopulation = data;
            } catch (error){
                console.error("Error fetching countries population:", error);
            }
        },

        async fetchAnimeRecomendation(){
            try {
                const response = await fetch('https://api.jikan.moe/v4/recommendations/anime');
                const data = await response.json();
                this.animeRecomendations = data;
            } catch (error){
                console.error("Error fetching random manga:", error);
            }
        },

    }
}
</script>

<style scoped>
button {
  margin: 10px;
  padding: 10px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
}
</style>