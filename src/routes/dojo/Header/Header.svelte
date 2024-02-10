<script>
    import Logo from '../assets/logo.svelte'
    import Text from './Text.svelte'
</script>

<header>
    <div/>
    <Text/>
    <Logo/>
</header>

<style>
    header {
        width: 338px;
        height: 100vh;

        display: flex;
        justify-content: space-between;
        flex-direction: column;
        align-items: center;

        position: sticky;
        left: 0;
        background: #fff;
        z-index: 1;
    }
</style>