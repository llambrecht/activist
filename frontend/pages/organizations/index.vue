<template>
  <div
    class="px-8 text-light-text dark:text-dark-text bg-light-content dark:bg-dark-content"
  >
    <Head>
      <Title>{{ $t("pages.organizations.index.header-title") }}</Title>
    </Head>
    <HeaderAppPage
      :header="$t('pages.organizations.index.header-title')"
      :tagline="$t('pages.organizations.index.subheader')"
    >
      <div class="flex flex-col space-x-3 sm:flex-row">
        <MarkerTopic topic="My topics dropdown" />
      </div>
    </HeaderAppPage>
    <div
      v-for="organization in organizations"
      class="pt-3 pb-6 space-y-6 md:pt-4"
    >
      <CardSearchResult
        searchResultType="organization"
        :isPrivate="false"
        :organization="organization"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
definePageMeta({
  layout: "sidebar",
});

const { data: organizations } = await useFetch(
  "http://localhost:8000/v1/entities/organizations/",
  {
    method: "GET",
  }
);

// import { Organization } from "../../types/organization";
// const organization: Organization = {
//   name: "tech from below",
//   status: "approved",
//   tagline: "Technologie von und für soziale Bewegungen",
//   location: "Berlin",
//   description: "This is the description of tech from below.",
//   topic: "Technology and Privacy",
//   members: 3,
//   supporters: 30,
//   imageURL: "/images/tech-from-below.svg",
// };
</script>
