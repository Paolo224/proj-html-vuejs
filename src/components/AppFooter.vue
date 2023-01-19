<script>

export default {
    components: {

    },
    data() {
        return {
            medicalDepartment: [
                'Cardiology',
                'Pediatrics',
                'Diabetes Care',
                'Pre-natel Care',
                'Ultrasound Echocardiogram',
            ],
        }
    },
}
</script>

<template>
    <footer>
        <div class="section">
            <div class="logo">
                <img src="../assets/img/medical_logo_1x_dark.png" alt="image">
            </div>
            <p>
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolemue launti totam aperiam,
                eaque ipsa quae abillo. Invente veriatis et quasi architecto beatae luptatem accusantium,
                remaperiamsiat. Voluptatem accusest etsium doloremque laudaien. Lorem ipsum sits dolores ets unser.
            </p>
            <hr>
            <h4>
                learn more about us
            </h4>
            <div class="socials">
                <div class="social">
                    <i class="fa-brands fa-facebook-f"></i>
                </div>
                <div class="social">
                    <i class="fa-brands fa-twitter"></i>
                </div>
                <div class="social">
                    <i class="fa-brands fa-youtube"></i>
                </div>
                <div class="social">
                    <i class="fa-brands fa-instagram"></i>
                </div>
            </div>
        </div>
        <div class="section">
            <h4>contact information</h4>
            <hr class="hr-small-green">
            <div class="adress-call">
                <div class="adress">
                    <i class="fa-solid fa-location-dot"></i>
                    121 King Street, London United Kingdom
                </div>
                <div class="call">
                    <i class="fa-solid fa-phone-flip"></i>
                    1.800.458.556
                </div>
            </div>
        </div>
        <div class="section">
            <h4>medical departments</h4>
            <hr class="hr-small-green">
            <div v-for="department in medicalDepartment" class="department">
                <div class="blue-point">
                    <i class="fa-solid fa-chevron-right"></i>
                </div>
                <div>
                    {{ department }}
                </div>
            </div>
            <button>view our departments</button>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

footer {
    padding: 2rem;
    display: flex;

    div.section {
        width: calc(100% / 3);
        padding: .8rem;

        div.logo {
            width: 50%;

            img {
                width: 100%;
            }
        }

        p {
            font-size: 0.8rem;
            line-height: 1.8rem;
            padding: .8rem 0;
        }

        hr {
            margin-top: .6rem;
        }

        hr.hr-small-green {
            background-color: $pelorous1;
            height: 5px;
            width: 10%;
            border: none;
            margin-bottom: 2rem;
        }

        h4 {
            text-transform: uppercase;
            font-weight: 300;
            margin-bottom: 2rem;
        }

        div.socials {
            display: flex;

            div.social {
                width: 25px;
                height: 25px;
                display: flex;
                align-items: center;
                justify-content: center;
                color: $white;
                margin-right: .6rem;
                background-color: $pelorous1;
                border-radius: .2rem;
            }
        }

        div.adress-call {
            display: flex;
            flex-direction: column;

            div.adress {
                padding: .5rem 0;
            }

            div.call {
                padding: .5rem 0;
            }

            i {
                color: $pelorous1;
                padding-right: .8rem;
            }
        }

        div.department {
            display: flex;
            margin: .4rem 0;

            div.blue-point {
                width: 20px;
                height: 20px;
                border-radius: 50%;
                display: flex;
                justify-content: center;
                align-items: center;
                background-color: $pelorous1;
                font-size: 0.5rem;
                color: $white;
                margin-right: .6rem;
            }
        }

        button {
            text-transform: uppercase;
            width: 70%;
            color: grey;
            padding: .7rem .4rem;
            font-size: .8rem;
            border: 2px solid grey;
            background-color: $white;
            margin-top: 2rem;
        }
    }
}
</style>