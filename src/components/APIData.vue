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
