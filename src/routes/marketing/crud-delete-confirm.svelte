<script lang="ts">
  import { Section } from '$lib';
  import { ExampleDiv, SectionHeader, EditOnGithub, MetaTag } from '../utils';
  import { Button, Modal, P, Breadcrumb, BreadcrumbItem } from 'flowbite-svelte';
  const breadcrumb_title = 'Crud delete confirm';
  const title = 'Crud delete confirm';
  const dir = 'marketing';
  const description =
    'Get started with a collection of delete confirmation modal components based on the CRUD layout to make sure the user is ready to remove a selected item.';
  let defaultModal = false;
</script>

<MetaTag {breadcrumb_title} {title} {dir} {description} />

<SectionHeader>
  <Breadcrumb navClass="flex mb-3">
    <BreadcrumbItem href="/" home>Blocks</BreadcrumbItem>
    <BreadcrumbItem href="/marketing">Marketing UI</BreadcrumbItem>
    <BreadcrumbItem>Delete Confirm (CRUD)</BreadcrumbItem>
  </Breadcrumb>
  <svelte:fragment slot="h1"
    >Tailwind CSS Delete Confirm (CRUD) - Flowbite-Svelte-Blocks</svelte:fragment
  >
  <svelte:fragment slot="paragraph">{description}</svelte:fragment>
</SectionHeader>

<Section name="none" classSection="py-6 sm:py-10" classDiv="px-4 mx-auto max-w-8xl">
  <div class="grid lg:grid-cols-2">
    <div>
      <h2 class="mb-1 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">
        Default delete confirmation modal
      </h2>
      <p class="text-lg text-gray-500 lg:mb-0 dark:text-gray-400 lg:max-w-2xl">
        Use this free example of a modal component coded with Tailwind CSS to confirm with the user
        before deleting an item from the database.
      </p>
      <EditOnGithub
        size="18"
        href="https://github.com/shinokada/flowbite-svelte-blocks/blob/main/src/routes/marketing/crud-delete-confirm.svelte"
        iconClass="text-gray-500"
      />
    </div>
  </div>
</Section>

<ExampleDiv>
  <div class="flex justify-center m-5">
    <Button on:click={() => (defaultModal = true)}>Show delete confirmation</Button>
  </div>
  <Modal title="" size="sm" bind:open={defaultModal} autoclose>
    <svg
      class="text-gray-400 dark:text-gray-500 w-11 h-11 mb-3.5 mx-auto"
      aria-hidden="true"
      fill="currentColor"
      viewBox="0 0 20 20"
      xmlns="http://www.w3.org/2000/svg"
      ><path
        fill-rule="evenodd"
        d="M9 2a1 1 0 00-.894.553L7.382 4H4a1 1 0 000 2v10a2 2 0 002 2h8a2 2 0 002-2V6a1 1 0 100-2h-3.382l-.724-1.447A1 1 0 0011 2H9zM7 8a1 1 0 012 0v6a1 1 0 11-2 0V8zm5-1a1 1 0 00-1 1v6a1 1 0 102 0V8a1 1 0 00-1-1z"
        clip-rule="evenodd"
      /></svg
    >
    <P align="center">Are you sure you want to delete this item?</P>
    <div class="flex justify-center items-center space-x-4">
      <Button color="light">No, cancel</Button>
      <Button color="red" type="submit">Yes, I'm sure</Button>
    </div>
  </Modal>
</ExampleDiv>
