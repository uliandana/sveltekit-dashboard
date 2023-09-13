<script lang="ts">
  import icTodaysMoney from '$lib/assets/update-todays-money.png';
  import icTodaysUsers from '$lib/assets/update-todays-users.png';
  import icNewClients from '$lib/assets/update-new-clients.png';
  import icSales from '$lib/assets/update-sales.png';
  import icRocket from '$lib/assets/rocket.png';
  import bgPersonWork from '$lib/assets/person work.png';
  import icScoreUsers from '$lib/assets/score-users.png';
  import icScoreClicks from '$lib/assets/score-clicks.png';
  import icScoreSales from '$lib/assets/score-sales.png';
  import icScoreItems from '$lib/assets/score-items.png';

  import UpdateCard from './UpdateCard.svelte';
  import Arrow from '$lib/icons/Arrow.svelte';
	import ScoresItem from './ScoresItem.svelte';
</script>

<section class="flex gap-[1.5rem] mb-[1.5rem] mr-[1.5rem]">
  <UpdateCard title="Today's Money" value="$53,000" rate="+55%" icon={icTodaysMoney} />
  <UpdateCard title="Today's Users" value="2,300" rate="+20%" icon={icTodaysUsers} />
  <UpdateCard title="New Clients" value="+3,462" rate="-2%" icon={icNewClients} />
  <UpdateCard title="Sales" value="$103,430" rate="+5%" icon={icSales} />
</section>
<section class="flex items-stretch gap-[1.5rem] mb-[1.5rem] mr-[1.5rem]">
  <div class="bg-white rounded-[1rem] p-[1rem] flex items-stretch justify-between gap-[3rem] shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
    <div class="flex flex-col justify-between w-[19.85rem]">
      <div>
        <h3 class="text-[#67748E] text-[1rem] font-[600] mb-[0.25rem]">Built by developers</h3>
        <h2 class="text-[#252F40] text-[1.25rem] font-[700] mb-[0.5rem]">Soft UI Dashboard</h2>
        <p class="text-[#67748E] text-[1rem] font-[400] leading-[1.625rem]">From colors, cards, typography to complex elements, you will find the full documentation.</p>
      </div>
      <a class="text-[#67748E] text-[0.875rem] font-[600] flex items-center gap-[0.25rem]" href="/">
        Read More
        <Arrow cls="h-[0.625rem] mt-[0.125rem]" fill="#67748E" />
      </a>
    </div>
    <img class="h-[13.125rem]" src={icRocket} alt="icon rocket" />
  </div>
  <div class="flex-1 bg-white rounded-[1rem] p-[1rem] flex items-stretch shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
    <div class="flex flex-col justify-between rounded-[1rem] p-[1rem] bg-cover" style="background-image: linear-gradient(0, #252F40BF, #252F40BF), url('{bgPersonWork}')">
      <div>
        <h3 class="text-white text-[1.25rem] font-[700] mb-[0.75rem]">Work with the rockets</h3>
        <p class="text-white text-[1rem] font-[400] leading-[1.625rem]">Wealth creation is an evolutionarily recent positive-sum game. It is all about who take the opportunity first.</p>
      </div>
      <a class="text-white text-[0.875rem] font-[600] flex items-center gap-[0.25rem]" href="/">
        Read More
        <Arrow cls="h-[0.625rem] mt-[0.125rem]" fill="white" />
      </a>
    </div>
  </div>
</section>
<section class="flex items-stretch gap-[1.5rem] mb-[1.5rem] mr-[1.5rem]">
  <div class="bg-white rounded-[1rem] p-[1rem] shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
    <div class="w-[26.375rem] h-[13.8125rem] mb-[1.5rem] rounded-[1rem] bg-[#3A416F]" />
    <h3 class="text-[#252F40] text-[1rem] font-[700] mb-[0.2rem]">Active Users</h3>
    <p class="text-[#252F40] text-[0.875rem] font-[400] mb-[1.8rem]">
      <span class="text-[#67748E] font-[700]">(+23%)</span>
      than last week
    </p>
    <ul class="flex items-stretch gap-[1.8rem]">
      <ScoresItem title="Users" value="3,6K" score={60} icon={icScoreUsers} />
      <ScoresItem title="Clicks" value="2m" score={50} icon={icScoreClicks} />
      <ScoresItem title="Sales" value="$772" score={70} icon={icScoreSales} />
      <ScoresItem title="Items" value="82" score={35} icon={icScoreItems} />
    </ul>
  </div>
  <div class="flex-1 bg-white rounded-[1rem] p-[1.5rem] shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
    <h3 class="text-[#252F40] text-[1rem] font-[700] mb-[0.3rem]">Sales Overview</h3>
    <p class="text-[#67748E] text-[0.875rem] font-[600] flex items-center gap-[0.25rem]">
      <Arrow cls="rotate-[270deg]" fill="#82D616" />
      4% more in 2021
    </p>
    <div class="h-[17rem] mt-[4rem] mb-[1rem] border-[0.0625rem] border-[#CB0C9F] rounded-[1rem]" />
  </div>
</section>
