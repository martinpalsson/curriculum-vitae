<script>
    import { ref } from 'vue';
    export default{
        name: "ContactDetails",
        props: {
            telephoneNumber: String,
            emailAddress: String,
            github: String,
        },
        setup(props) {
            const emailAddress = ref(props.emailAddress)
            const telephoneNumber = ref(props.telephoneNumber)
            const github = ref(props.github)
            return {
                emailAddress: emailAddress,
                telephoneNumber: telephoneNumber,
                github: github,
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
    <div class="resume_info">
        <div class="resume_subtitle">Github</div>
        <div class="resume_subinfo">{{ github }}</div>
    </div>
</div>
</template>