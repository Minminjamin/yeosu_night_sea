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
        overflow: hidden;
        transform: translate3d(0, 0, 0);
    }

    .night {
        position: relative;
        overflow: hidden;
        background: linear-gradient(to bottom, #22207c, #632f90);
        position: relative;
    }

    /* .night::before {
        content: "";
        position: absolute;
        top: 45%;
        width: 100%;
        height: 2%;
        opacity: 0.01;
        background: white;
        box-shadow: 2px 0px white inset;
    } */

    .sea {
        width: 100%;
        height: 30%;
        position: fixed;
        bottom: 0;
    }

    .waveContainer {
        width: 100%;
        height: 100%;
        background: none;
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

<main class="night">
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
