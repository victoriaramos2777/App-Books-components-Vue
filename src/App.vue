<script>
export default {
  data() {
    return  {
      books: [
        {
          id: 1,
          title: "Dime Quién Soy I",
          autor: "Julia Navarro",
          releaseDate: "2010-03-05",
        },
        {
          id: 2,
          title: "Dime Quién Soy II",
          autor: "Julia Navarro",
          releaseDate: "2010-03-05",
        }, {
          id: 3,
          title: "Dime Quién Soy III",
          autor: "Julia Navarro",
          releaseDate: "2010-03-05",
        },
      ],
    };
  },
};
</script>

<template>
  <h1>Mis Libros</h1>
  <ul>
    <book-info
      id="1"
      title="Dime Quién Soy I "
      author="Julia Navarro"
      releaseDate="2010-03-05"
      is-liked="1"
    ></book-info>
    <book-info  id="2"
      title="Dime Quién Soy II "
      author="Julia Navarro"
      releaseDate="2010-03-05"
      is-liked="0"></book-info>
    <book-info  id="3"
      title="Dime Quién Soy III"
      author="Julia Navarro"
      releaseDate="2010-03-05"
      is-liked="1"></book-info>
  </ul>
</template>

<style>
h1 {
  color: rgb(238, 238, 130);
  background-color: black;
  width: 96%;
  text-align: center;
  padding: 5%;
}
ul {
  list-style: none;
  background-color: black;
  color: aqua;
  padding: 3%;
}
</style>
