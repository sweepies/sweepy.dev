<script>
    import Fa from 'svelte-fa/src/fa.svelte'
    import { faGithub, faTwitter, faDiscord } from "@fortawesome/free-brands-svg-icons"
    import { faArrowDown, faEnvelope } from "@fortawesome/free-solid-svg-icons"
</script>

<div id="head" class="container">
    <div id="title">I'm Sweepy</div>
    <div id="arrow"><Fa
        icon={faArrowDown}
        style="margin-top: 3rem;"
    /></div>
    
</div>

<div class="center">
    <a href="https://github.com/sweepyoface"><Fa icon={faGithub} style="margin-right: 0.5rem;"/>github</a>
    <a href="https://twitter.com/sweepyoface"><Fa icon={faTwitter} style="margin-right: 0.5rem;"/>twitter</a>
    <div><Fa icon={faDiscord} style="margin-right: 0.5rem;"/>Sweepy#5624</div>
</div>

<img src="/wave.svg" alt="wave-shape">

<style lang="scss">
    :global {
        body {
            background-color: lightpink;
            // background-color: lightpink;
            font-family: "Gaegu", sans-serif;
            color: #313131;
        }

        a {
            color: #313131;
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }
    }

    .container {
        display: flex;
        justify-content: space-between;
        flex-direction: column;
    }
    #title {
        display: flex;
        font-size: 7rem;
    }
    #arrow {
        display: flex;
        font-size: 3rem;
    }

    #head {
        margin-top: 2rem;
        align-items: center;
    }

    .center {
        font-size: 2rem;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        margin-top: 5rem;
    }

    img {
        pointer-events: none;
        position: fixed;
        bottom: 0%;
    }
</style>
