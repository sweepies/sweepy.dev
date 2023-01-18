<script>
    import Fa from "svelte-fa/src/fa.svelte";
    import {
        faGithub,
        faTwitter,
        faDiscord,
    } from "@fortawesome/free-brands-svg-icons";
    import { faClipboard } from "@fortawesome/free-solid-svg-icons";
    import Clipboard from "svelte-clipboard";

    let copied
</script>

<div class="flex flex-col gap-y-16 items-center justify-center">
    <div class="text-center mt-32 text-7xl md:text-8xl lg:text-9xl">I'm Sweepy</div>

    <div class="flex flex-row gap-x-6 text-6xl md:text-7xl lg:text-8xl">
        <a href="https://github.com/sweepyoface"><Fa icon={faGithub} /></a>
        <a href="https://twitter.com/sweepy_twt"><Fa icon={faTwitter} /></a>

        <Clipboard
            text="Sweepy#5624"
            let:copy
            on:copy={() => {
                if (copied) return

                copied = true

                setTimeout(() => {
                    copied = false
                }, 1000)
            }}
        >
        <span class="cursor-pointer" on:click={copy}>
            {#if !copied}
                <Fa icon={faDiscord} />
            {:else}
                <Fa icon={faClipboard} />
            {/if}
        </span>
        </Clipboard>
    </div>
</div>

<div class="absolute bottom-0 left-0 w-full overflow-hidden">
    <svg
        class="relative block h-64"
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1200 120"
        preserveAspectRatio="none"
    >
        <path
            d="M985.66,92.83C906.67,72,823.78,31,743.84,14.19c-82.26-17.34-168.06-16.33-250.45.39-57.84,11.73-114,31.07-172,41.86A600.21,600.21,0,0,1,0,27.35V120H1200V95.8C1132.19,118.92,1055.71,111.31,985.66,92.83Z"
            style="fill: #313131;"
        />
    </svg>
</div>

<style lang="scss">
</style>
