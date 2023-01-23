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
        projects: Array,
    },
    setup(props) {
        const period = ref(props.period)
        const company = ref(props.company)
        const role = ref(props.role)
        const roleDescription = ref (props.roleDescription)
        const tasks = ref(props.tasks)
        const projects = ref(props.projects)

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
        
        <div class="content">
            <div>
                <div>
                    <div style="display: inline-block;">
                        <strong>{{ company }}</strong> <br> 
                        <strong>{{ role }}</strong> <br>
                    </div>
                    <div style="display: inline-block; margin: 10px;">
                        <strong>{{ period }}</strong>
                    </div>
                </div>
                
                {{ roleDescription }}
            </div>
            <br>
            <template v-if="projects">Projects:</template>
            <ul>
                <li class="job_item" v-for="item in projects">{{ item }}</li>
            </ul>
            <template v-if="tasks">Duties:</template>
            <ul>
                <li class="job_item" v-for="item in tasks">{{ item }}</li>
            </ul>
        </div>
        <!-- <div class="year">{{ period }}</div> -->
        <!-- <div class="year"></div> -->
    </div>
</template>