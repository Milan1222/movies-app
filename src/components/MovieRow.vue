<template>
    <tr>
        <td>{{movie.id}}</td>
        <td>{{movie.title}}</td>
        <td>{{movie.director}}</td>
        <img :src="movie.imageUrl">
        <td>{{movie.releaseDate}}</td>
        <td>{{movie.genre}}</td>
        <td>{{movie.duration}}</td>
    </tr>
</template>

<script>
export default {
    props: [
        'movie'
    ]
}
</script>

<style>

</style>
