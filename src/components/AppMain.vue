<script>
import AppMeetDoctors from './AppMeetDoctors.vue'
import AppService from './AppService.vue'
import AppAppointment from './AppAppointment.vue'

export default {
    components: {
        AppMeetDoctors,
        AppService,
        AppAppointment
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

            bigSquares: [
                {
                    title: 'Emergency Care',
                    img: 'wave-divider',
                    info: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque',
                    button: 'learn more',
                    color: 'class-1'
                },
                {
                    title: 'Expert Diagnostic',
                    img: 'wave-divider',
                    info: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque',
                    button: 'learn more',
                    color: 'class-2'
                },
                {
                    title: 'Superb rehabilitation',
                    img: 'wave-divider',
                    info: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque',
                    button: 'learn more',
                    color: 'class-3'
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
    <main>
        <section class="container">
            <h1>
                Welcome to Avada Health
            </h1>
            <p class="title">
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam
                rem
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
        <AppService />
        <section class="tour">
            <div class="text-tour">
                <img src="../assets/img/icon-7.png" alt="image">
                <h1>
                    our health service
                </h1>
                <hr>
                <p>
                    Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium,
                    totam
                    rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae
                </p>
                <img src="../assets/img/play-icon.png" alt="image">
            </div>
        </section>
        <section class="squares">
            <div v-for="square in bigSquares" class="square" :class="square.color">
                <h1>
                    {{ square.title }}
                </h1>
                <img :src="getImagePath(square.img)" alt="image">
                <p>
                    {{ square.info }}
                </p>
                <button :class="square.color">
                    {{ square.button }}
                </button>
            </div>
        </section>
        <AppAppointment />
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

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

section.tour {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 600px;
    background-image: url(../assets/img/paralax-bg-tour-facilities.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;

    div.text-tour {
        display: flex;
        flex-direction: column;
        align-items: center;
        color: $white;

        img {
            width: 60px;
        }

        h1 {
            text-transform: uppercase;
            font-weight: 300;
        }

        hr {
            background-color: $limed-spruce;
            width: 30%;
            margin: 1rem 0;
        }

        p {
            width: 50%;
            text-align: center;
            line-height: 1.8rem;
            padding-bottom: 1rem;
        }
    }
}

section.squares {
    display: flex;

    div.square {
        width: calc(100% / 3);
        padding: 2.5rem 1.6rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        color: $white;

        h1 {
            text-transform: uppercase;
            font-weight: 300;
            font-size: 1rem;
        }

        img {
            margin: .7rem 0;
        }

        button {
            text-transform: uppercase;
            width: 50%;
            color: $white;
            padding: .7rem .4rem;
            font-size: .8rem;
            border: 2px solid white;
        }

        p {
            text-align: center;
            line-height: 1.8rem;
            padding: .5rem 0;
        }
    }
}

.class-1 {
    background-color: $pelorous1;
}

.class-2 {
    background-color: $pelorous3;
}

.class-3 {
    background-color: $pelorous2;
}
</style>