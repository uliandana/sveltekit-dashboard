<script lang="ts">
  import face1 from '$lib/assets/face-1.png';
  import face2 from '$lib/assets/face-2.png';
  import face3 from '$lib/assets/face-3.png';
  import face4 from '$lib/assets/face-4.png';
  import face5 from '$lib/assets/face-5.png';
  import face6 from '$lib/assets/face-6.png';

  const faces = [face1, face2, face3, face4, face5, face6];
</script>

<section class="bg-white rounded-[1rem] p-[1.5rem] shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)] mb-[1.5rem]">
  <h2 class="text-[1.25rem] text-[#141414] font-[600] mb-[1.5rem]">Authors Table</h2>
  <table class="w-[100%]">
    <thead>
      <tr>
        {#each ['Author', 'Function', 'Status', 'Employed', ''] as i}
          <th class="py-[0.75rem] uppercase text-[#8392AB] text-[0.875rem] font-[700] text-left">{i}</th>
        {/each}
      </tr>
    </thead>
    <tbody>
      {#each [
        { name: 'Michael John', email: 'michael@mail.com', position: 'Manager', function: 'Organization', online: true, employed: '23/04/18' },
        { name: 'Alexa Liras', email: 'alexa@mail.com', position: 'Programmer', function: 'Developer', online: false, employed: '23/23/20' },
        { name: 'Laure Perrier', email: 'laure@mail.com', position: 'Executive', function: 'Projects', online: true, employed: '13/04/19' },
        { name: 'Miriam Eric', email: 'miriam@mail.com', position: 'Marketing', function: 'Organization', online: true, employed: '03/04/21' },
        { name: 'Richard Gran', email: 'richard@mail.com', position: 'Manager', function: 'Organization', online: false, employed: '23/03/20' },
        { name: 'John Levi', email: 'john@mail.com', position: 'Tester', function: 'Developer', online: false, employed: '14/04/17' },
      ] as i, idx}
        <tr class="border-t-[0.0625rem] border-t-[#F5F5F5]">
          <td class="py-[1rem]">
            <div class="flex items-center gap-[1.5rem]">
              <img class="w-[2.5rem] rounded-[0.5rem]" src={faces[idx]} alt="face" />
              <div>
                <h4 class="text-[#141414] text-[1rem] font-[600]">{i.name}</h4>
                <p class="text-[#8392AB] text-[0.875rem] font-[400]">{i.email}</p>
              </div>
            </div>
          </td>
          <td class="py-[1rem]">
            <p class="text-[#8392AB] text-[0.875rem] font-[600]">{i.position}</p>
            <p class="text-[#8392AB] text-[0.875rem] font-[400]">{i.function}</p>
          </td>
          <td class="py-[1rem]">
            {#if i.online}
              <p class="inline-block text-white text-[0.75rem] font-[700] px-[0.75rem] py-[0.25rem] rounded-[0.5rem] bg-green-500">Online</p>
            {:else}
              <p class="inline-block text-white text-[0.75rem] font-[700] px-[0.75rem] py-[0.25rem] rounded-[0.5rem] bg-gray-500">Offline</p>
            {/if}
          </td>
          <td class="py-[1rem] text-[#8392AB] text-[0.875rem] font-[400]">
            {i.employed}
          </td>
          <td class="py-[1rem] text-[#8392AB] text-[0.875rem] font-[400]">
            Edit
          </td>
        </tr>
      {/each}
    </tbody>
  </table>
</section>
<section class="bg-white rounded-[1rem] p-[1.5rem] shadow-[0_1.25rem_1.6875rem_0_rgba(0,0,0,0.05)]">
  <h2 class="text-[1.25rem] text-[#141414] font-[600] mb-[1.5rem]">Projects Table</h2>
  <table></table>
</section>
