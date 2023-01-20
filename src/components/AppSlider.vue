<script>
export default {
    data() {
        return {
            imgSlider: [
                'client-logos-1',
                'client-logos-2',
                'client-logos-3',
                'client-logos-4'
            ],
        }
    },

    methods: {
        getImagePath: function (imgpath) {
            return new URL(`../assets/img/${imgpath}.png`, import.meta.url).href
        },
    }
}

</script>

<template>
    <section class="slider">
        <div class="slider-container">
            <div class="slide">
                <img v-for="img in imgSlider" :src="getImagePath(img)" alt="">
            </div>
            <img class="shadow-left" src="../assets/img/image (1).png" alt="">
            <img class="shadow-right" src="../assets/img/image (1).png" alt="">
        </div>
    </section>
</template>

<style lang="scss" scoped>
section.slider {
    background-image: url(../assets/img/rgb-gradient-bar-for-logo-carrasel.jpg);
    padding: 1rem;
    display: flex;
    justify-content: center;

    div.slider-container {
        padding: .4rem;
        width: 50%;
        position: relative;

        div.slide {
            display: flex;
            justify-content: space-around;
            flex-direction: row;

            img {
                width: 22%;
            }

        }

        img.shadow-right {
            position: absolute;
            top: 0;
            right: 0;
            height: 100%;
        }

        img.shadow-left {
            position: absolute;
            top: 0;
            left: 0;
            height: 100%;
        }
    }
}
</style>