<template>
    <!-- Start Works Area -->
    <section class="works-area" style="background: white">

        <b-modal ref="modal-zoom" :modal-class="modalZoom" static :return-focus="this.$parent" size="lg" hide-footer>
            <template #modal-title>
               {{modalProperties[index].title}}
            </template>
            <img :src="getImgUrl()" />
        </b-modal>

        <div class="works-slides" style="margin-top: 3rem">
            <carousel
                :autoplay = "true"
                :paginationEnabled = "false"
                :loop = "true"
                :autoplaySpeed = "true"
                :autoplayTimeout = "5000"
                :perPageCustom = "[[0, 1],[768, 2],[1200, 3], [1500, 4]]"
            >
                <slide>
                    <div class="single-works carousel-green-hover">
                        <img src="../resources/template5.png">
                        <a v-if="windowWidth > 767" @click="index = 0;$refs['modal-zoom'].show()" style="cursor: pointer;" class="icon"><feather type="zoom-in"></feather></a>

                        <div class="works-content">
                            <h3><a href="#">Rent-to-price & Cap Rate on autopilot</a></h3>
                            <p>Doorhacker calculates rent-to-price and cap rate</p>
                        </div>
                    </div>
                </slide>

                <slide>
                    <div class="single-works carousel-green-hover">
                        <img src="../resources/template4.png">
                        <a v-if="windowWidth > 767" @click="index = 1;$refs['modal-zoom'].show()" style="cursor: pointer;" class="icon"><feather type="zoom-in"></feather></a>

                        <div class="works-content">
                            <h3><a href="#">Export data to excel</a></h3>
                            <p>Conveniently share with others or use for additional analysis</p>
                        </div>
                    </div>
                </slide>

                <slide>
                    <div class="single-works carousel-green-hover">
                        <img src="../resources/template6.png" >
                        <a v-if="windowWidth > 767" @click="index = 2;$refs['modal-zoom'].show()" style="cursor: pointer;" class="icon"><feather type="zoom-in"></feather></a>

                        <div class="works-content">
                            <h3><a href="#">Focus only on best returns, prices or rents</a></h3>
                            <p>With sorting, no need to waste time on properties which don't meet your requirements</p>
                        </div>
                    </div>
                </slide>

                <slide>
                    <div class="single-works carousel-green-hover">
                        <img src="../resources/template1.png" >
                        <a v-if="windowWidth > 767" @click="index = 3;$refs['modal-zoom'].show()" style="cursor: pointer;" class="icon"><feather type="zoom-in"></feather></a>

                        <div class="works-content">
                            <h3><a href="#">Asking rent average for each investment property</a></h3>
                            <p>Calculated from Zillow asking rents in the neighborhood</p>
                        </div>
                    </div>
                </slide>
            </carousel>
        </div>
        <div class="shape4"><img src="../../../assets/img/shape4.svg"></div>
    </section>
    <!-- End Works Area -->
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';

export default {
    name: 'WorksTemplate',
    components: { Carousel, Slide },
    data() {
        return {
            modalZoom: ['modal-zoom'],
            windowWidth: window.innerWidth,
            index: 0,
            modalProperties: [
                {
                   title : "Rent-to-price & Cap Rate on autopilot",
                   img: "./template5.png"
                },
                {
                    title : "Export data to excel",
                    img: "./template4.png"
                },
                {
                    title : "Focus only on best returns, prices or rents",
                    img: "./template6.png"
                },
                {
                    title : "Asking rent average for each investment property",
                    img: "./template1.png"
                }

            ]
        }
    },
    mounted() {
        this.$nextTick(() => {
            window.addEventListener('resize', this.onResize);
        })
    },

    beforeDestroy() {
        window.removeEventListener('resize', this.onResize);
    },
    methods: {
        onResize() {
            this.windowWidth = window.innerWidth
        },
        getImgUrl() {
            var images = require.context('../resources/', false, /\.png$/)
            return images(this.modalProperties[this.index].img)
        }
    }
}
</script>
