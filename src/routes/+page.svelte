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
  import icAtlassian from '$lib/assets/logo-atlassian.svg';
  import icInvision from '$lib/assets/logo-invision.svg';
  import icJira from '$lib/assets/logo-jira.svg';
  import icShopify from '$lib/assets/logo-shopify.svg';
  import icSlack from '$lib/assets/logo-slack.svg';
  import icSpotify from '$lib/assets/logo-spotify.svg';

  import face1 from '$lib/assets/face-1.png';
  import face2 from '$lib/assets/face-2.png';
  import face3 from '$lib/assets/face-3.png';
  import face4 from '$lib/assets/face-4.png';

  import icBellGreen from '$lib/assets/bell-green.svg';
  import icHtml5 from '$lib/assets/html5.svg';
  import icCart from '$lib/assets/cart.svg';
  import icCreditCard from '$lib/assets/credit-card.svg';
  import icAccessKey from '$lib/assets/access-key.svg';
  import icMoneyCoins from '$lib/assets/money-coins.svg';

  import UpdateCard from './UpdateCard.svelte';
  import Arrow from '$lib/icons/Arrow.svelte';
	import ScoresItem from './ScoresItem.svelte';

  const faces = [face1, face2, face3, face4];
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
<section class="flex items-stretch gap-[1.5rem] mb-[2.5rem] mr-[1.5rem]">
  <div class="flex-1 bg-white rounded-[1rem] p-[1.5rem] shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
    <h3 class="text-[#252F40] text-[1rem] font-[700] mb-[0.5]">Projects</h3>
    <p class="text-[#67748E] text-[0.875rem] font-[600] mb-[1.75rem]">
      done this month
      <span class="text-[#17C1E8] font-[700]">40%</span>
    </p>
    <table class="w-[100%]">
      <thead>
        <tr>
          {#each ['Companies', 'Members', 'Budget', 'Completion'] as i}
            <th class="py-[0.75rem] uppercase text-[#8392AB] text-[0.875rem] font-[700] text-left">{i}</th>
          {/each}
        </tr>
      </thead>
      <tbody>
        {#each [
          { icon: icShopify, company: 'Soft UI Shopify Version', members: [1, 4, 2, 3], budget: '$14,000', completion: 60 },
          { icon: icAtlassian, company: 'Progress Track', members: [4, 3], budget: '$3,000', completion: 10 },
          { icon: icSlack, company: 'Fix Platform Errors', members: [1, 2, 3], budget: 'Not Set', completion: 100 },
          { icon: icSpotify, company: 'Launch new Mobile App', members: [1, 2], budget: '$20,600', completion: 100 },
          { icon: icJira, company: 'Add the New Landing Page', members: [1, 4, 2, 3], budget: '$4,000', completion: 80 },
          { icon: icInvision, company: 'Redesign Online Store', members: [1, 4, 3], budget: '$2,000', completion: -1 },
        ] as i}
          <tr class="border-t-[0.0625rem] border-t-[#F5F5F5]">
            <td class="py-[1rem] text-[#252F40] text-[0.875rem] font-[600]">
              <img class="w-[1.5rem] mr-[1.5rem] inline-block" src={i.icon} alt="logo" />
              {i.company}
            </td>
            <td class="py-[1rem]">
              {#each i.members as j}
                <img class="h-[1.3125rem] rounded-full inline-block mr-[-0.625rem]" src={faces[j - 1]} alt="user" />
              {/each}
            </td>
            <td class="py-[1rem] text-[#8392AB] text-[0.75rem] font-[600]">
              {i.budget}
            </td>
            <td class="py-[1rem] text-[#67748E] text-[0.875rem] font-[400]">
              {i.completion < 0 ? 'cancel' : `${i.completion}%`}
              <div class="flex items-center rounded-[1rem] w-[7.5rem] h-[0.1875rem] mt-[0.25rem]" style="background-color: {i.completion < 0 ? '#F5222D' : '#E9ECEF'};">
                <span class="h-[100%]" style="flex: {i.completion}; background-color: {i.completion === 100 ? '#52C41A' : '#1890FF'}" />
                <span class="h-[100%]" style="flex: {100 - i.completion}" />
              </div>
            </td>
          </tr>
        {/each}
      </tbody>
    </table>
  </div>
  <div class="w-[22.25rem] bg-white rounded-[1rem] p-[1.5rem] shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
    <h3 class="text-[#252F40] text-[1rem] font-[700] mb-[0.5]">Orders History</h3>
    <p class="text-[#252F40] text-[0.875rem] font-[400] flex items-center gap-[0.25rem] mb-[2.3rem]">
      <Arrow cls="rotate-[270deg] w-[0.75rem]" fill="#82D616" />
      24% this month
    </p>
    <ul>
      {#each [
        { icon: icBellGreen, title: '$2,400 - Redesign store', date: '09 JUN 7:20 PM' },
        { icon: icHtml5, title: 'New order #3654323', date: '08 JUN 12:20 PM' },
        { icon: icCart, title: 'Company server payments ', date: '04 JUN 3:10 PM' },
        { icon: icCreditCard, title: 'New card added for order #4826321', date: '02 JUN 2:45 PM' },
        { icon: icAccessKey, title: 'Unlock folders for development', date: '18 MAY 1:30 PM' },
        { icon: icMoneyCoins, title: 'New order #46282344', date: '14 MAY 3:30 PM' },
      ] as i}
        <li class="
          flex items-start gap-[1rem] mb-[1.3rem] relative
          after:content-[''] after:absolute after:w-[0.125rem] after:h-[2.2rem] after:left-[0.35rem] after:top-[1.65rem] after:bg-[#F5F5F5]
        ">
          <img class="w-[0.875rem] mt-[0.35rem]"
            src={i.icon} alt="icon" />
          <div>
            <h4 class="text-[#252F40] text-[0.875rem] font-[600] mb-[0.25rem]">{i.title}</h4>
            <p class="text-[#67748E] text-[0.75rem] font-[600]">{i.date}</p>
          </div>
        </li>
      {/each}
    </ul>
  </div>
</section>
