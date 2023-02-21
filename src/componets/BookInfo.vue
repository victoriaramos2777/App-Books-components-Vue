<script>

export default {
 // props:["id", "title","autor", "releaseDate","isLiked"],
 //objeto que valide los props
    props:{
      id: {
        type: String,
        required: true,
      },
      title: {
        type: String,
        required: true,
      },
      author: {
        type: String,
        required: true,
      },
      releaseDate: {
        type: String,
        required: true,
      },
      isLiked: {
        type: String,
        required: false,
        default:"0",
        validator:function(value){
          return value === "1" || value === "0";
        },
      },
    },
  
  data() {
    return {
      detailsAreVisible: false,
      bookIsLiked:this.isLiked,
    };
  },
  methods: {
    toggletDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
    toggletFavorite(){
      if(this.bookIsLiked === "1"){
            this.bookIsLiked  = "0";
      }else{
        this.bookIsLiked = "1";
      }
    }
  },
};
</script>

<template>
  <li>
    <h2>
      {{title }} {{  bookIsLiked==="1" ? "(Liked)":"(Not Liked)" }}
    </h2>
    <button type="button" @click="toggletDetails">
      {{ detailsAreVisible ? "Hiden" : "Show" }}
    </button>
    <button type="button" @click="toggletFavorite">
      Togglet  Favorite
    </button>
    <ul v-if="detailsAreVisible">
      <li><strong>Autor: </strong>{{ author }}</li>
      <li><strong>Release Date: </strong>{{releaseDate }}</li>
    </ul>
  </li>
</template>
