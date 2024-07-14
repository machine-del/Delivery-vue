<template>
    <div>
        <section class="banner">
            <div class="container">
                <div class="banner-item">
                    <h2 class="banner-item--title">
                        Онлайн-сервис<br>
                        доставки еды на дом
                    </h2>
                    <p class="banner-item--subtitle">
                        Блюда из любимого ресторана привезет курьер в перчатках, маске и с антисептиком
                    </p>
                </div>
            </div>
        </section>

        <section class="products">
            <div class="container">
                <div class="products-wrapper">
                    <router-link class="products-card" v-for="rest in goodArray" :key="rest.id"
                        :to="`/?id=${rest.id}`">
                        <div class="products-card__image">
                            <img :src="getUrl(rest.image)" alt="Sushi">
                        </div>

                        <div class="products-card__description">
                            <div class="products-card__description-row">
                                <h5 class="products-card__description--name">{{ rest.title }}</h5>
                            </div>
                            <div class="products-card__description-row">
                                <p class="products-card__description--text">{{ rest.description }}</p>
                            </div>
                            <div class="products-card__description-row">
                                <div class="products-card__description-controls">
                                    <button class="btn btn-primary">
                                        В корзину
                                        <img src="../assets/images/icons/shopping-cart--white.svg" alt="cart">
                                    </button>
                                    <span class="products-card__description-controls--price">{{ rest.price }} ₽</span>
                                </div>
                            </div>
                        </div>
                    </router-link>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
import { goodArray } from '../constants/rests'

const getUrl = (name) => {
    return new URL(`../assets/images/goods/${name}`, import.meta.url)
}
</script>
