<script>
export default {
    data() {
        return{
          
            books:[
             {
                id:1,
                title: "Dime Quién Soy ",
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
    <book-info></book-info>
    <book-info></book-info>
    <book-info></book-info>
  </ul>
</template>

<style>
h1{
    color:rgb(238, 238, 130);
    background-color: black;
    width: 30%;
    text-align: center;
}
ul{
  list-style: none;
  background-color: black;
  color: aqua;
  width: 30%;
}
</style>
