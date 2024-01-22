<script>
    import { onMount } from "svelte";

onMount(() => {
    function progressBarScroll() {
        let winScroll = document.body.scrollTop || document.documentElement.scrollTop,
            height = document.documentElement.scrollHeight - document.documentElement.clientHeight,
            scrolled = (winScroll / height) * 100;
        document.getElementById("progress-bar").style.width = scrolled + "%";
    }

    window.onscroll = function () {
    progressBarScroll();
    };
});
</script>

<div id="progress-bar"></div>

<style>
    #progress-bar {
        min-height: 5px;
        background-color: #D21404;
        position: sticky;
        top: 0px;
        z-index: 2;
        border-radius: 0px 0px 2px 2px
    }
</style>