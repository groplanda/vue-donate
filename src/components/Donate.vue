<template>
  <section class="donate">
    <div class="wrapper">
        <h3 class="donate__title title">о пожертвованиях</h3>
        <div class="donate__wrapper">
          <!--peoples start-->
          <div class="donate__peoples">
            <!--slider start-->
            <div class="donate__peoples-slider">

              <!--slide item start-->
              <div class="donate__peoples-slider-item">
                <h1 class="donate__peoples-slider-title">Садака</h1>
              </div>
              <!--slide item end-->

              <!--slide item start-->
              <div class="donate__peoples-slider-item">
                <h1 class="donate__peoples-slider-title active">Закят</h1>
              </div>
              <!--slide item end-->

              <!--slide item start-->
              <div class="donate__peoples-slider-item">
                <h1 class="donate__peoples-slider-title">Фитр</h1>
              </div>
              <!--slide item end-->

              <!--slide item start-->
              <div class="donate__peoples-slider-item">
                <h1 class="donate__peoples-slider-title">Садака</h1>
              </div>
              <!--slide item end-->

              <!--slide item start-->
              <div class="donate__peoples-slider-item">
                <h1 class="donate__peoples-slider-title">Фитр</h1>
              </div>
              <!--slide item end-->

            </div>
            <!--slider end-->

            <div class="donate__peoples-slider-navigation">
              <button class="donate__peoples-slider-arrow next">
                <img src="@/assets/images/icon/arrow.svg" alt="arrow">
              </button>
            </div>

          </div>
          <!--peoples end-->
          <div class="donate__content">
            <!--content start-->
            <div class="donate__content-body">
              <p class="donate__content-description">
                один из пяти столпов ислама, обязательный ежегодный налог в исламском праве,
                выплачиваемый с различного вида доходов и имущества (движимого и недвижимого)
                всеми самостоятельными, свободными, дееспособными и взрослыми мусульманами в
                пользу нуждающихся единоверцев. Согласно шариату, его выплата означает, что
                полученные доходы и нажитое богатство не являются греховными. Точные размеры
                закята, как и то на какие виды собственности он распространяется, являются
                предметом дискуссий среди знатоков мусульманского права.
              </p>
              <div class="donate__content-action">
                <button class="donate__content-button">Расчитать закят</button>
              </div>
            </div>

            <!--content end-->
          </div>
        </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Donate',
  mounted() {
    const slider = document.querySelector('.donate__peoples-slider'),
          slides = slider.querySelectorAll('.donate__peoples-slider-item');
    window.addEventListener('resize', event => {
      const target = event.target;
      if(target.innerWidth <= 768) {
        slider.prepend(slides[1]);
      } else {
        slider.prepend(slides[0]);
      }
    }, false);

    if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
      slider.prepend(slides[1]);
    }
  }
}
</script>