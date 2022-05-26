<template>
  <h2 v-for="(name, index) in names" :key="name">{{index}} {{name}}</h2>
  <h2 v-for="name in fullNames" :key="name.first">{{name.first}} {{name.last}}</h2>

<br>
<div v-for="actor in actors" :key="actor.name">
  <h2>{{actor.name}}</h2>
  <h3 v-for="movie in actor.movies" :key="movie">{{movie}}</h3>
</div>

<h2 v-for="(value, key, index) in myInfo" :key="value">{{index}} :- {{key}} :- {{value}}</h2>

<template v-for="name in names" :key="name">
<h2>{{name}}</h2>
<hr />

</template>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{ 
      names:['vijay', 'gokul','prajwal','nithin'],
      fullNames:[ 
        { first: 'vijay', last: 'mane'},
        { first: 'gokul', last: 'M K'},
        { first: 'prajwal', last: 'something'},
        { first: 'nithin', last: 'savkar'}
      ],
      actors:[ 
        {
          name: "1. Navrang theatre",
          movies: ['Badava Rascal','Yuvarathnaa'],
        },
        {
          name: "2. Balaji theatre",
          movies: ['KGF part-2', 'Ek Love Ya']
        },
      ],
      myInfo: {
        name: 'Vijaykumar',
        channel: 'Codevolution',
        course: 'vue 3'
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
