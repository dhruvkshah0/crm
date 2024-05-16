<template>
  <Dialog
    v-model="show"
    :options="{
      size: '3xl',
      title: __('New CRM Lead'),
    }"
  >
    <template #body-content>
      <Tabs v-model="tabIndex" v-slot="{ tab }" :tabs="tabs" height="">
        <template v-if="tab.name === 'Details'">
          <div class="grid-container">
            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Organization") }}
                </div>
                <TextInput
                  ref="organization"
                  variant="outline"
                  v-model="_merchant.organization"
                  :placeholder="__('')"
                />
              </div>

              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Website") }}
                </div>
                <TextInput
                  ref="website"
                  variant="outline"
                  v-model="_merchant.website"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Territory") }}
                </div>
                <TextInput
                  ref="territory"
                  variant="outline"
                  v-model="_merchant.territory"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Industry") }}
                </div>
                <TextInput
                  ref="industry"
                  variant="outline"
                  v-model="_merchant.industry"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Job Title") }}
                </div>
                <TextInput
                  ref="job_title"
                  variant="outline"
                  v-model="_merchant.job_title"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Source") }}
                </div>
                <TextInput
                  ref="source"
                  variant="outline"
                  v-model="_merchant.source"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Lead Owner") }}
                </div>
                <TextInput
                  ref="lead_owner"
                  variant="outline"
                  v-model="_merchant.lead_owner"
                  :placeholder="__('')"
                />
              </div>
            </div>
          </div>
        </template>
        <template v-if="tab.name === 'Person'">
          <div class="grid-container">
            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("First Name") }}
                </div>
                <TextInput
                  ref="first_name"
                  variant="outline"
                  v-model="_merchant.first_name"
                  :placeholder="__('John')"
                />
              </div>

              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Last Name") }}
                </div>
                <TextInput
                  ref="last_name"
                  variant="outline"
                  v-model="_merchant.last_name"
                  :placeholder="__('Doe')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Full Name") }}
                </div>
                <TextInput
                  ref="full_name"
                  variant="outline"
                  v-model="_merchant.full_name"
                  :placeholder="__('John Doe')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Personal Phone") }}
                </div>
                <TextInput
                  ref="personal_phone"
                  variant="outline"
                  v-model="_merchant.personal_phone"
                  :placeholder="__('+91 9898987888')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">{{ __("Email") }}</div>
                <TextInput
                  ref="email"
                  variant="outline"
                  v-model="_merchant.email"
                  :placeholder="__('abc@gmail.com')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">{{ __("EIN") }}</div>
                <TextInput
                  ref="ein"
                  variant="outline"
                  v-model="_merchant.ein"
                  :placeholder="__('')"
                />
              </div>
            </div>
            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Business Legal Name") }}
                </div>
                <TextInput
                  ref="business_legal_name"
                  variant="outline"
                  v-model="_merchant.business_legal_name"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Business Phone") }}
                </div>
                <TextInput
                  ref="business_phone"
                  variant="outline"
                  v-model="_merchant.business_phone"
                  :placeholder="__('+91 9878989898')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Business Email") }}
                </div>
                <TextInput
                  ref="business_email"
                  variant="outline"
                  v-model="_merchant.business_email"
                  :placeholder="__('abc@gmail.com')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Application") }}
                </div>
                <TextInput
                  ref="application"
                  variant="outline"
                  v-model="_merchant.application"
                  :placeholder="__('')"
                />
              </div>
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">{{ __("Nurture") }}</div>
                <TextInput
                  ref="nurture"
                  variant="outline"
                  v-model="_merchant.nurture"
                  :placeholder="__('')"
                />
              </div>
            </div>
          </div>
        </template>

        <template v-if="tab.name === 'Others'">
          <div class="grid-container">
            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Series") }}
                </div>
                <TextInput
                  ref="series"
                  variant="outline"
                  v-model="_merchant.series"
                  :placeholder="__('')"
                />
              </div>

              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Full Name") }}
                </div>
                <TextInput
                  ref="full_name_others"
                  variant="outline"
                  v-model="_merchant.full_name_others"
                  :placeholder="__('')"
                />
              </div>

              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Middle Name") }}
                </div>
                <TextInput
                  ref="middle_name"
                  variant="outline"
                  v-model="_merchant.middle_name"
                  :placeholder="__('')"
                />
              </div>

              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Gender") }}
                </div>
                <TextInput
                  ref="gender"
                  variant="outline"
                  v-model="_merchant.gender"
                  :placeholder="__('')"
                />
              </div>

              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Phone") }}
                </div>
                <TextInput
                  ref="phone"
                  variant="outline"
                  v-model="_merchant.phone"
                  :placeholder="__('')"
                />
              </div>
            </div>
            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Status") }}
                </div>
                <TextInput
                  ref="status"
                  variant="outline"
                  v-model="_merchant.status"
                  :placeholder="__('New')"
                />
              </div>

              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("No. Of Employees") }}
                </div>
                <TextInput
                  ref="no_of_employees"
                  variant="outline"
                  v-model="_merchant.no_of_employees"
                  :placeholder="__('')"
                />
              </div>

              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Annual Revenue") }}
                </div>
                <TextInput
                  ref="annual_revenue"
                  variant="outline"
                  v-model="_merchant.annual_revenue"
                  :placeholder="__('')"
                />
              </div>
            </div>
          </div>
        </template>

        <template v-if="tab.name === 'SLA'">
          <div class="grid-container">
            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("SLA") }}
                </div>
                <TextInput
                  ref="sla"
                  variant="outline"
                  v-model="_merchant.sla"
                  :placeholder="__('')"
                />
              </div>
            </div>

            <div class="grid-item">
              <div class="mt-2">
                <div class="mb-1.5 text-sm text-gray-600">
                  {{ __("Communication Status") }}
                </div>
                <TextInput
                  ref="communication_status"
                  variant="outline"
                  v-model="_merchant.communication_status"
                  :placeholder="__('')"
                />
              </div>
            </div>
          </div>
        </template>
      </Tabs>

      <ErrorMessage class="mt-4" v-if="error" :message="__(error)" />
    </template>
    <template #actions>
      <div class="flex flex-row-reverse gap-2">
        <Button
          variant="solid"
          :label="__('Create')"
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
import { Tabs, createResource } from "frappe-ui";
import { computed, onMounted, ref, reactive } from "vue";
import { useRouter } from "vue-router";

const { getUser } = usersStore();
const { getLeadStatus, statusOptions } = statusesStore();

const show = defineModel();
const router = useRouter();
const error = ref(null);
const isLeadCreating = ref(false);

const _merchant = ref({
  first_name: "",
  last_name: "",
  full_name: "",
  personal_phone: "",
  email: "",
  ein: "",
  business_legal_name: "",
  business_phone: "",
  business_email: "",
  application: "",
  nurture: "",
  merchant_notes: "",
  category: "",
  created_datetime: "",
  organization: "",
  website: "",
  territory: "",
  industry: "",
  job_title: "",
  source: "",
  lead_owner: "",

  series: "",
  full_name_others: "",
  middle_name: "",
  gender: "",
  phone: "",
  status: "New",
  no_of_employees: "",
  annual_revenue: "",

  sla: "",
  communication_status: "Open",
});

const tabIndex = ref("Details");
const tabs = computed(() => {
  let tabOptions = [
    {
      name: "Details",
      label: __("Details"),
    },
    {
      name: "Person",
      label: __("Person"),
    },
    {
      name: "Others",
      label: __("Others"),
    },
    {
      name: "SLA",
      label: __("SLA"),
    },
    {
      name: "Log",
      label: __("Log"),
    },
    {
      name: "Applications",
      label: __("Applications"),
    },
  ];
  return tabOptions.filter((tab) => (tab.condition ? tab.condition() : true));
});

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
  createLead.submit(_merchant, {
    validate() {
      error.value = null;
      if (!_merchant.full_name) {
        error.value = "Full Name is mandatory";
        return error.value;
      }

      if (
        _merchant.business_phone &&
        isNaN(_merchant.business_phone.replace(/[-+() ]/g, ""))
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
</style>
