<script>
  import { onMount } from "svelte";
  // import Glide from "@glidejs/glide";
  import Chevron from "./../components/Chevron.svelte";
  export let list = [],
    Component,
    autoplay = 0,
    currentId = 0;

  onMount(() => {
    let glide = new Glide(".glide");
    glide.on("run.after", e => {
      if (glide.index >= 0) {
        currentId = glide.index;
      }
    });
    glide.mount().update({
      type: "slider",
      perView: 1,
      startAt: 0,
      autoplay
    });
  });
</script>

<style>
  .list {
    /* max-height: 350px; */
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
  }
  .list > img {
    height: 650px;
    width: 500px;
  }
</style>

<div class="slider-container">
  <div class="glide">
    <div class="glide__track" data-glide-el="track">
      <div class="glide__slides list">
        <img src="./src/images/KRITI.jpg" alt="cert1" />
        <img src="./src/images/kriti2.png" alt="cert2" />
        <img src="./src/images/kriti3.png" alt="cert3" />
        <img src="./src/images/kriti4.png" alt="cert4" />
        <img src="./src/images/1.png" alt="cert4" />
        <img src="./src/images/2.png" alt="cert4" />
        <img src="./src/images/3.png" alt="cert4" />
        <img src="./src/images/4.png" alt="cert4" />
        <img src="./src/images/5.png" alt="cert4" />
        <img src="./src/images/6.png" alt="cert4" />
        <img src="./src/images/7.png" alt="cert4" />
      </div>
    </div>
    <div class="glide__bullets">
      <li
        class="glide__bullet {0 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={0} />
      <li
        class="glide__bullet {1 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={1} />
      <li
        class="glide__bullet {2 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={2} />
      <li
        class="glide__bullet {3 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={3} />
      <li
        class="glide__bullet {4 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={4} />
      <li
        class="glide__bullet {5 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={5} />
      <li
        class="glide__bullet {6 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={6} />
      <li
        class="glide__bullet {7 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={7} />
      <li
        class="glide__bullet {8 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={8} />
      <li
        class="glide__bullet {9 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={9} />
      <li
        class="glide__bullet {10 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={10} />
      <li
        class="glide__bullet {11 === currentId ? 'glide__bullet--active' : ''}"
        data-glide-dir={11} />
    </div>
  </div>
</div>
