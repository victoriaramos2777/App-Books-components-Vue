<script>
export default {
    data() {
        return{
            detailsAreVisible:false,
            book: {
                id:1,
                title: "Dime Quién Soy",
                autor: "Julia Navarro",
                releaseDate: "2010-03-05",
             },
           
        };

    },
    methods:{
      toggletDetails(){
       this.detailsAreVisible  = !this.detailsAreVisible;
      }
    }
};
</script>

<template>
<li>
    <h2>
        {{ book.title }}
    </h2>
    <button type="button" @click="toggletDetails">
    {{ detailsAreVisible ? "Hiden": "Show"}}
    </button>
    <ul v-if ="detailsAreVisible">
        <li><strong>Autor</strong>{{ book.autor }}</li>
        <li><strong>Release Date</strong>{{ book.releaseDate }}</li>
    </ul>
</li>
</template>