<script>
  export let src = '';
  export let size = '100px';
  export let background = 'transparent';
  export let opacityImg = '1'
</script>

<style>
  .circle-container {
    width: var(--size);
    height: var(--size);
    border-radius: 50%;
    background: var(--background);
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .circle-container img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    opacity: var(--opacity);
  }
</style>

<div class="circle-container" style="--size: {size}; --background: {background}; --opacity: {opacityImg}">
  <img src={src} alt="Circular Image" />
</div>
