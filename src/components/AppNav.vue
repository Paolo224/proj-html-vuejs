<script>

export default {
    data() {
        return {
            components: [
                'Home',
                'About',
                'Departments',
                'Article',
            ],
        }
    },
    components: {

    }
}
</script>

<template>
    <ul>
        <li v-for="component in components">
            {{ component }}
        </li>
    </ul>
    <button>
        make appointment
    </button>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

ul {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 100%;
    width: 60%;

    li {
        list-style-type: none;
        padding: .4rem;
        color: $white;
    }
}

button {
    text-transform: uppercase;
    background-color: $pelorous1;
    width: 35%;
    color: $white;
    padding: .4rem 1rem;
    font-size: .8rem;
    border: none;
}

button:hover {
    transition: all .3s ease-in-out;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    transform: scale(1.05);
    cursor: pointer;
}

li:hover {
    transition: all .3s ease-in-out;
    color: $pelorous3;
    cursor: pointer;
}
</style>