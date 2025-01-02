<script lang="ts">
    export let duration: string = "300ms";
    export let offset: number = 40;
    export let tolerance: number = 10;
  
    let headerClass: string = "show";
    let y: number = 0;
    let lastY: number = 0;
  
    function deriveClass(y: number, dy: number): string {
      if (y < offset) {
        return "show";
      }
  
      if (Math.abs(dy) <= tolerance) {
        return headerClass;
      }
  
      if (dy < 0) {
        return "hide";
      }
  
      return "show";
    }
  
    function updateClass(y: number): string {
      const dy = lastY - y;
      lastY = y;
      return deriveClass(y, dy);
    }
  
    function setTransitionDuration(node: HTMLElement): void {
      node.style.transitionDuration = duration;
    }
  
    $: headerClass = updateClass(y);
  </script>
  
  <style>
    div {
      position: fixed;
      width: 100%;
      top: 0;
      transition: transform 300ms linear;
    }
    .show {
      transform: translateY(0%);
    }
    .hide {
      transform: translateY(-100%);
    }
  </style>
  
  <svelte:window bind:scrollY={y} />
  
  <div use:setTransitionDuration class={headerClass}>
      <slot />
  </div>
  