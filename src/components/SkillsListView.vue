<script>
	import SkillBarItem from './SkillBarItem.vue';
	export default {
		name: "SkillsListView",
		components: {
			SkillBarItem,
		}
	}
</script>

<template>
    <div class="resume_item resume_skills">

        <div class="resume_title">Skills</div>
        <div class="resume_info skill_container">
            <div class="skill_list">
                <!-- Left side -->
                <ul>
                    <li>Python</li>
                    <li>Javascript</li>
                    <li>Rust</li>
                    <li>Linux</li>
                </ul>
            </div>
            <div class="skill_list">
                <!-- Right side -->
                <ul>
                    <li>HTML</li>
                    <li>CSS</li>
                    <li>Vue 3</li>
                </ul>
            </div>
        </div>
        <br />
        <div class="resume_title">Skills Embedded Systems</div>
        <div class="resume_info skill_container">
            <div class="skill_list">
                <!-- Left side -->
                <ul>
                    <li>C</li>
                    <li>C++</li>
                    <li>STM32</li>
                    <li>I2C</li>
                    <li>SPI</li>
                    <li>Arduino</li>
                    
                </ul>
            </div>
            <div class="skill_list">
            <!-- Right side -->
                <ul>
                    
                    <li>CANbus</li>
                    <li>RTOS</li>
                    <li>Canalyzer</li>
                    <li>CAPL</li>
                    <li>FMEA</li>
                    <li>TARA</li>
                    <li>Requirements</li>
                </ul>
            </div>
        </div>
        <br />
        <div class="resume_title">Licenses</div>
        <div class="resume_info skill_container">
            <div class="skill_list">
                <!-- Left side -->
                <ul>
                    <li>Heavy Truck</li>
                </ul>
            </div>
            <div class="skill_list">
            <!-- Right side -->
                <ul>
                    <li>Car</li>
                </ul>
            </div>
        </div>
	</div>
</template>

<style scoped>
    .skill_container {
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
    }
    .skill_list {
        flex-shrink: 0;
        margin-left: 0;
        margin-right: auto;
    }
</style>