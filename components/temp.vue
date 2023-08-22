<div class="flex flex-col">
  <div class="md:mx-auto pt-2 sm:pt-7 md:pt-5 pb-2 px-4 md:px-0 w-full md:w-[90%] 2xl:w-[55%]">
    <div class="inline-block min-w-full py-2 sm:px-6 lg:px-8">
      <div class="overflow-hidden">
        <table class="min-w-full text-white text-left text-sm font-light">
          <thead class="border-b font-medium dark:border-neutral-500">
            <tr>
              <th scope="col" class="flex items-center px-6 py-4">
                Name
                <img src="../static/group.svg" alt="group svg icon">
              </th>
              <th scope="col" class="px-6 py-4">OVR</th>
              <th scope="col" class="px-6 py-4">POS</th>
              <th scope="col" class="px-6 py-4">Type</th>
              <th scope="col" class="px-6 py-4">PAC</th>
              <th scope="col" class="px-6 py-4">SHO</th>
              <th scope="col" class="px-6 py-4">PAS</th>
              <th scope="col" class="px-6 py-4">DRI</th>
              <th scope="col" class="px-6 py-4">DEF</th>
              <th scope="col" class="px-6 py-4">PHY</th>
              <th scope="col" class="px-6 py-4">WR</th>
            </tr>
          </thead>
          <tbody>
            <tr class="border-b dark:border-neutral-500">
              <td class="whitespace-nowrap px-6 py-4 font-medium">1</td>
              <td class="whitespace-nowrap px-6 py-4">Mark</td>
              <td class="whitespace-nowrap px-6 py-4">Otto</td>
              <td class="whitespace-nowrap px-6 py-4">@mdo</td>
              <td class="whitespace-nowrap px-6 py-4">@mdo</td>
              <td class="whitespace-nowrap px-6 py-4">@mdo</td>
              <td class="whitespace-nowrap px-6 py-4">@mdo</td>
              <td class="whitespace-nowrap px-6 py-4">@mdo</td>
              <td class="whitespace-nowrap px-6 py-4">@mdo</td>
              <td class="whitespace-nowrap px-6 py-4">@mdo</td>
              <td class="whitespace-nowrap px-6 py-4">@mdo</td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="relative overflow-x-auto">
			<table class="w-full text-left text-sm text-gray-500 dark:text-gray-400">
				<tbody>
					<tr class="border-b bg-white dark:border-gray-700 dark:bg-gray-800">
						<th
							scope="row"
							class="whitespace-nowrap px-6 py-4 font-medium text-gray-900 dark:text-white"
						>
							Name
						</th>
						<td class="px-6 py-4"> {data.feedback?.name ? data.feedback.name : '(no name)'} </td>
					</tr>
					<tr class="border-b bg-white dark:border-gray-700 dark:bg-gray-800">
						<th
							scope="row"
							class="whitespace-nowrap px-6 py-4 font-medium text-gray-900 dark:text-white"
						>
							Email
						</th>
						<td class="px-6 py-4"> {data.feedback?.email} </td>
					</tr>
					<tr class="bg-white dark:bg-gray-800">
						<th
							scope="row"
							class="whitespace-nowrap px-6 py-4 font-medium text-gray-900 dark:text-white"
						>
							Feedback comment
						</th>
						<td class="px-6 py-4"> {data.feedback?.comment}</td>
					</tr>
				</tbody>
			</table>
		</div>
    </div>
  </div>
</div>
