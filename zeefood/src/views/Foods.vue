<template>
    <div>
        <NavItem/>
        <div class="container">
            <div class="row">
                <div class="col">
                    <h2>Daftar <Strong>Menu</Strong></h2>
                </div>
            </div>
            
            <div class="row mt-3">
                <div class="col">
                    <div class="input-group mb-3">
                        <div class="input-group-prepend">
                            <span class="input-group-text" id="basic-addon1">
                            @
                            </span>
                        </div>
                        <!--<input type="text" class="form-control" placeholder="Username" arial-label="Username" aria-describedby="basic-addon1"></input>-->
                    </div>
                </div>
            </div>
            
            <div class="row mb-4">
                <div class="col-md-4 mt-d-4" v-for="product in products" :key="product.id">
                    <CardProduct :product="product"/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
// @ is an alias to /src
import NavItem from '@/components/NavItem.vue'
import CardProduct from '@/components/CardProduct.vue';
import axios from 'axios';

export default {
    name : 'FoodS',
    components: {
        NavItem,
        CardProduct,
    },
    data() {
        return {
            products: []
        };
    },
    methods: {
        setProducts(data) {
            this.products = data
        },
    },
    mounted() {
        axios
        .get("http://localhost:3000/products")
        .then((response) => this.setProducts(response.data))
        .catch((error) => console.log(error))
    },
}
</script>

<style>

</style>