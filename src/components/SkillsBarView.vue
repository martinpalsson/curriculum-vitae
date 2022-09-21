<script>
	import SkillBarItem from './SkillBarItem.vue';
	export default {
		name: "SkillsBarView",
		components: {
			SkillBarItem,
		}
	}
</script>

<template>
    <div class="resume_item resume_skills">
		<div class="resume_title">Skills</div>
		<div class="resume_info">
			<SkillBarItem skill-name="C" 		 :proficiency="100" />
			<SkillBarItem skill-name="C++" 		 :proficiency="60" />
			<SkillBarItem skill-name="C#" 		 :proficiency="75" />
			<SkillBarItem skill-name="Python" 	 :proficiency="85" />
			<SkillBarItem skill-name="PlantUML"  :proficiency="75" />
			<SkillBarItem skill-name="Canalyzer" :proficiency="75" />
		</div>
	</div>
</template>