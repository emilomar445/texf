# texf<div id="app" class="media-display">
  <button @click="prev" class="button prev">Prev</button>
  <button @click="shuffle" class="button shuffle">Shuffle</button>
  <button @click="next" class="button next">Next</button>
  
  <transition-group name="flip-list" class="media-gallery">
    <figure 
            class="media-post" 
            v-for="(image,i) in images" 
            :key="image" 
            @click="shift(image)"
            :style="{ 
                    '--i': i, 
                    '--flip-delay': images.length - i 
                    }">
      <img :src="image" width="400" height="400" />
      <figcaption>{{i+1}}</figcaption>
    </figure>
  </transition-group>
</div>
