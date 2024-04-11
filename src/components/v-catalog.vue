<template>
  <div class="v-catalog">
    <vCatalogItem v-for="product in products" :key="product.article" :product_data ='product' @hi ="showArticleFromChild" />
  </div>
</template>

<script>
import vCatalogItem from "./v-catalog-item.vue";

export default {
    name:"v-catalog",
    components:{
        vCatalogItem
        },
    props: {},
    data(){
        return {
            products: [
        {
            image: "1.png",
            name: "Analyst",
            price: 2100,
            imgURL: "https://loremflickr.com/640/360/1",
            article: "T1",
            available: true,
            category: "it products",
            quantity: 0,
            about: "Hi i'm an Analyst! Nice to meet you!"
        },
        {
            image: "2.png",
            name: "Designer",
            price: 3150,
            imgURL: "https://loremflickr.com/640/360/2",
            article: "T2",
            available: true,
            category: "it products",
            quantity: 0,
            about: "Hey my friend! Nice to meet you!"
        },
        {
            image: "3.png",
            name: "Marketer",
            price: 4200,
            imgURL: "https://loremflickr.com/640/360/3",
            article: "T3",
            available: false,
            category: "it products",
            quantity: 0,
            about: "Hello! How have you been?"
        },
        {
            image: "4.png",
            name: "Developer",
            price: 5300,
            imgURL: "https://loremflickr.com/640/360/4",
            article: "T4",
            available: true,
            category: "it products",
            quantity: 0,
            about: "Nice to meet you! What about Vue?"
        },
        {
            image: "5.png",
            name: "Business Accelerator",
            price: 6500,
            imgURL: "https://loremflickr.com/640/360/5",
            article: "T5",
            available: false,
            category: "it products",
            quantity: 0,
            about: "Hey! We'll solve any problems!"
        },
        {
            image: "6.png",
            name: "Engineer",
            price: 8700,
            imgURL: "https://loremflickr.com/640/360/6",
            article: "T6",
            available: true,
            category: "it products",
            quantity: 0,
            about: "Hi! I've many solutions!"
        }
    ]
        };
    },
    computed: {},
    methods: {
        showArticleFromChild(data){
            console.log(data)
        }
    }
    

}
</script>

<style>
.v-catalog{
   display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    align-items: center; 
}
  
</style>