<template>
  <div class="card" id="cardId">
    <div class="card__flipper">
      <div class="card__wrapperFront">
        <div class="card__wrapperBack">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardComponent",
  setup() {
    
  },
}
</script>

<style>
  .card {
    display: flex;
    width: 130px;
    height: 130px;
    margin: 0 0 25px 0;
    
    perspective: 600px;
}

.card:hover {
    cursor: pointer;
}

.card__flipper {
    position: relative;
    
    width: 100%;
    height: 100%;
    
    transition: 0.6s;
    transform-style: preserve-3d;   
} 

.card__wrapperFront,
.card__wrapperBack {
    position: absolute;
    top: 0;
    left: 0;
    border-radius: 9px;
    width: 100%;
    height: 100%;
    box-shadow: 1px 1px 5px rgba(0,0,0,0.5);

    backface-visibility: hidden;
}

.card__wrapperFront {
    box-sizing: border-box;
    border: 5px solid white;

    background-image: linear-gradient(45deg, #22ab93, #19668d);
    z-index: 2;
}

.card__wrapperBack {
    display: flex;
    justify-content: center;
    align-content: center;
    background-color: white;
    

    transform: rotateY(180deg);
}
</style>
