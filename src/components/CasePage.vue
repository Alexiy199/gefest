<script setup>
import { ref } from 'vue'

const items = ref([
  'exmp_1',
  'exmp_2',
  'exmp_3',
  'exmp_4',
  'exmp_5',
  'exmp_6',
  'exmp_7',
  'exmp_8',
  'exmp_9',
  'exmp_10',
  'exmp_11',
  'exmp_12',
  'exmp_13',
  'exmp_14',
  'exmp_15',
  'exmp_16',
  'exmp_17',
  'exmp_18'
])

const src = (name) => {
  return name
}
</script>

<template>
  <section id="case-page">
    <div class="wraper-content">
      <h2>Примеры работ</h2>

      <div class="wrap-exmp">
        <div v-for="item in items" class="card-example">
          <div class="box-img">
            <img :src="`/src/assets/gefest/${item}.jpg`" alt="example" class="img-example" />
          </div>
          <div class="description-exmp">
            <span class="title-card">Title</span>
            <p>Описание бла бла бла...</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.wrap-exmp {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  justify-content: center;
  width: 98%;
  margin: 0 auto;
  padding: 1.5em;
  & .card-example {
    position: relative;
    width: 15em;
    height: 15.5em;
    margin: 0;
    cursor: pointer;
    transition: all 0.3s ease;
    & .box-img {
      text-align: center;
      width: 14.9em;
      height: 75%;
      overflow: hidden;
      & .img-example {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center;
        aspect-ratio: 1 / 1;
        image-rendering: crisp-edges;
      }
    }
    & .description-exmp {
      height: 25%;
      border-bottom: 1px solid hsla(0, 90%, 90%, 0.7);
    }
  }
}

@media (hover: hover) {
  .card-example:hover {
    scale: 1.05;
    border: 1px solid hsla(120, 50%, 50%, 0.5);
    box-shadow: 1px 1px 10px 4px hsla(120, 50%, 50%, 0.5);
    & .description-exmp {
      background-color: hsla(120, 50%, 50%, 0.5);
    }
  }
}

@media (hover: none) {
  .card-example:active {
    scale: 1.05;
    border: 1px solid hsla(120, 50%, 50%, 0.5);
    box-shadow: 2px 2px 15px 6px hsla(120, 50%, 50%, 0.5);
    & .description-exmp {
      background-color: hsla(120, 50%, 50%, 0.5);
    }
  }
}
</style>
