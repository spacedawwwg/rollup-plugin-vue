<style scoped>
.test {
  color: red;
}
.test:after {
  content: 'bye!';
}
h1 {
  color: green;
}
.anim {
  animation: color 5s infinite, other 5s;
}
.anim-2 {
  animation-name: color;
  animation-duration: 5s;
}
.anim-3 {
  animation: 5s color infinite, 5s other;
}
.anim-multiple {
  animation: color 5s infinite, opacity 2s;
}
.anim-multiple-2 {
  animation-name: color, opacity;
  animation-duration: 5s, 2s;
}

@keyframes color {
  from {
    color: red;
  }
  to {
    color: green;
  }
}
@-webkit-keyframes color {
  from {
    color: red;
  }
  to {
    color: green;
  }
}
@keyframes opacity {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes opacity {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
.foo p >>> .bar {
  color: red;
}
</style>

<template>
  <div>
    <div><h1>hi</h1></div>
    <p class="abc def">hi</p>
    <template v-if="!ok"><p class="test" id="test">Hello</p></template>
    <svg>
      <template>
        <p></p>
      </template>
    </svg>
  </div>
</template>
