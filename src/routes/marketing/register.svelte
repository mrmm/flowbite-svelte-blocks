<script lang="ts">
  import { Section, Register } from '$lib';
  import { ExampleDiv, SectionHeader, EditOnGithub, MetaTag } from '../utils';
  import { Breadcrumb, BreadcrumbItem, Button, Checkbox, Label, Input } from 'flowbite-svelte';
  const breadcrumb_title = 'Register';
  const title = 'Register';
  const dir = 'marketing';
  const description =
    'Use a collection of register pages to let your users create an account on your website based on multiple layouts, social media authentication, and more.';
</script>

<MetaTag {breadcrumb_title} {title} {dir} {description} />

<SectionHeader>
  <Breadcrumb navClass="flex mb-3">
    <BreadcrumbItem href="/" home>Blocks</BreadcrumbItem>
    <BreadcrumbItem href="/marketing">Marketing UI</BreadcrumbItem>
    <BreadcrumbItem>Register Forms</BreadcrumbItem>
  </Breadcrumb>
  <svelte:fragment slot="h1">Tailwind CSS Register Form - Flowbite-Svelte-Blocks</svelte:fragment>
  <svelte:fragment slot="paragraph">{description}</svelte:fragment>
</SectionHeader>

<Section name="none" classSection="py-6 sm:py-10" classDiv="px-4 mx-auto max-w-8xl">
  <div class="grid lg:grid-cols-2">
    <div>
      <h2 class="mb-1 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">
        Default register page
      </h2>
      <p class="text-lg text-gray-500 lg:mb-0 dark:text-gray-400 lg:max-w-2xl">
        This example can be used to allow users to create an account on your website using their
        email address and password and also a checkbox with the terms and conditions as a
        requirement.
      </p>
      <EditOnGithub
        size="18"
        href="https://github.com/shinokada/flowbite-svelte-blocks/blob/main/src/routes/marketing/register.svelte"
        iconClass="text-gray-500"
      />
    </div>
  </div>
</Section>

<ExampleDiv>
  <Section name="register">
    <Register href="/">
      <svelte:fragment slot="top">
        <img
          class="w-8 h-8 mr-2"
          src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/logo.svg"
          alt="logo"
        />
        Flowbite
      </svelte:fragment>
      <div class="p-6 space-y-4 md:space-y-6 sm:p-8">
        <form class="flex flex-col space-y-6" action="/">
          <h3 class="text-xl font-medium text-gray-900 dark:text-white p-0">Create and account</h3>
          <Label class="space-y-2">
            <span>Your email</span>
            <Input type="email" name="email" placeholder="name@company.com" required />
          </Label>
          <Label class="space-y-2">
            <span>Your password</span>
            <Input type="password" name="password" placeholder="•••••" required />
          </Label>
          <Label class="space-y-2">
            <span>Confirm password</span>
            <Input type="password" name="confirm-password" placeholder="•••••" required />
          </Label>
          <div class="flex items-start">
            <Checkbox
              >I accept the <a
                class="font-medium text-primary-600 hover:underline dark:text-primary-500"
                href="/"
              >
                Terms and Conditions</a
              ></Checkbox
            >
          </div>
          <Button type="submit" class="w-full1">Create an account</Button>
          <div class="text-sm font-medium text-gray-500 dark:text-gray-300">
            Already have an account? <a
              href="/"
              class="font-medium text-primary-600 hover:underline dark:text-primary-500"
              >Login here</a
            >
          </div>
        </form>
      </div>
    </Register>
  </Section>
</ExampleDiv>
