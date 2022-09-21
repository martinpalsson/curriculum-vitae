<script>
    import { ref } from 'vue';
export default{
    name: "SkillBarItem",
    props: {
        skillName: String,
        proficiency: Number,
    },
    setup(props) {
        const profPercent = ref(Number)
        const skillName = ref("")

        profPercent.value = props.proficiency
        skillName.value = props.skillName

        return {
            skillName: skillName,
            profPercent: profPercent,
        }
    }
}
</script>

<template>
    <div class="skills_list">
        <div class="skills_left">{{ skillName }}</div>
        <div class="skills_bar">
            <p>
                <span :style="{ width: profPercent + '%' }"></span>
            </p>
        </div>
    </div>
</template>