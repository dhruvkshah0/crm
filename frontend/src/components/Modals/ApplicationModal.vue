<template>
  <Dialog
    v-model="show"
    :options="{
      size: '3xl',
      title: __('New Application'),
    }"
  >
    <template #body-content>
      <div class="mb-1.5 mt-3 text-sm text-gray-600">
        {{ __('Application ID') }}
      </div>
      <TextInput
        ref="merchant_notes"
        variant="outline"
        v-model="_merchant.merchant_notes"
        :placeholder="__('')"
      />
      <div class="secondgrid-container mt-2">
        <div class="grid-item">
          <div class="mb-1.5 mt-3 text-sm text-gray-600">
            {{ __('Full Name') }}
          </div>
          <TextInput
            ref="merchant_notes"
            variant="outline"
            v-model="_merchant.merchant_notes"
            :placeholder="__('')"
          />
        </div>
        <div class="grid-item">
          <div class="mb-1.5 mt-3 text-sm text-gray-600">
            {{ __('Merchant ID') }}
          </div>
          <TextInput
            ref="category"
            variant="outline"
            v-model="_merchant.category"
            :placeholder="__('')"
          />
        </div>
        <div class="grid-item">
          <div class="mb-1.5 mt-3 text-sm text-gray-600">
            {{ __('Merchant Name') }}
          </div>
          <TextInput
            ref="created_datetime"
            variant="outline"
            v-model="_merchant.created_datetime"
            :placeholder="__('')"
          />
        </div>
      </div>
      <h3 class="mt-2 mb-2">Application Information</h3>

      <div class="grid-container">
        <div class="grid-item">
          <div>
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Sales Assistant Assigned') }}
            </div>
            <TextInput
              ref="first_name"
              variant="outline"
              v-model="_merchant.first_name"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Federal Tax ID') }}
            </div>
            <TextInput
              ref="last_name"
              variant="outline"
              v-model="_merchant.last_name"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Ownership Start Date') }}
            </div>
            <TextInput
              ref="full_name"
              variant="outline"
              v-model="_merchant.full_name"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Ownership End Date') }}
            </div>
            <TextInput
              ref="personal_phone"
              variant="outline"
              v-model="_merchant.personal_phone"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Entity Type') }}
            </div>
            <TextInput
              ref="email"
              variant="outline"
              v-model="_merchant.email"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Type of Business') }}
            </div>
            <TextInput
              ref="ein"
              variant="outline"
              v-model="_merchant.ein"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Product/Service Sold') }}
            </div>
            <TextInput
              ref="ein"
              variant="outline"
              v-model="_merchant.ein"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('What percent of the business do you own?') }}
            </div>
            <TextInput
              ref="ein"
              variant="outline"
              v-model="_merchant.ein"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Amount Request') }}
            </div>
            <TextInput
              ref="ein"
              variant="outline"
              v-model="_merchant.ein"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Merchant Website') }}
            </div>
            <TextInput
              ref="ein"
              variant="outline"
              v-model="_merchant.ein"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Phone Number') }}
            </div>
            <TextInput
              ref="ein"
              variant="outline"
              v-model="_merchant.ein"
              :placeholder="__('')"
            />
          </div>

          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Owner Name') }}
            </div>
            <TextInput
              ref="ein"
              variant="outline"
              v-model="_merchant.ein"
              :placeholder="__('')"
            />
          </div>
        </div>

        <div class="grid-item">
          <div>
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Address') }}
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
              {{ __('State/Province') }}
            </div>
            <TextInput
              ref="business_phone"
              variant="outline"
              v-model="_merchant.business_phone"
              :placeholder="__('')"
            />
          </div>
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('ZIP/Postal Code') }}
            </div>
            <TextInput
              ref="business_email"
              variant="outline"
              v-model="_merchant.business_email"
              :placeholder="__('')"
            />
          </div>
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Date of Birth') }}
            </div>
            <TextInput
              ref="application"
              variant="outline"
              v-model="_merchant.application"
              :placeholder="__('')"
            />
          </div>
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Social Security') }}
            </div>
            <TextInput
              ref="nurture"
              variant="outline"
              v-model="_merchant.nurture"
              :placeholder="__('')"
            />
          </div>
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Application Datetime') }}
            </div>
            <TextInput
              ref="nurture"
              variant="outline"
              v-model="_merchant.nurture"
              :placeholder="__('')"
            />
          </div>
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Agent Assigned') }}
            </div>
            <TextInput
              ref="nurture"
              variant="outline"
              v-model="_merchant.nurture"
              :placeholder="__('')"
            />
          </div>
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Top Categories of Merchant') }}
            </div>
            <TextInput
              ref="nurture"
              variant="outline"
              v-model="_merchant.nurture"
              :placeholder="__('')"
            />
          </div>
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Merchant Business Description') }}
            </div>
            <TextInput
              ref="nurture"
              variant="outline"
              v-model="_merchant.nurture"
              :placeholder="__('')"
            />
          </div>
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">{{ __('Funded') }}</div>
            <TextInput
              ref="nurture"
              variant="outline"
              v-model="_merchant.nurture"
              :placeholder="__('')"
            />
          </div>
        </div>
      </div>
      <hr class="mt-2" />
      <h3 class="mt-2 mb-2">Deal Shopping</h3>
      <div class="grid-container">
     <div class="grid-item">
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Lender') }}
            </div>
            <TextInput
              ref="first_name"
              variant="outline"
              v-model="_merchant.first_name"
              :placeholder="__('')"
            />
          </div>
        </div>
        <div class="grid-item">
          <div class="mt-2">
            <div class="mb-1.5 text-sm text-gray-600">
              {{ __('Document') }}
            </div>
            <TextInput
              ref="first_name"
              variant="outline"
              v-model="_merchant.first_name"
              :placeholder="__('')"
            />
          </div>
        </div>
      </div>

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
import { usersStore } from '@/stores/users'
import { statusesStore } from '@/stores/statuses'
import { createResource } from 'frappe-ui'
import { computed, onMounted, ref, reactive } from 'vue'
import { useRouter } from 'vue-router'

const { getUser } = usersStore()
const { getLeadStatus, statusOptions } = statusesStore()

const show = defineModel()
const router = useRouter()
const error = ref(null)
const isLeadCreating = ref(false)

const _merchant = ref({
  first_name: '',
  last_name: '',
  full_name: '',
  personal_phone: '',
  email: '',
  ein: '',
  business_legal_name: '',
  business_phone: '',
  business_email: '',
  application: '',
  nurture: '',
  merchant_notes: '',
  category: '',
  created_datetime: '',
})


const createLead = createResource({
  url: 'frappe.client.insert',
  makeParams(values) {
    return {
      doc: {
        doctype: 'CRM Merchant',
        ...values,
      },
    }
  },
})

function createNewLead() {
  createLead.submit(_merchant, {
    validate() {
      error.value = null
      if (!_merchant.full_name) {
        error.value = 'Full Name is mandatory'
        return error.value
      }

      if (
        _merchant.business_phone &&
        isNaN(_merchant.business_phone.replace(/[-+() ]/g, ''))
      ) {
        error.value = 'Mobile No should be a number'
        return error.value
      }

      isLeadCreating.value = true
    },
    onSuccess(data) {
      isLeadCreating.value = false
      show.value = false
      router.push({ name: 'Lead', params: { leadId: data.name } })
    },
  })
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
