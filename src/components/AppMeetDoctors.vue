<script>
import AppDoctorsCards from './AppDoctorsCards.vue'

export default {
    components: {
        AppDoctorsCards,
    }
}
</script>

<template>
    <section class="bg-gray">
        <div class="meet-doctors-title container">
            <img src="../assets/img/icon-5.png" alt="image">
            <h1>
                meet our doctors
            </h1>
            <hr>
            <p>
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam
                rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae
            </p>
        </div>
        <AppDoctorsCards />
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

section.bg-gray {
    background-color: $french-gray;
    padding: 3rem;

    div.meet-doctors-title {
        display: flex;
        flex-direction: column;
        align-items: center;
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
        width: 70%;
        text-align: center;
        line-height: 1.8rem;
    }
}
</style>