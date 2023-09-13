<script lang="ts">
  export let title: string;
  export let value: string;
  export let score: number;
  export let icon: string;
</script>
<li class="mx-[0.25rem]">
  <div class="flex gap-[0.5rem] items-center mb-[0.6rem]">
    <img class="w-[1.3125rem] shadow-[0_0.25rem_0.375rem_-0.0625rem_rgba(0,0,0,0.12)]" src={icon} alt="icon" />
    <p class="text-[#67748E] text-[0.875rem] font-[600]">{title}</p>
  </div>
  <p class="text-[#252F40] text-[1.5rem] font-[700] mb-[0.25rem]">{value}</p>
  <div class="flex h-[0.1875rem] rounded-[1rem] bg-[#F0F0F0] mb-[1rem]">
    <span class="h-[100%] bg-[#252F40]" style="flex: {score}" />
    <span class="h-[100%]" style="flex: {100 - score}" />
  </div>
</li>
