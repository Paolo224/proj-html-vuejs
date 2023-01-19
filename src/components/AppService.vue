<script>
import AppServiceCards from './AppService-cards.vue';

export default {
    components: {
        AppServiceCards,
    }
}
</script>

<template>
    <div class="service-title container">
        <img src="../assets/img/icon-6.png" alt="image">
        <h1>
            our health service
        </h1>
        <hr>
        <p>
            Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam
            rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae
        </p>
    </div>
    <AppServiceCards />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

div.service-title {
    display: flex;
    flex-direction: column;
    align-items: center;

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