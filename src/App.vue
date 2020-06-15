<template>
    <div id="app">
        <Header @changePage="scrollToComponent"></Header>
        <Main id="Main"></Main>
        <About id="About"></About>
        <Advantages id="Advantages"></Advantages>
        <Contacts id="Contacts"></Contacts>
        <Footer @changePage="scrollToComponent"></Footer>
    </div>
</template>

<script>
    import Header from './components/Header'
    import Main from './components/Main'
    import About from './components/About'
    import Advantages from './components/Advantages'
    import Contacts from './components/Contacts'
    import Footer from './components/Footer'
    import styles from './App.css'

    export default {
        name: 'App',
        components: {
            Header,
            Main,
            About,
            Advantages,
            Contacts,
            Footer
        },
        methods: {
            scrollToComponent(name) {
                document.getElementById(name).scrollIntoView();
            }
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        min-width: 370px;
        overflow: scroll;
    }
    body {
        margin: 0;
    }
</style>
