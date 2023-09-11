<script lang="ts">
  import UpdateCard from './UpdateCard.svelte';
  import icTodaysMoney from '$lib/assets/update-todays-money.png';
  import icTodaysUsers from '$lib/assets/update-todays-users.png';
  import icNewClients from '$lib/assets/update-new-clients.png';
  import icSales from '$lib/assets/update-sales.png';
  import icRocket from '$lib/assets/rocket.png';
  import bgPersonWork from '$lib/assets/person work.png';
</script>

<section class="flex gap-[1.5rem] mb-[1.5rem] mr-[1.5rem]">
  <UpdateCard title="Today's Money" value="$53,000" rate="+55%" icon={icTodaysMoney} />
  <UpdateCard title="Today's Users" value="2,300" rate="+20%" icon={icTodaysUsers} />
  <UpdateCard title="New Clients" value="+3,462" rate="-2%" icon={icNewClients} />
  <UpdateCard title="Sales" value="$103,430" rate="+5%" icon={icSales} />
</section>
<section class="flex items-stretch gap-[1.5rem] mb-[1.5rem] mr-[1.5rem]">
  <div class="bg-white rounded-[1rem] p-[1rem] flex items-stretch justify-between gap-[2rem] shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
    <div class="flex flex-col justify-between">
      <div>
        <h3 class="text-[#67748E] text-[1rem] font-[600] mb-[0.25rem]">Built by developers</h3>
        <h2 class="text-[#252F40] text-[1.25rem] font-[700] mb-[0.5rem]">Soft UI Dashboard</h2>
        <p class="text-[#67748E] text-[1rem] font-[400] leading-[1.625rem]">From colors, cards, typography to complex elements, you will find the full documentation.</p>
      </div>
      <a class="text-[#67748E] text-[0.875rem] font-[600]" href="/">Read More <span>{'->'}</span></a>
    </div>
    <img class="h-[13.125rem]" src={icRocket} alt="icon rocket" />
  </div>
  <div class="bg-white rounded-[1rem] p-[1rem] flex items-stretch shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
    <div class="flex flex-col justify-between rounded-[1rem] p-[1rem] bg-cover" style="background-image: linear-gradient(0, #252F40BF, #252F40BF), url('{bgPersonWork}')">
      <div>
        <h3 class="text-white text-[1.25rem] font-[700] mb-[0.75rem]">Work with the rockets</h3>
        <p class="text-white text-[1rem] font-[400] leading-[1.625rem]">Wealth creation is an evolutionarily recent positive-sum game. It is all about who take the opportunity first.</p>
      </div>
      <a class="text-white text-[0.875rem] font-[600]" href="/">Read More <span>{'->'}</span></a>
    </div>
  </div>
</section>
