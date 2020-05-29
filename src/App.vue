<template>
    <div id="app">
        <Header></Header>
        <Main></Main>
        <About></About>
        <Advantages></Advantages>
        <Contacts></Contacts>
        <Footer></Footer>
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
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
    }
    body {
        margin: 0;
    }
</style>
