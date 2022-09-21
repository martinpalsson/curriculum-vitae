<script>
    import { ref } from 'vue';
    export default{
        name: "ContactDetails",
        props: {
            telephoneNumber: String,
            emailAddress: String,
        },
        setup(props) {
            const emailAddress = ref(props.emailAddress)
            const telephoneNumber = ref(props.telephoneNumber)

            return {
                emailAddress: emailAddress,
                telephoneNumber: telephoneNumber,
            }
        }
    }
</script>

<template>
<div class="resume_item resume_contact">
    <div class="resume_title">Contact details</div>
    <div class="resume_info">
        <div class="resume_subtitle">Telephone</div>
        <div class="resume_subinfo">{{ telephoneNumber }}</div>
    </div>
    <div class="resume_info">
        <div class="resume_subtitle">Email</div>
        <div class="resume_subinfo">{{ emailAddress }}</div>
    </div>
</div>
</template>