<script>
  import "$lib/reset.css";
</script>

<header>
  <h1>dodododo</h1>
</header>

<slot/>

<style>
  header {
    position: relative;
    left: 50%;
    translate: -50% 0%;

    width: 80dvw;
    padding: 0rem 1rem;

    @media screen and (max-width: 805px) {
      text-align: center;
    }
  }
</style>