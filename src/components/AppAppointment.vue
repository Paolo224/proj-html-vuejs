<script>
export default {

}
</script>

<template>
    <section class="appointment">
        <div class="appointment-text container">
            <h1>
                make an appointment
            </h1>
            <hr>
            <p>
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium,
                totam
                rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae
            </p>
        </div>
        <div class="appointment-form container">
            <input class="input" type="text" placeholder="Name*">
            <input class="input" type="email" placeholder="Email*">
            <input class="input" type="text" placeholder="Phone Number*">
            <input class="input" type="date" placeholder="Appointment Date*">
        </div>
        <div class="text-area container">
            <textarea placeholder="How can we help?*"></textarea>
        </div>
        <div class="button container">
            <button>make an appointment</button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

section.appointment {
    display: flex;
    justify-content: center;
    flex-direction: column;
    width: 100%;
    height: 600px;
    background-image: url(../assets/img/make-an-appointment.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;

    div.appointment-text {
        display: flex;
        flex-direction: column;
        align-items: center;
        color: $white;

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

    div.appointment-form {
        padding: .3rem;
        padding-bottom: .15rem;

        input.input {
            border: 2px solid grey;
            padding: .8rem;
            width: calc((100% / 2) - 1rem);
            margin: .5rem;
            background-color: transparent;
            color: grey;
        }
    }

    div.text-area {
        padding: .3rem;
        padding-top: .15rem;
        display: flex;
        justify-content: center;
        align-items: center;

        textarea {
            border: 2px solid grey;
            padding: .8rem;
            margin: .5rem;
            width: 100%;
            background-color: transparent;
            color: grey;
        }
    }

    div.button {
        padding: .98rem;

        button {
            width: 100%;
            padding: .8rem;
            color: $white;
            background-color: $pelorous3;
            text-transform: uppercase;
            font-size: 1.4rem;
            font-weight: 300;
        }
    }
}
</style>