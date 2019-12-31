<template>
    <nav>
      <div class="flex flex-row justify-between">
        <a class="text-green-600 text-xs font-bold underline" href="https://github.com/davidfowl/FeatherHttp">.NET Feather HTTP GitHub</a>
        <button @click="toggleMenu">
          <svg height="32px" id="Layer_1" style="enable-background:new 0 0 32 32; color: white;" version="1.1" viewBox="0 0 32 32" width="32px" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <path fill="#38a169" d="m4,8.491662l24,0c1.104,0 2,-1.121245 2,-2.502779s-0.896,-2.502779 -2,-2.502779l-24,0c-1.104,0 -2,1.121245 -2,2.502779s0.896,2.502779 2,2.502779zm24,5.005559l-24,0c-1.104,0 -2,1.121245 -2,2.502779s0.896,2.502779 2,2.502779l24,0c1.104,0 2,-1.121245 2,-2.502779s-0.896,-2.502779 -2,-2.502779zm0,10.011118l-24,0c-1.104,0 -2,1.121245 -2,2.502779s0.896,2.502779 2,2.502779l24,0c1.104,0 2,-1.121245 2,-2.502779s-0.896,-2.502779 -2,-2.502779z"></path>
          </svg>
        </button>
      </div>
      <ul :class="{ 'max-h-none': isHidden, 'p-2 border-gray-700 border max-h-full transition-max-height': !isHidden }" class="absolute leading-loose mt-1 rounded-lg font-bold bg-green-500 text-white w-4/5 transition-250 overflow-y-hidden">
        <li><a href="#">Hello World</a></li>
        <li><a href="#">MVC</a></li>
        <li><a href="#">Razor Page</a></li>
        <li><a href="#">SignalR</a></li>
        <li><a href="#">gRPC</a></li>
        <li><a href="#">Blazor</a></li>
      </ul>
    </nav>
</template>

<script>
export default {
    data() {
      return {
        isHidden: true
      }
    },
    methods: {
      toggleMenu() {
        this.isHidden = !this.isHidden;
      }
    }
}
</script>