<script>
    const lyrics = [
      "여수 밤바다", "이 조명에 담긴", "아름다운 얘기가 있어", "네게 들려주고파", 
      "전활 걸어 뭐 하고 있냐고", "나는 지금 여수 밤바다", "여수 밤바다", 
      "아 아 아 아 아 아 아", "너와 함께 걷고 싶다", "이 바다를 너와 함께 걷고 싶어", 
      "이 거리를 너와 함께 걷고 싶다", "이 바다를 너와 함께 걷고 싶어", 
      "여수 밤바다", "여수 밤바다", "이 바람에 걸린 알 수 없는", "향기가 있어", 
      "네게 전해주고파 전활 걸어", "뭐 하고 있냐고", "나는 지금 여수 밤바다", 
      "여수 밤바다", "아 아 아 아 아 아 아 아", "너와 함께 걷고 싶다", 
      "이 바다를 너와 함께 걷고 싶어", "이 거리를 너와 함께 걷고 싶다", 
      "이 바다를 너와 함께", "너와 함께 오", "바다 이 조명에 담긴", 
      "아름다운 얘기가 있어", "네게 들려주고파", "전활 걸어 뭐 하고 있냐고", 
      "나는 지금 여수 밤바다", "여수 밤바다", "아 바다 아아아 하아 아아", 
      "허오오오", "허오오오 허오오오", "뭐 하고 있냐고", "나는 지금 여수 밤바다"
  ];

  let currentIndex = 0;

   setInterval(() => {
      currentIndex = (currentIndex + 1) % lyrics.length;
  }, 2000);
</script>

<article class="scroll">
    <section>
        {#each lyrics as lyric, index}
            <p class:current={index === currentIndex} class:previous={index < currentIndex}>
                {lyric}
            </p>
        {/each}
    </section>
    
</article>

<style lang="scss">
   .scroll {
      width: 100%;
      height: 15%;
      border: solid 1px red;
      overflow: hidden;    
      scroll-behavior: smooth;
      position: relative;
  }

  section {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
  }

  p {
      font-size: 1.2rem;
      opacity: 0.5;
      transition: opacity 0.5s, font-weight 0.5s;
  }

  p.current {
      opacity: 1;
      font-weight: bold;
  }

  p.previous {
      opacity: 0.2;
  }

  @keyframes scrollText {
      from { transform: translateY(0%); }
      to { transform: translateY(-1800%); }
  }

  section {
      animation: scrollText 20s infinite linear;
  }
</style>

