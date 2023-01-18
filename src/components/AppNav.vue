<script>

export default {
    components: {

    }
}
</script>

<template>
    <ul>
        <li>
            Home
        </li>
        <li>
            About
        </li>
        <li>
            Departments
        </li>
        <li>
            Articles
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
</style>