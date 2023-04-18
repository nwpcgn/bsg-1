<script>
  //
</script>

<section class="page flex">

  <div class="grid-game container">
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
    <div class="pg-empty-placeholder" />
  </div>

  <div class="container py-4">
    <div>
      <div class="card">
        <h5 class="card-header">Featured</h5>
        <div class="card-body">
          <h5 class="card-title">Special title treatment</h5>
          <p class="card-text">
            With supporting text below as a natural lead-in to additional
            content.
          </p>
        </div>
      </div>
    </div>
  </div>

</section>

<style>
  .grid-game {
    --space: 0.5rem;
    --py: 1.5rem;
    --px: 1.5rem;
    flex: 1;
    
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr;
    grid-gap: var(--space);
    padding: calc(var(--py) * 0.5) calc(var(--px) * 0.5);
    position: relative;
/*     align-self: center;
    width: 100%;
    max-width: 600px; */
  }
  .pg-empty-placeholder {
    background-color: var(--bs-light);
    border: var(--bs-border-width) solid var(--bs-border-color);
    border-radius: var(--bs-border-radius);
    
  }
</style>
