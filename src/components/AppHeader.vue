<script>
export default {
    data() {
        return {
            activeItem: 0,
            menu: [
                {
                    label: 'Characters',
                    url: '#',
                    active: false
                },
                {
                    label: 'Comics',
                    url: '#',
                    active: true
                },
                {
                    label: 'Movies',
                    url: '#',
                    active: false
                },
                {
                    label: 'TV',
                    url: '#',
                    active: false
                },
                {
                    label: 'Games',
                    url: '#',
                    active: false
                },
                {
                    label: 'Video',
                    url: '#',
                    active: false
                },
                {
                    label: 'Fans',
                    url: '#',
                    active: false
                },
                {
                    label: 'News',
                    url: '#',
                    active: false
                },
                {
                    label: 'Shop',
                    url: '#',
                    active: false
                },
            ]
        }
    },
    methods: {
        selectedItem(index) {
            this.activeItem = index
            }
    }
}
</script>

<template lang="">
  <header>
    <a href="/" class="logo">
        <img src="../assets/img/dc-logo.png" alt="logo-dc">
    </a>
    <nav>
        <ul>
            <li v-for="(item, index) in menu" :key="index" @click="selectedItem(index)" :class="(activeItem === index) ? 'active' : ''">
                <a :href="item.url">
                    {{ item.label }}
                </a>
            </li>
        </ul>
       </nav>
  </header>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

  header{
    text-align: center;
    align-items: center;
    margin-top: 1em;
    @include justify_around;

    ul {
        list-style: none;
        margin: 2rem 1rem;
        @include justify_center;

        .active {
            color: $primary;
            border-bottom: 3px solid $primary;
            padding-bottom: 2em;
        }

        li a {
            padding: 1em;
            font-size: 16px;
            text-decoration: none;
        }
  }
}
</style>