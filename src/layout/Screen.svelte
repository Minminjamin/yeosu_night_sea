<script>
</script>

<style>
    main {
        width: 100%;
        height: 100%;
        background: #6f67ff;
        color: #fff;
    }

    .day {
        background: linear-gradient(to bottom, #00c1ff, #d1f3fd);
        position: relative;
        position: relative;
        overflow: hidden;
        transform: translate3d(0, 0, 0);
    }

    .sea {
        width: 100%;
        height: 30%;
        border: solid 1px black;
        position: fixed;
        bottom: 0;
        /* overflow: hidden; */
    }

    .waveContainer {
        width: 100%;
        height: 100%;
        border: solid 1px orange;
        background: none;
        /* border-radius: 5px;
        box-shadow: 0 2px 30px rgba(black, 0.2);
        background: lighten(#f0f4c3, 10%);
        position: relative;
        overflow: hidden;
        transform: translate3d(0, 0, 0); */
    }

    .wave {
        position: absolute;
        background: blue;
        width: 100vw;
        border-radius: 50%;
        opacity: 0.9;
        animation: drift 7000ms infinite linear;
    }

    .wave.-one {
        left: -45%;
        border-radius: 40%;
        height: 98vw;
        opacity: 0.8;
    }

    .wave.-two {
        height: 95vw;
        left: -25%;
    }

    .wave.-three {
        border-radius: 60%;
        height: 90vw;
        opacity: 0.7;
    }

    .wave.-four {
        height: 95vw;
        left: 20%;
        opacity: 0.8;
    }

    .wave.-five {
        animation: drift 90000ms infinite linear;
        height: 95vw;
        left: 40%;
        border-radius: 38%;
    }

    @keyframes drift {
        from {
            transform: rotate(0deg);
        }
        to {
            transform: rotate(360deg);
        }
    }

    /* 갈매기 or 구름 애니메이션ㄴ */
</style>

<main class="day">
    <article class="sea">
        <section class="waveContainer">
            <figure class="wave -one" />
            <figure class="wave -two" />
            <figure class="wave -three" />
            <figure class="wave -four" />
            <figure class="wave -five" />
        </section>
    </article>
</main>
