<script>
  let run;
  const toggle = () => {
    run = !run;
  };
  const handleAniEnd = () => {
    run = false;
  };
</script>

<section class="page flex">
  <div class="container aligner">
    <article class="game-monitor rounded">
      {#if run}
        <figure class="aiko-move" on:animationend={handleAniEnd}>
          <div class:run id="aiko" />
        </figure>
      {/if}
    </article>
  </div>

  <div class="container py-4">
    <div>
      <div class="card">
        <h5 class="card-header">Featured</h5>
        <div class="card-body">
          <h5 class="card-title">Special title treatment</h5>
          <p class="card-text">
            <button on:click={toggle} type="button" class="btn btn-primary"
              >Run</button
            >
          </p>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  figure {
    margin-bottom: 0;
  }
  .game-monitor {
    width: 100%;
    aspect-ratio: 16/9;
    max-width: var(--maxw, 820px);
    margin: auto;
    position: relative;
    overflow: hidden;
    background-image: url("./img/s2/1/8.jpg");
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
  }
  #aiko {
    width: 130px;
    height: 180px;
    background: url("./img/aiko.png");
  }
  .aiko-move {
    position: absolute;
    display: inline-block;
    z-index: 10;
    bottom: 0;
    left: 0;
    animation: aikomove 2.5s forwards linear;
  }

  @keyframes aikomove {
    0% {
      left: -130px;
    }

    100% {
      left: 100vw;
    }
  }

  #aiko.run,
  #aiko:hover {
    /* -webkit-animation: animAiko 0.8s steps(10) forwards; */
    -webkit-animation: animAiko 0.8s steps(10) infinite;
  }
  @-webkit-keyframes animAiko {
    0% {
      background-position-x: 0;
    }

    100% {
      background-position-x: -1300px;
    }
  }

  
  /* -webkit-animation: play .8s steps(10) infinite;
       -moz-animation: play .8s steps(10) infinite;
        -ms-animation: play .8s steps(10) infinite;
         -o-animation: play .8s steps(10) infinite;
            animation: play .8s steps(10) infinite; */
</style>
