<script>

export default {
    components: {

    },

    data() {
        return {
            doctorsCards: [
                {
                    img: 'doctor-1',
                    name: 'jon snow',
                    role: 'Anesthesiologist',
                    info: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque',
                },
                {
                    img: 'doctor-2',
                    name: 'tony stark',
                    role: 'Cardiologist',
                    info: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque',
                },
                {
                    img: 'doctor-3',
                    name: 'anna smith',
                    role: 'Nurse Practitioner',
                    info: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque',
                },
            ],
        }
    },

    methods: {
        getImagePath: function (imgpath) {
            return new URL(`../assets/img/${imgpath}.jpg`, import.meta.url).href
        },
    },
}
</script>

<template>
    <section class="container">
        <div v-for="card in doctorsCards" class="doctor-card">
            <div class="img">
                <img :src="getImagePath(card.img)" alt="image">
            </div>
            <div class="doctor-info">
                <h3>{{ card.name.toUpperCase() }}</h3>
                <h5>{{ card.role }}</h5>
                <p>{{ card.info }}</p>
                <div class="socials">
                    <div class="social">
                        <i class="fa-brands fa-facebook-f"></i>
                    </div>
                    <div class="social">
                        <i class="fa-brands fa-twitter"></i>
                    </div>
                    <div class="social">
                        <i class="fa-brands fa-instagram"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

section {
    display: flex;
}

div.doctor-card {
    width: calc((100% / 3) - 1rem);
    margin: 1rem .5rem;
    background-color: $white;

    div.img img {
        width: 100%;
    }

    div.doctor-info {
        padding: 1.5rem;

        h3 {
            font-weight: 300;
        }

        h5 {
            padding: 1rem 0;
        }

        p {
            padding: 1rem 0;
            line-height: 1.4rem;
        }

        div.socials {
            display: flex;
        }

        div.social {
            width: 25px;
            height: 25px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: $white;
            margin: 0 .5rem;
            background-color: $pelorous1;
            border-radius: .2rem;
        }
    }
}
</style>