<script>
export default {
    data() {
        return {
            servicesCards: [
                {
                    img: 'icon-11',
                    title: 'rehabilitation center',
                    info: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
                },
                {
                    img: 'icon-12',
                    title: 'dental implants',
                    info: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
                },
                {
                    img: 'icon-13',
                    title: 'medicine research',
                    info: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
                },
                {
                    img: 'icon-14',
                    title: 'blood bank',
                    info: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
                },
                {
                    img: 'icon-15',
                    title: 'pharmaceutical advice',
                    info: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
                },
                {
                    img: 'icon-16',
                    title: 'medical counseling',
                    info: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
                },
            ]
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
        <div v-for="card in servicesCards" class="service-card">
            <div class="img">
                <img :src="getImagePath(card.img)" alt="image">
            </div>
            <div class="service-info">
                <h3>{{ card.title.toUpperCase() }}</h3>
                <p>{{ card.info }}</p>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

section {
    display: flex;
    flex-wrap: wrap;
    padding: 3rem 0;
}

div.service-card {
    width: calc((100% / 3) - 1.4rem);
    margin: 1rem .7rem;
    text-align: center;

    div.service-info h3 {
        font-weight: 300;
        padding: .5rem 0;
    }

    div.service-info p {
        padding: 1rem 0;
        line-height: 1.4rem;
        text-align: justify;
    }
}
</style>