<script>
  import SkillsListView from './components/SkillsListView.vue'
  import ContactDetails from './components/ContactDetails.vue'
  import TimelineItem from './components/TimelineItem.vue'

  export default {
    components: {
      SkillsListView,
      ContactDetails,
      TimelineItem,
    }
  }
</script>

<template>
  <div class="resume_wrapper">
	<div class="resume_left">
		<div class="resume_image">
			<img src="./assets/pic2.jpg" alt="Resume_image">
		</div>
		<div class="resume_bottom">
			<div class="resume_item resume_namerole">
				<div class="name">Martin Pålsson</div>
				<div class="role">Software engineer</div>
			</div>
      <!-- Profile introduction -->
			<div class="resume_item resume_profile">
				<div class="resume_title">Profile</div>
				<div class="resume_info">
          Engineer with a strong sense of ownership and will to deliver.
          <br>
          <br>
          Born 1989. Grew up on a farm. I'm used to heavy duty work, machinery and long days.
          <br>
          <br>
          I love to automate chores, decrease "friction" in reoccuring tasks, and leave a trail of useful documentation.
        </div>
			</div>

			<!-- Contact details -->
      <ContactDetails telephone-number="+46 706 26 49 90" email-address="martin.palsson@outlook.com"/>
			<!-- Skills -->
      <SkillsListView />
		</div>
	</div>
	<div class="resume_right">
		<div class="resume_item resume_namerole">
			<div class="name">Martin Pålsson</div>
			<div class="role">Software engineer</div>
		</div>
		<div class="resume_item resume_education">
			<div class="resume_title">Career summary</div>
			<div class="resume_info">
				<TimelineItem 
          period="2020 - 2022" 
          company="Scania CV AB" 
          role="System Owner"
          role-description="System- and product ownership bodywork interface"
          :tasks="[
            'Lead team activities Backlog refinement, sprint planning', 
            'Release coordination and planning',
            'Conducted TARA (Threat Analysis and Risk Assessment)',
            'Continious work on FMEA (Failure Mode and Risk Assessment)',
            'Validation of SW in vehicle and on bench',
            ]"
        />
        <TimelineItem 
          period="2018 - 2020" 
          company="Scania CV AB" 
          role="Function owner"
          role-description="As a function owner, I managed and lead the development of a number of features related to 
							the bodywork interface, that provides the ability for third part to adapt the bodywork interface
							to the purpose of the vehicles. It mainly consists of a PLC-like ECU (for discrete interfaces)
							and a CAN-based API."
          :tasks="[
            'Development of telematics solution for bodyworks', 
            'Development of HMI functions for bodywork',
            'Development of enhancements to the PLC-like programming language for the discrete bodywork interface',
            'Development of control function for electrical power take off',
            'User requirements elicitation and breakdown',
            'Planning, and documenting architectural changes of user functions',
            'Planning, and documenting signal flows over serial interfaces (CAN, J1939)',
            'Developed production firmware, in C',
            'Validation of cross functional software features in vehicle and on test bench',
            'Development of control panels and other CAPL scripts in Canalyzer',
            ]"
        />
        <TimelineItem 
          period="2017 - 2018" 
          company="InContext AB" 
          role="Development engineer, Consultant"
          role-description="Software development for automotive embedded systems"
          :tasks="[
            'Adapted application layer to be independent of powertrain type (Combustion / HEV / BEV)',
            'Documentation and requirements development',
            'Test automation, test scripts in Python',
            ]"
        />
        <!-- <TimelineItem 
          period="2016" 
          company="ABB" 
          role="Assembly line worker"
          role-description="Assembly of high power contactors"
        />
        <TimelineItem 
          period="2015 - 2016" 
          company="Academic Work" 
          role="Warehouse worker"
          role-description="Side job while attending KTH"
        /> -->
        <TimelineItem 
          period="2008 - 2009, 2012 - 2014" 
          company="NärkeÄgg AB" 
          role="Teamlead"
          role-description="Teamlead for an egg grading team of 5 members"
          :tasks="[
            'Operational planning of production, daily deadlines for delivery',
            'Accountability',
            'Established work station instructions',
            'Training of new team members',
            'Repair and maintenance of egg grading equipment and facility',
            'Installation of new equipment',
            ]"
        />
				
			</div>
		</div>
		<div class="resume_item resume_experience">
			<div class="resume_title">Education</div>
			<div class="resume_info">
        <TimelineItem 
          period="2017" 
          role="Won swedish championship in robotic sumo (mini/500g class)"
          :tasks="[
            'PCB-design, KiCAD',
            '3d-modeling, Autodesk Fusion 360',
            'Arduino',
            ]"
        />
        <TimelineItem 
          period="2014 - 2017" 
          company="KTH - Royal Institute of Technology" 
          role="BSc. Mechanical enginering - Robotics and Mechatronics"
          role-description="No diploma"
        />
        <TimelineItem 
          period="2009 - 2012" 
          company="SLU - Swedish University of Agriculture" 
          role="Forestry science"
          role-description="120p Forestry science"
        />				
			</div>
		</div>
	</div>
</div>
</template>
