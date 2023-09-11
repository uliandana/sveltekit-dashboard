<script lang="ts">
  export let title: string;
  export let value: string;
  export let rate: string;
  export let icon: string;

  const clRate = rate.startsWith('-') ? 'text-[#EA0606] text-[0.875rem] font-[700] ml-[0.25rem]' : 'text-[#82D616] text-[0.875rem] font-[700] ml-[0.25rem]';
</script>
<div class="flex gap-[1rem] items-center justify-between flex-1 bg-white rounded-[1rem] p-[1rem] shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
  <div>
    <h5 class="text-[#67748E] text-[0.875rem] font-[600] mb-[0.25rem]">{title}</h5>
    <p class="text-[#252F40] text-[1.25rem] font-[700]">{value} <span class={clRate}>{rate}</span></p>
  </div>
  <img class="w-[3rem] shadow-[0_0.125rem_0.25rem_-0.0625rem_rgba(0,0,0,0.07)]" src={icon} alt="icon" />
</div>
