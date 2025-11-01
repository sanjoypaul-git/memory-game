<script>
  let flipped = $state(false)
</script>

<button
  class="card {flipped ? 'flipped' : ''}"
  onclick={() => flipped = !flipped}
>
  <div class="front">🍒</div>
  <div class="back">
    <div class="pattern"></div>
  </div>
</button>

<style lang="scss">
  .card {
    width: 100px;
    height: 130px;
    position: relative;
    cursor: pointer;
    user-select: none;
    /* background: #1C1F2A; */
    border-radius: 5px;
    border: none;
    transform: rotateY(180deg);
    transition: transform 0.5s;
    transform-style: preserve-3d;
    .front,
    .back {
      display: flex;
      align-items: center;
      justify-content: center;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border: 1px solid gray;
      border-radius: inherit;
      backface-visibility: hidden;
      box-sizing: border-box;
    }
    .front {
      background: #fff;
      font-size: 30px;
    }
    .back {
      transform: rotateY(180deg);
      padding: 5px;
      .pattern {
        width: 100%;
        height: 100%;
        border-radius: 5px;
        background-color: #def;
        background-image: radial-gradient(closest-side, transparent 98%, rgba(0,0,0,.3) 99%),
        radial-gradient(closest-side, transparent 98%, rgba(0,0,0,.3) 99%);
        background-size: 20px 20px;
        background-position: 0 0, 10px 10px;
      }
    }
    &.flipped {
      transform: rotateY(0);
    }
  }
</style>
