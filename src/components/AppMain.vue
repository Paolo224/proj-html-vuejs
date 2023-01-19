<script>
import AppMeetDoctors from './AppMeetDoctors.vue'

export default {
    components: {
        AppMeetDoctors,
    },

    data() {
        return {
            cardsMain: [
                {
                    img: 'icon-1',
                    title: 'same day appointments',
                    info: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium'
                },
                {
                    img: 'icon-2',
                    title: 'world class facilities',
                    info: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium'
                },
                {
                    img: 'icon-3',
                    title: 'expert doctors',
                    info: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium'
                },
                {
                    img: 'icon-4',
                    title: 'complementary therapies',
                    info: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium'
                },
            ],
        }
    },

    methods: {
        getImagePath: function (imgpath) {
            return new URL(`../assets/img/${imgpath}.png`, import.meta.url).href
        },
    },
}
</script>

<template>
    <section class="container">
        <h1>
            Welcome to Avada Health
        </h1>
        <p class="title">
            Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem
            aperiam, eaque ipsa quae ab illo
        </p>
        <section class="cards">
            <div v-for="card in cardsMain" class="card">
                <img :src="getImagePath(card.img)" alt="">
                <h4>{{ card.title }}</h4>
                <h5>
                    {{ card.info }}
                </h5>
            </div>
        </section>
    </section>
    <AppMeetDoctors />
</template>

<style lang="scss" scoped>
h1 {
    text-align: center;
    font-weight: 300;
}

p.title {
    text-align: center;
    padding: .5rem 4.5rem;
    line-height: 1.8rem;
}

section.cards {
    display: flex;

    div.card {
        width: calc(100% / 4);
        padding: .8rem;
        margin: 2rem 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        justify-content: space-between;

        h4 {
            margin: .6rem 0;
            font-weight: 500;
            text-transform: uppercase;
        }

        h5 {
            font-weight: 300;
            text-align: justify;
            line-height: 1.3rem;
        }
    }
}
</style>