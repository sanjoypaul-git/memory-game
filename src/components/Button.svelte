<script>
  let props = $props()
</script>

<button class="btn" {...props}>
  {@render props.children?.()}
</button>

<style>
  .btn {
    background: #65B891;
    border: none;
    padding: 10px 35px;
    color: #fff;
    font-size: 14px;
    font-weight: bold;
    position: relative;
    border-radius: 5px;
    cursor: pointer;
    transform-style: preserve-3d;
    transition: transform 0.3s cubic-bezier(0, 0, 0.58, 1),
      background 0.3s cubic-bezier(0, 0, 0.58, 1);
    &::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      background: #65B891;
      height: 100%;
      width: 100%;
      border-radius: inherit;
      transform: translate3d(0, 8px, -16px);
      transition: transform 0.3s cubic-bezier(0, 0, 0.58, 1);
    }
    &::after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      background: rgba(0, 0, 0, 0.25);
      filter: blur(4px);
      height: 100%;
      width: 100%;
      border-radius: inherit;
      transform: translate3d(0, 12px, -16px);
      transition: transform 0.3s cubic-bezier(0, 0, 0.58, 1);
    }
    &:hover {
      transform: translateY(-4px);
    }
    &:hover::before {
      transform: translate3d(0, 12px, -16px);
    }
    &:hover::after {
      transform: translate3d(0, 16px, -16px);
    }
    &:active {
      transform: translate(0, 8px);
    }
    &:active::before,
    &:active::after {
      transform: translate3d(0, 0, -16px);
    }
    &:disabled {
      cursor: not-allowed;
      pointer-events: none;
    }
  }
</style>