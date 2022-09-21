<script>
import { ref } from 'vue';
export default{
    name: "TimelineItem",
    props: {
        period: String,
        company: String,
        role: String,
        roleDescription: String,
        tasks: Array,
    },
    setup(props) {
        const period = ref(props.period)
        const company = ref(props.company)
        const role = ref(props.role)
        const roleDescription = ref (props.roleDescription)
        const tasks = ref(props.tasks)

        return {
            period: period,
            company: company,
            role: role,
            roleDescription: roleDescription,
            tasks:tasks
        }
    }
}
</script>

<template>
    <div class="resume_data">
        <div class="year">{{ period }}</div>
        <div class="content">
            <p>
                <strong>{{ company }}</strong> <br> 
                <strong>{{ role }}</strong> <br>
                {{ roleDescription }}

            </p>
            <br>
            <ul>
                <li class="job_item" v-for="item in tasks">{{ item }}</li>
            </ul>
        </div>
    </div>
</template>