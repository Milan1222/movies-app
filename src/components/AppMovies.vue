<template>
    <div>
          <table border="1" v-for="movie in movies" :key="movie.id">
            <thead>
                <th>Id:</th>
                <th>Title:</th>
                <th>Director:</th>
                <th>ImageURL:</th>
                <th>Release Date:</th>
                <th>Genre:</th>
                <th>Duration:</th>
            </thead>
            <tbody>
                <movie-row :movie="movie"/>
            </tbody>
        </table>
    </div>
</template>

<script>
import MovieRow from './MovieRow.vue'
import Movies from '../Services/Movies'

export default {


    beforeRouteEnter(to, from, next) {
        Movies.getAll()
            .then(r => {
                next((vm) => {
                    console.log('awsda')
                    vm.movies = r.data
                })
            })
    },
    data() {
        return {
            movies: []
        }
    },

    components: { 
        MovieRow
    }
}
</script>

<style scoped>
    table {
        width: 100%;
        border: 1px;
    }

</style>
