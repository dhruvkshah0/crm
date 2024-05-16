<template>
  <Dialog
    v-model="show"
    :options="{
      size: '3xl',
      title: __('New Lender'),
    }"
  >
    <template #body-content>
      <Tabs v-model="tabIndex" v-slot="{ tab }" :tabs="tabs">
        <template v-if="tab.name === 'Details'">
          <div class="grid-container">
            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Name") }}
                </div>
                <TextInput
                  ref="lender_name"
                  variant="outline"
                  v-model="_lender.lender_name"
                  :placeholder="__('')"
                />
              </div>

              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Contact Name") }}
                </div>
                <TextInput
                  ref="lender_contact_name"
                  variant="outline"
                  v-model="_lender.lender_contact_name"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Address") }}
                </div>
                <TextInput
                  ref="lender_address"
                  variant="outline"
                  v-model="_lender.lender_address"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Type") }}
                </div>
                <TextInput
                  ref="lender_type"
                  variant="outline"
                  v-model="_lender.lender_type"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Notes") }}
                </div>
                <TextInput
                  ref="lender_notes"
                  variant="outline"
                  v-model="_lender.lender_notes"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Contact Phone") }}
                </div>
                <TextInput
                  ref="lender_contact_phone"
                  variant="outline"
                  v-model="_lender.lender_contact_phone"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Contact Email") }}
                </div>
                <TextInput
                  ref="lender_contact_email"
                  variant="outline"
                  v-model="_lender.lender_contact_email"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">{{ __("Funds CA") }}</div>
                <TextInput
                  ref="funds_ca"
                  variant="outline"
                  v-model="_lender.funds_ca"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">{{ __("Funds VA") }}</div>
                <TextInput
                  ref="funds_va"
                  variant="outline"
                  v-model="_lender.funds_va"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Max Funding") }}
                </div>
                <TextInput
                  ref="max_funding"
                  variant="outline"
                  v-model="_lender.max_funding"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">{{ __("Max Term") }}</div>
                <TextInput
                  ref="max_term"
                  variant="outline"
                  v-model="_lender.max_term"
                  :placeholder="__('')"
                />
              </div>
            </div>
            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Funds Trucking") }}
                </div>
                <TextInput
                  ref="funds_trucking"
                  variant="outline"
                  v-model="_lender.funds_trucking"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Funds Legal") }}
                </div>
                <TextInput
                  ref="funds_legal"
                  variant="outline"
                  v-model="_lender.funds_legal"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Funds Auto") }}
                </div>
                <TextInput
                  ref="funds_auto"
                  variant="outline"
                  v-model="_lender.funds_auto"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("TIB") }}
                </div>
                <TextInput
                  ref="tib"
                  variant="outline"
                  v-model="_lender.tib"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("MAX NSFS Per Month") }}
                </div>
                <TextInput
                  ref="max_nsfs_per_month"
                  variant="outline"
                  v-model="_lender.max_nsfs_per_month"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Min Fico") }}
                </div>
                <TextInput
                  ref="min_fico"
                  variant="outline"
                  v-model="_lender.min_fico"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Tier") }}
                </div>
                <TextInput
                  ref="tier"
                  variant="outline"
                  v-model="_lender.tier"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Funds Cut Pmts") }}
                </div>
                <TextInput
                  ref="funds_cut_pmts"
                  variant="outline"
                  v-model="_lender.funds_cut_pmts"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Funds Behind RAM") }}
                </div>
                <TextInput
                  ref="funds_behind_ram"
                  variant="outline"
                  v-model="_lender.funds_behind_ram"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Funds Behind Reverse") }}
                </div>
                <TextInput
                  ref="funds_behind_reverse"
                  variant="outline"
                  v-model="_lender.funds_behind_reverse"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Funds NonProfit") }}
                </div>
                <TextInput
                  ref="funds_behind_reverse"
                  variant="outline"
                  v-model="_lender.funds_non_profit"
                  :placeholder="__('')"
                />
              </div>
            </div>
          </div>
          <hr class="mt-4" />
          <h3 class="mt-2 mb-2">Email Settings</h3>
          <div class="secondgrid-container mt-2">
            <div class="grid-item">
              <div class="mb-1.5 text-sm text-gray-600">
                {{ __("Email Template") }}
              </div>
              <TextInput
                ref="email_template"
                variant="outline"
                v-model="_lender.email_template"
                :placeholder="__('')"
              />
            </div>
          </div>
        </template>
        <template v-else-if="tab.name === 'Contact & Address'">
          <h3 class="mt-2">Primary Address and Contact</h3>
          <div class="grid-container">
            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Primary Contact") }}
                </div>
                <TextInput
                  ref="lender_primary_contact"
                  variant="outline"
                  v-model="_lender.lender_primary_contact"
                  :placeholder="__('')"
                />
              </div>
            </div>

            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Primary Address") }}
                </div>
                <TextInput
                  ref="lender_primary_address"
                  variant="outline"
                  v-model="_lender.lender_primary_address"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lender Primary Address") }}
                </div>
                <Textarea
                  ref="primary_address"
                  variant="outline"
                  v-model="_lender.primary_address"
                  :placeholder="__('')"
                />
              </div>
            </div>
          </div>
        </template>
      </Tabs>
    </template>
    <template #actions>
      <div class="flex flex-row-reverse gap-2">
        <Button
          variant="solid"
          :label="__('Save')"
          :loading="isLeadCreating"
          @click="createNewLead"
        />
      </div>
    </template>
  </Dialog>
</template>

<script setup>
import { usersStore } from "@/stores/users";
import { statusesStore } from "@/stores/statuses";
import { computed, onMounted, ref, reactive } from "vue";
import { useRouter } from "vue-router";
import {
  createResource,
  FileUploader,
  Dropdown,
  Tooltip,
  Avatar,
  Tabs,
  Switch,
  Breadcrumbs,
  call,
} from "frappe-ui";
import Textarea from "frappe-ui/src/components/Textarea.vue";

const tabIndex = ref("Details");

const tabs = computed(() => {
  let tabOptions = [
    {
      name: "Details",
      label: __("Details"),
    },
    {
      name: "Contact & Address",
      label: __("Contact & Address"),
    },
  ];
  return tabOptions.filter((tab) => (tab.condition ? tab.condition() : true));
});
const { getUser } = usersStore();
const { getLeadStatus, statusOptions } = statusesStore();

const show = defineModel();
const router = useRouter();
const error = ref(null);
const isLeadCreating = ref(false);

const _lender = ref({
  lender_name: "",
  lender_contact_name: "",
  lender_address: "",
  lender_type: "",
  lender_notes: "",
  lender_contact_phone: "",
  lender_contact_email: "",
  funds_ca: "",
  funds_va: "",
  max_funding: "",
  max_term: "",
  funds_trucking: "",

  funds_legal: "",
  funds_auto: "",
  tib: "",
  max_nsfs_per_month: "",
  min_fico: "",
  tier: "",
  funds_cut_pmts: "",
  funds_behind_ram: "",
  funds_behind_reverse: "",
  funds_non_profit: "",
  email_template: "",
  lender_primary_contact: "",
  lender_primary_address: "",
  primary_address: "",
});
const activeTab = ref("");

function activeTabTrigger(trigger) {
  if (trigger === 0) {
    activeTab.value = "details";
    console.log(activeTab.value);
  } else {
    activeTab.value = "contacts";
  }
}

const createLead = createResource({
  url: "frappe.client.insert",
  makeParams(values) {
    return {
      doc: {
        doctype: "CRM Merchant",
        ...values,
      },
    };
  },
});

function createNewLead() {
  createLead.submit(_lender, {
    validate() {
      error.value = null;

      if (
        _lender.business_phone &&
        isNaN(_lender.business_phone.replace(/[-+() ]/g, ""))
      ) {
        error.value = "Mobile No should be a number";
        return error.value;
      }

      isLeadCreating.value = true;
    },
    onSuccess(data) {
      isLeadCreating.value = false;
      show.value = false;
      router.push({ name: "Lead", params: { leadId: data.name } });
    },
  });
  return { activeTab, activeTabTrigger };
}
</script>
<style>
.grid-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 10px;
}
.grid-item {
}
.secondgrid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
}
.tabs {
  display: flex;
}
.tab {
  padding: 10px 15px;
  cursor: pointer;
}
.tab.active {
  background-color: #f0f0f0;
}
.tab-content {
  display: none;
}
.tab-content.active {
  display: block;
}
</style>
