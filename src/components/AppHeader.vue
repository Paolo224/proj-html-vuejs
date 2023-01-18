<script>
import AppNav from './AppNav.vue'

export default {
    components: {
        AppNav,
    }
}
</script>

<template>
    <header>
        <section class="nav-bar">
            <div class="logo">
                <img src="../assets/img/medical_logo_1x_light.png" alt="logo">
            </div>
            <div class="nav">
                <AppNav />
            </div>
        </section>
        <section class="header-more">
            <div class="text-more">
                <h1>
                    Caring <span>For Life</span>
                </h1>
                <p>
                    Kind words can be short and easy to speak, but their echoes are truly endless.
                    Avada Health focus on you as if it was our own family.
                </p>
                <button>
                    learn more
                </button>
            </div>
        </section>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

header {
    position: relative;
    width: 100%;
    height: 700px;
    background-image: url(../assets/img/header-image-homepage.jpg);
    background-size: cover;
    background-position: top;
    background-repeat: no-repeat;
    margin-bottom: 5rem;

    section.nav-bar {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 65px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem 3rem;

        div.logo {
            width: 15%;
            height: 100%;

            img {
                width: 100%;
            }
        }

        div.nav {
            width: 50%;
            height: 100%;
            display: flex;
            justify-content: space-between;
        }
    }

    section.header-more {
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;

        div.text-more {
            width: 900px;
            margin: 0 auto;
            color: $white;

            h1 {
                font-weight: 300;
                font-size: 4rem;

                span {
                    color: $pelorous1
                }
            }

            p {
                font-weight: 300;
                padding: 1rem 0 1.5rem 0;
                width: 60%;
                font-size: 1rem;
            }

            button {
                text-transform: uppercase;
                background-color: $pelorous1;
                width: 16%;
                color: $white;
                padding: .4rem;
                font-size: .8rem;
                border: none;
            }
        }
    }
}
</style>