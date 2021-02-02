<template>
  <div class="container text-center">
      <nav>
          <ul class="list-unstyled ">
             <li>
               <nuxt-link to="/" class="btn btn-link text-decoration-none">Home</nuxt-link>
               <nuxt-link to="/fade" class="btn btn-link text-decoration-none">Fade</nuxt-link>
               <nuxt-link to="/bounce" class="btn btn-link text-decoration-none">Bounce</nuxt-link>
               <nuxt-link to="/slide" class="btn btn-link text-decoration-none">Slide</nuxt-link>
             </li>
          </ul>
      </nav>
      <main class="pt-5">
        <img src="/tracter.png" alt="tracter">
        <Nuxt/>
      </main>
  </div>
</template>

<style  >
    .page-enter-active,
    .page-leave-active{
      transition: opacity 0.5s;
    }
    .page-enter,
    .page-leave-to{
      opacity: 0;
    }

    .layout-enter-active,
    .layout-leave-active{
      transition: opacity 0.5s;
    }
    .layout-enter,
    .layout-leave-to{
      opacity: 0;
    }

    .slide-bottom-enter-active,
    .slide-bottom-leave-active{
      transition: opacity 0.25s ease-in-out, transform 0.25s ease-in-out;
    }
    .slide-bottom-enter,
    .slide-bottom-leave-to{
      opacity: 0;
      transform: translate3d(0,15px,0);
    }
    .bounce-enter-active{
      transform-origin: top;
      animation: bounce-in 0.8s;
    }
    .bounce-leave-active{
      transform-origin: top;
      animation: bounce-out 0.5s;
    }

    @keyframes bounce-in {
      0%{
        transform: scale(0);
      }
      50%{
        transform: scale(1.25);
      }
      100%{
        transform: scale(1);
      }
    }

    @keyframes bounce-out {
      0%{
        transform: scale(1);
      }
      50%{
        transform: scale(1.25);
      }
      100%{
        transform: scale(0);
      }
    }

</style>
