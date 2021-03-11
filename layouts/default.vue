<template>
  <div class="container">
    <GlobalHeader />
    <Nuxt />
  </div>
</template>


<style>

/* font-family: 'Lato', sans-serif; */

* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

body {
  font-family: 'Lato', sans-serif;
  color: #333;
  line-height: 1.6;
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
  color: #333;
}

h1, h2 {
  font-weight: 300;
  line-height: 1.2;
  margin: 10px 0; /* Top and bottom margin */
}

p {
  margin: 10px 0;
}

img {
  width: 100%;
}

code, pre {
  background: #333;
  color: #fff;
  padding: 10px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 5px 5px;
}

/* Smaller devices breakpoint */
@media only screen and (max-width: 768px) {

}

/* Bigger devices breakpoint */
@media only screen and (min-width: 768px) {
  
}

</style>
