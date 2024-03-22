<template>

    <section class="trending-product section">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="section-title">
                        <h2>All Product</h2>
                        <p>There are many variations of passages of Lorem Ipsum available, but the majority have
                            suffered alteration in some form.</p>
                    </div>
                </div>
            </div>
            <div class="row">
                <div v-for="(product, index) in products" :key="index" class="col-lg-3 col-md-6 col-12">

                    <div class="single-product">
                        <div class="product-image">
                            <img :src="product.image" alt="#">
                            <div class="button">
                                <a href="product-details.html" class="btn"><i class="lni lni-cart"></i> Add to Cart</a>
                            </div>
                        </div>
                        <div class="product-info">
                            <span class="category">{{product.category}}</span>
                            <h4 class="title">
                                <router-link :to="{name: 'product', params:{id: product.id}}" >{{product.short_name}}</router-link>
                            </h4>
                            <ul class="review">
                                <li><i class="lni lni-star-filled"></i></li>
                                <li><i class="lni lni-star-filled"></i></li>
                                <li><i class="lni lni-star-filled"></i></li>
                                <li><i class="lni lni-star-filled"></i></li>
                                <li><i class="lni lni-star"></i></li>
                                <li><span>4.0 Review(s)</span></li>
                            </ul>
                            <div class="price">
                                <span>{{product.selling_price}} <span class="text-danger">TK.</span></span>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </div>
    </section>


</template>

<script>
    import axios from "axios";

    export default {
        name: "AllProducts",
        data() {
            return {
                products : [],
            }
        },
        created() {
            this.getAllProduct();
        },

        components: {},

        methods: {
            getAllProduct()
            {
                axios.get("http://localhost/my_shopgrid/public/api/get-all-product").then((response)=> {
                    this.products = response.data;
                    console.log(this.products);
                });
            }
        }


    }
</script>

<style scoped>

</style>