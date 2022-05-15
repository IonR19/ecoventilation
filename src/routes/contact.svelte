<div class="bg-slate-800 p-2 text-white">
	<h1 class="mt-10 text-center text-4xl font-semibold">Don't hesitate to contact us !</h1>

	<form class="mx-auto mt-10 max-w-3xl font-light">
		<div class="mt-8">
			<label class="my-2 block text-xl font-thin" for="name">Name:</label>
			<input
				class="block w-full rounded-md py-2 px-3 text-xl text-slate-900"
				type="text"
				id="name"
			/>
		</div>

		<div class="mt-8">
			<label class="my-2 block text-xl font-thin" for="email">Email:</label>
			<input
				class="block w-full rounded-md py-2 px-3 text-xl text-slate-900"
				type="text"
				id="email"
			/>
		</div>

		<div class="mt-8">
			<label class="my-2 block text-xl font-thin" for="subject">Subject:</label>
			<input
				class="block w-full rounded-md py-2 px-3 text-xl text-slate-900"
				type="text"
				id="subject"
			/>
		</div>

		<div class="mt-8">
			<label class="my-2 block text-xl font-thin" for="phone">Phone:</label>
			<div class="flex items-center">
				<div disabled class="rounded-l bg-gray-200 py-2 px-3 text-xl text-slate-900">++965</div>
				<input
					class="block w-full rounded-r py-2 px-3 text-xl text-slate-900"
					type="number"
					id="phone"
				/>
			</div>
		</div>

		<div class="mt-8">
			<label class="my-2 block text-xl font-thin" for="message">Message:</label>
			<textarea
				class="block w-full  resize-none rounded-md py-2 px-3 text-xl text-slate-900"
				rows="5"
				name="message"
				id="message"
			/>
		</div>

		<button
			class="m-5 mx-auto mt-10 block rounded-xl bg-lime-300 py-3 px-5 text-2xl font-extralight text-gray-800"
			>Submit</button
		>
	</form>
</div>
