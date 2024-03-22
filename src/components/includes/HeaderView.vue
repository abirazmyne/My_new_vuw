<template>
    <div class="preloader">
        <div class="preloader-inner">
            <div class="preloader-icon">
                <span></span>
                <span></span>
            </div>
        </div>
    </div>


    <header class="header navbar-area">



        <div class="header-middle">
            <div class="container">
                <div class="row align-items-center">
                    <div class="col-lg-3 col-md-3 col-7">

                        <router-link class="navbar-brand" to="/">
                            <img src="/website/assets/images/logo/vue.png" alt="Logo">
                        </router-link>

                    </div>
                    <div class="col-lg-5 col-md-7 d-xs-none">

                        <div class="main-menu-search">

                            <div class="navbar-search search-style-5">

                                <div class="search-input">
                                    <input type="text" placeholder="Search">
                                </div>
                                <div class="search-btn">
                                    <button><i class="lni lni-search-alt"></i></button>
                                </div>
                            </div>

                        </div>

                    </div>
                    <div class="col-lg-4 col-md-2 col-5">
                        <div class="middle-right-area">
                            <div class="nav-hotline">
                                <i class="lni lni-phone"></i>
                                <h3>Hotline:
                                    <span>(+100) 17973068**</span>
                                </h3>
                            </div>
                            <div class="navbar-cart">
                                <div class="wishlist">
                                    <a href="javascript:void(0)">
                                        <i class="lni lni-heart"></i>
                                        <span class="total-items">0</span>
                                    </a>
                                </div>
                                <div class="cart-items">
                                    <a href="javascript:void(0)" class="main-btn">
                                        <i class="lni lni-cart"></i>
                                        <span class="total-items">2</span>
                                    </a>

                                    <div class="shopping-item">
                                        <div class="dropdown-cart-header">
                                            <span>2 Items</span>
                                            <a href="cart.html">View Cart</a>
                                        </div>
                                        <ul class="shopping-list">
                                            <li>
                                                <a href="javascript:void(0)" class="remove" title="Remove this item"><i class="lni lni-close"></i></a>
                                                <div class="cart-img-head">
                                                    <a class="cart-img" href="product-details.html"><img src="/website/assets/images/header/cart-items/item1.jpg" alt="#"></a>
                                                </div>
                                                <div class="content">
                                                    <h4><a href="product-details.html">
                                                        Apple Watch Series 6</a></h4>
                                                    <p class="quantity">1x - <span class="amount">$99.00</span></p>
                                                </div>
                                            </li>
                                            <li>
                                                <a href="javascript:void(0)" class="remove" title="Remove this item"><i class="lni lni-close"></i></a>
                                                <div class="cart-img-head">
                                                    <a class="cart-img" href="product-details.html"><img src="/website/assets/images/header/cart-items/item2.jpg" alt="#"></a>
                                                </div>
                                                <div class="content">
                                                    <h4><a href="product-details.html">Wi-Fi Smart Camera</a></h4>
                                                    <p class="quantity">1x - <span class="amount">$35.00</span></p>
                                                </div>
                                            </li>
                                        </ul>
                                        <div class="bottom">
                                            <div class="total">
                                                <span>Total</span>
                                                <span class="total-amount">$134.00</span>
                                            </div>
                                            <div class="button">
                                                <a href="checkout.html" class="btn animate">Checkout</a>
                                            </div>
                                        </div>
                                    </div>

                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>


        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-8 col-md-6 col-12">
                    <div class="nav-inner">

                        <div class="mega-category-menu">
                            <span class="cat-button"><i class="lni lni-menu"></i>All Categories</span>
                            <ul class="sub-category">
                                <li v-for="(cotegory,key) in categories" :key="key">

                                    <router-link :to="{name: 'category', params:{id: cotegory.id}}">{{cotegory.name}}
                                        <i class="lni lni-chevron-right"></i>
                                    </router-link>

                                    <ul class="inner-sub-category">

                                        <li v-for="(subcategory, key1) in cotegory.sub_categories" :key="key1">
                                            <a href="product-grids.html">{{subcategory.name}}</a>
                                        </li>

                                    </ul>
                                </li>

                            </ul>
                        </div>


                        <nav class="navbar navbar-expand-lg">
                            <button class="navbar-toggler mobile-menu-btn" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                                <span class="toggler-icon"></span>
                                <span class="toggler-icon"></span>
                                <span class="toggler-icon"></span>
                            </button>
                            <div class="collapse navbar-collapse sub-menu-bar" id="navbarSupportedContent">
                                <ul id="nav" class="navbar-nav ms-auto">
                                    <li class="nav-item">
                                        <a href="index.html" class="active" aria-label="Toggle navigation"></a>
                                    </li>
                                </ul>
                            </div>
                        </nav>

                    </div>
                </div>
                <div class="col-lg-4 col-md-6 col-12">

                    <div class="nav-social">
                        <h5 class="title">Follow Us:</h5>
                        <ul>
                            <li>
                                <router-link to="/product-category"><i class="lni lni-facebook-filled"></i></router-link>
                            </li>
                            <li>
                                <router-link to="/product-detail"><i class="lni lni-twitter-original"></i></router-link>
                            </li>
                            <li>
                                <a href="javascript:void(0)"><i class="lni lni-instagram"></i></a>
                            </li>
                            <li>
                                <a href="javascript:void(0)"><i class="lni lni-skype"></i></a>
                            </li>
                        </ul>
                    </div>

                </div>
            </div>
        </div>

    </header>


</template>

<script>

    import axios from 'axios'


    export default {
        name: "HeaderView",
        data() {
            return {
                categories : [],
            }
        },
        created() {
            this.getAllCategory();
        },

        components: {},

        methods: {
            getAllCategory()
            {
                axios.get("http://localhost/my_shopgrid/public/api/get-all-category").then((response)=> {
                    this.categories = response.data;
                    console.log(this.categories);
                });
            }
        }
    }
</script>

<style scoped>

</style>