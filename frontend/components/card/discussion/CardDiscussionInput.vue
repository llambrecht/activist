<template>
  <div class="flex flex-col w-full md:flex-row card-style px-3 py-4">
    <div class="flex-col pt-3 space-y-3 md:pl-2 md:space-y-4 md:grow md:pt-0">
      <div class="flex flex-col justify-between md:flex-row">
        <div class="flex items-center justify-center space-x-2 md:space-x-4">
          <div class="w-min md:w-min">
            <BtnLabeled
              class="w-small flex mt-1"
              :cta="true"
              :label="$t('components.card-discussion-input.write')"
              fontSize="sm"
              iconSize="1.25em"
              ariaLabel="components.btn-labeled.support-organization-aria-label"
            />
          </div>
          <div class="w-min md:w-min">
            <BtnLabeled
              class="w-small flex mt-1"
              :cta="false"
              :label="$t('components.card-discussion-input.preview')"
              fontSize="sm"
              iconSize="1.25em"
              ariaLabel="components.btn-labeled.support-organization-aria-label"
            />
          </div>
        </div>
        <div
          class="flex items-center w-full mt-2 space-x-1 md:flex-row md:w-fit lg:space-x-3"
        >
          <Icon
            @click="at()"
            class="cursor-pointer"
            name="bi:at"
            size="1.75em"
          />
          <Icon
            @click="heading()"
            class="cursor-pointer"
            name="bi:h-square"
            size="1.5em"
          />
          <Icon
            @click="bold()"
            class="cursor-pointer"
            name="bi:type-bold"
            size="1.75em"
          />
          <Icon
            @click="italic()"
            class="cursor-pointer"
            name="bi:type-italic"
            size="1.75em"
          />
          <Icon
            @click="blockquote()"
            class="cursor-pointer"
            name="bi:blockquote-left"
            size="1.75em"
          />
          <Icon
            @click="link()"
            class="cursor-pointer"
            name="bi:link-45deg"
            size="1.75em"
          />
          <Icon
            @click="attach()"
            class="cursor-pointer"
            name="bi:paperclip"
            size="1.6em"
          />
          <Icon
            @click="listul()"
            class="cursor-pointer"
            name="bi:list-ul"
            size="1.75em"
          />
          <Icon
            @click="listol()"
            class="cursor-pointer"
            name="bi:list-ol"
            size="1.75em"
          />
        </div>
      </div>
      <div class="w-full md:w-full">
        <textarea
          id="message"
          rows="4"
          class="block p-2.5 w-full text-sm text-light-text bg-light-content rounded-lg border border-light-section-div dark:bg-dark-content dark:border-dark-section-div placeholder-light-special-text dark:placeholder-dark-special-text dark:text-dark-text focus-brand"
          :placeholder="$t('components.card-discussion-input.leave-comment')"
        ></textarea>
      </div>
      <div class="flex items-center justify-between px-1">
        <p class="inline-flex items-center">
          {{ $t("components.card-discussion-input.markdown-support") }}
          <Icon class="mx-1" name="bi:markdown" size="1.25em"></Icon>
        </p>
        <div class="flex space-x-1">
          <BtnLabeled
            class="inline-flex justify-center items-center w-small"
            :cta="true"
            :label="$t('components.card-discussion-input.comment')"
            fontSize="sm"
            iconSize="1.25em"
            ariaLabel="components.btn-labeled.support-organization-aria-label"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { DiscussionInput } from "~/types/card-discussion-input";

defineProps<{
  discussionInput: DiscussionInput;
}>();

const at = () => {
  console.log("click on at");
};

const heading = () => {
  console.log("click on heading");
};

const bold = () => {
  console.log("click on bold");
};

const italic = () => {
  console.log("click on italic");
};

const blockquote = () => {
  console.log("click on blockquote");
};

const link = () => {
  console.log("click on link");
};

const attach = () => {
  console.log("click on attach");
};

const listul = () => {
  console.log("click on listul");
};

const listol = () => {
  console.log("click on listol");
};
</script>
