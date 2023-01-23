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
        <div class="resume_title">General</div>
        <div class="resume_info skill_container">
            <div class="skill_list">
                <!-- Left side -->
                <ul>
                    <li>Python</li>
                    <li>Rust</li>
                    <li>Docker</li>
                    <li>Linux</li>
                    <li>GIT</li>
                    <li>Perforce</li>
                </ul>
            </div>
            <div class="skill_list">
                <!-- Right side -->
                <ul>
                    <li>HTML</li>
                    <li>CSS</li>
                    <li>Javascript</li>
                    <li>Vue 3</li>
                    <li>Django</li>
                    <li>Django REST Framework</li>
                </ul>
            </div>
        </div>
        <br />
        <div class="resume_title">Embedded Systems</div>
        <div class="resume_info skill_container">
            <div class="skill_list">
                <!-- Left side -->
                <ul>
                    <li>C</li>
                    <li>C++</li>
                    <li>RTOS</li>
                    <li>STM32</li>
                    <li>I2C</li>
                    <li>SPI</li>
                    
                </ul>
            </div>
            <div class="skill_list">
            <!-- Right side -->
                <ul>
                    
                    <li>CAN</li>
                    
                    <li>Canalyzer</li>
                    <li>CAPL</li>
                    <li>FMEA</li>
                    <li>TARA</li>
                    <li>Requirements</li>
                </ul>
            </div>
        </div>
        <br />
        <div class="resume_title">Miscellaneous</div>
        <div 
            class="resume_info skill_container"
            style="overflow-wrap: break-word;"
            >
            <div class="skill_list">
                <!-- Left side -->
                <ul>
                    <li>Drivers license commercial truck</li>
                    <li>Drivers license car</li>
                    <li>Swedish Champion Robotic mini-sumo 2017</li>
                </ul>
            </div>
            <div class="skill_list">
            <!-- Right side -->
                <ul>
                    
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