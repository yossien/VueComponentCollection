<template>
  <div class="modal-mask">
    <div class="modal-wrapper">
      <div class="loader">
      </div>
      <div class="loading-message">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Loading.vue"
    }
</script>

<style scoped lang="scss">
  $mask-background-color : rgba(255, 255, 255, .7);

  $loading-message-font-size : 32px;
  $loading-message-font-weight : lighter;
  $loading-message-color: #aaa;
  $loading-message-font-family: "ヒラギノ角ゴ ProN W3","Courier","Arial Narrow";
  $loading-letter-spacing: 1.2em;

  $loading-color : #888;
  $loading-color-1 : rgba(128, 128, 128, 0.2);
  $loading-color-2 : rgba(128, 128, 128, 0.5);
  $loading-color-3 : rgba(128, 128, 128, 0.7);
  $loader-animation-speed : 1.3s;

  .loader {
    margin: 100px auto;
    font-size: 25px;
    width: 1em;
    height: 1em;
    border-radius: 50%;
    position: relative;
    text-indent: -9999em;
    -webkit-animation: load5 $loader-animation-speed infinite ease;
    animation: load5 $loader-animation-speed infinite ease;
    -webkit-transform: translateZ(0);
    -ms-transform: translateZ(0);
    transform: translateZ(0);
  }
  .loading-message {
    display: block;
    padding-top: 1.2em;
    font-size: $loading-message-font-size;
    font-weight: $loading-message-font-weight;
    font-family: $loading-message-font-family;
    letter-spacing: $loading-letter-spacing;
    color: $loading-message-color;
  }
  @-webkit-keyframes load5 {
    0%,
    100% {
      box-shadow: 0em -2.6em 0em 0em $loading-color, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-2, -1.8em -1.8em 0 0em $loading-color-3;
    }
    12.5% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-3, 1.8em -1.8em 0 0em $loading-color, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-2;
    }
    25% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-2, 1.8em -1.8em 0 0em $loading-color-3, 2.5em 0em 0 0em $loading-color, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-1;
    }
    37.5% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-2, 2.5em 0em 0 0em $loading-color-3, 1.75em 1.75em 0 0em $loading-color, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-1;
    }
    50% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-2, 1.75em 1.75em 0 0em $loading-color-3, 0em 2.5em 0 0em $loading-color, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-1;
    }
    62.5% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-2, 0em 2.5em 0 0em $loading-color-3, -1.8em 1.8em 0 0em $loading-color, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-1;
    }
    75% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-2, -1.8em 1.8em 0 0em $loading-color-3, -2.6em 0em 0 0em $loading-color, -1.8em -1.8em 0 0em $loading-color-1;
    }
    87.5% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-2, -2.6em 0em 0 0em $loading-color-3, -1.8em -1.8em 0 0em $loading-color;
    }
  }
  @keyframes load5 {
    0%,
    100% {
      box-shadow: 0em -2.6em 0em 0em $loading-color, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-2, -1.8em -1.8em 0 0em $loading-color-3;
    }
    12.5% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-3, 1.8em -1.8em 0 0em $loading-color, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-2;
    }
    25% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-2, 1.8em -1.8em 0 0em $loading-color-3, 2.5em 0em 0 0em $loading-color, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-1;
    }
    37.5% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-2, 2.5em 0em 0 0em $loading-color-3, 1.75em 1.75em 0 0em $loading-color, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-1;
    }
    50% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-2, 1.75em 1.75em 0 0em $loading-color-3, 0em 2.5em 0 0em $loading-color, -1.8em 1.8em 0 0em $loading-color-1, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-1;
    }
    62.5% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-2, 0em 2.5em 0 0em $loading-color-3, -1.8em 1.8em 0 0em $loading-color, -2.6em 0em 0 0em $loading-color-1, -1.8em -1.8em 0 0em $loading-color-1;
    }
    75% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-2, -1.8em 1.8em 0 0em $loading-color-3, -2.6em 0em 0 0em $loading-color, -1.8em -1.8em 0 0em $loading-color-1;
    }
    87.5% {
      box-shadow: 0em -2.6em 0em 0em $loading-color-1, 1.8em -1.8em 0 0em $loading-color-1, 2.5em 0em 0 0em $loading-color-1, 1.75em 1.75em 0 0em $loading-color-1, 0em 2.5em 0 0em $loading-color-1, -1.8em 1.8em 0 0em $loading-color-2, -2.6em 0em 0 0em $loading-color-3, -1.8em -1.8em 0 0em $loading-color;
    }
  }

  .modal-mask {
    position: fixed;
    z-index: 9998;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: $mask-background-color;
    display: table;
    transition: opacity .3s ease;
  }

  .modal-wrapper {
    display: table-cell;
    vertical-align: middle;
  }

  .modal-header h3 {
    margin-top: 0;
    color: #42b983;
  }

</style>