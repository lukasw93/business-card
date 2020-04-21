<script>
  import PersonConfig, { person } from '../components/PersonConfig.svelte';
</script>

<svelte:head>
	<title>Business Card - {person.fullname}</title>
</svelte:head>

<div class="z-40 grid grid-cols-1 text-center pt-3 lg:pt-4 xl:pt-12">
  <div class="mt-4 text-lg md:text-2xl">{@html person.displayNameHtml}</div>
  <div class="text-gray-700 text-base md:text-xl">{person.jobTitle}<br/><a target="_blank" class="text-blue-700 hover:text-blue-400" href="{person.companyUrl}">@{person.company}</a></div>
  <div class="mt-6 text-sm md:text-base">{person.fullname}</div>
  <div class="text-sm md:text-base">phone: <a href="tel:{person.phoneNumber}" class="text-blue-700 hover:text-blue-400">{person.phoneDisplayNumber}</a></div>
  <div class="text-sm md:text-base">email: <a href="mailto:{person.email}" class="text-blue-700 hover:text-blue-400">{person.email}</a></div>
  <div class="mx-auto mt-1 flex items-center">
    {#if person.linkedinUrl}
      <div class="m-1 hover:opacity-75">
        <a target="_blank" href="{person.linkedinUrl}">
          <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 172 172" style=" fill:#000000;">
            <g fill="none" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><path d="M0,172v-172h172v172z" fill="none"></path><g fill="#000000"><path d="M141.04,13.76h-110.08c-9.4944,0 -17.2,7.7056 -17.2,17.2v110.08c0,9.4944 7.7056,17.2 17.2,17.2h110.08c9.4944,0 17.2,-7.7056 17.2,-17.2v-110.08c0,-9.4944 -7.7056,-17.2 -17.2,-17.2zM58.48,68.8v65.36h-20.64v-65.36zM37.84,49.7768c0,-4.816 4.128,-8.4968 10.32,-8.4968c6.192,0 10.0792,3.6808 10.32,8.4968c0,4.816 -3.8528,8.7032 -10.32,8.7032c-6.192,0 -10.32,-3.8872 -10.32,-8.7032zM134.16,134.16h-20.64c0,0 0,-31.8544 0,-34.4c0,-6.88 -3.44,-13.76 -12.04,-13.8976h-0.2752c-8.3248,0 -11.7648,7.0864 -11.7648,13.8976c0,3.1304 0,34.4 0,34.4h-20.64v-65.36h20.64v8.8064c0,0 6.6392,-8.8064 19.9864,-8.8064c13.6568,0 24.7336,9.3912 24.7336,28.4144z"></path></g></g>
          </svg>
        </a>
      </div>
    {/if}
    {#if person.instagramUrl}
      <div class="m-1 hover:opacity-75">
        <a target="_blank" href="{person.instagramUrl}">
          <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 172 172" style=" fill:#000000;">
            <g fill="none" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><path d="M0,172v-172h172v172z" fill="none"></path><g fill="#000000"><path d="M55.04,10.32c-24.65626,0 -44.72,20.06374 -44.72,44.72v61.92c0,24.65626 20.06374,44.72 44.72,44.72h61.92c24.65626,0 44.72,-20.06374 44.72,-44.72v-61.92c0,-24.65626 -20.06374,-44.72 -44.72,-44.72zM55.04,17.2h61.92c20.9375,0 37.84,16.9025 37.84,37.84v61.92c0,20.9375 -16.9025,37.84 -37.84,37.84h-61.92c-20.9375,0 -37.84,-16.9025 -37.84,-37.84v-61.92c0,-20.9375 16.9025,-37.84 37.84,-37.84zM127.28,37.84c-3.79972,0 -6.88,3.08028 -6.88,6.88c0,3.79972 3.08028,6.88 6.88,6.88c3.79972,0 6.88,-3.08028 6.88,-6.88c0,-3.79972 -3.08028,-6.88 -6.88,-6.88zM86,48.16c-20.85771,0 -37.84,16.98229 -37.84,37.84c0,20.85771 16.98229,37.84 37.84,37.84c20.85771,0 37.84,-16.98229 37.84,-37.84c0,-20.85771 -16.98229,-37.84 -37.84,-37.84zM86,55.04c17.13948,0 30.96,13.82052 30.96,30.96c0,17.13948 -13.82052,30.96 -30.96,30.96c-17.13948,0 -30.96,-13.82052 -30.96,-30.96c0,-17.13948 13.82052,-30.96 30.96,-30.96z"></path></g></g>
          </svg>
        </a>
      </div>
    {/if}
    {#if person.twitterUrl}
      <div class="m-1 hover:opacity-75">
        <a target="_blank" href="{person.githubUrl}">
          <svg fill="#000000" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24px" height="24px"><path d="M 24 4.300781 C 23.101563 4.699219 22.199219 5 21.199219 5.101563 C 22.199219 4.5 23 3.5 23.398438 2.398438 C 22.398438 3 21.398438 3.398438 20.300781 3.601563 C 19.300781 2.601563 18 2 16.601563 2 C 13.898438 2 11.699219 4.199219 11.699219 6.898438 C 11.699219 7.300781 11.699219 7.699219 11.800781 8 C 7.699219 7.800781 4.101563 5.898438 1.699219 2.898438 C 1.199219 3.601563 1 4.5 1 5.398438 C 1 7.101563 1.898438 8.601563 3.199219 9.5 C 2.398438 9.398438 1.601563 9.199219 1 8.898438 C 1 8.898438 1 8.898438 1 9 C 1 11.398438 2.699219 13.398438 4.898438 13.800781 C 4.5 13.898438 4.101563 14 3.601563 14 C 3.300781 14 3 14 2.699219 13.898438 C 3.300781 15.898438 5.101563 17.300781 7.300781 17.300781 C 5.601563 18.601563 3.5 19.398438 1.199219 19.398438 C 0.800781 19.398438 0.398438 19.398438 0 19.300781 C 2.199219 20.699219 4.800781 21.5 7.5 21.5 C 16.601563 21.5 21.5 14 21.5 7.5 C 21.5 7.300781 21.5 7.101563 21.5 6.898438 C 22.5 6.199219 23.300781 5.300781 24 4.300781"/></svg>
        </a>
      </div>
    {/if}
    {#if person.facebookUrl}
      <div class="m-1 hover:opacity-75">
        <a target="_blank" href="{person.githubUrl}">
          <svg fill="#000000" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="26" height="26"><path d="M 21.800781 0 L 2.199219 0 C 1 0 0 1 0 2.199219 L 0 21.800781 C 0 23 1 24 2.199219 24 L 12 24 L 12 14 L 9 14 L 9 11 L 12 11 L 12 8 C 12 5.5 13 4 16 4 L 19 4 L 19 7 L 17.699219 7 C 16.800781 7 16 7.800781 16 8.699219 L 16 11 L 20 11 L 19.5 14 L 16 14 L 16 24 L 21.800781 24 C 23 24 24 23 24 21.800781 L 24 2.199219 C 24 1 23 0 21.800781 0 Z"/></svg>
        </a>
      </div>
    {/if}
    {#if person.githubUrl}
      <div class="m-1 hover:opacity-75">
        <a target="_blank" href="{person.githubUrl}">
          <svg height="27" width="27" viewBox="0 0 16 16" version="1.1" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"></path></svg>
        </a>
      </div>
    {/if}
  </div>
</div>