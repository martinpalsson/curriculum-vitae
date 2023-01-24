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
            tasks:tasks,
            projects:projects
        }
    }
}
</script>

<template>
    <div class="resume_data">
        
        <div class="content">
            <div>
                <div style="display: flex">
                    <div style="display: inline-block; width: 80%; float: left; position: relative;">
                        <strong>{{ company }}</strong> <br> 
                        <strong>{{ role }}</strong> <br>
                    </div>
                    <div style="display: inline-block; width: 20%; float: left; position: relative;">
                        <strong>{{ period }}</strong>
                    </div>
                </div>
                
                {{ roleDescription }}
            </div>
            <br>
            <h4 v-if="projects">Projects:</h4>
            <ul>
                <li class="job_item" v-for="item in projects">{{ item }}</li>
            </ul>
            <h4 style="margin-top: 5px;" v-if="tasks">Duties:</h4>
            <ul>
                <li class="job_item" v-for="item in tasks">{{ item }}</li>
            </ul>
        </div>
    </div>
</template>