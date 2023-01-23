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
			<!-- <div class="resume_item resume_profile">
				<div class="resume_title">Profile</div>
				<div class="resume_info">
          Hello
        </div>
			</div> -->

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
          period="2018 - Now" 
          company="Scania CV AB" 
          role="Development engineer"
          role-description="Was reqruited to the role of Function Owner, 
              with responsibility of the external interfaces (network based + I/O based).
              My responsibilities also included a PLC-like programmable unit allowing third party to define limited functionality in the external interface,
              such as activating Power Take Off, Engine Control or interacting with the driver via Switches or Telltales.
              Took over ownership of more functions as time passed. 
              Promoted to System Owner in 2020, which can be compared to product owner mixed with limited release train engineer duties. I did keep the Function owner duties.
               "
          :projects="[
            'Telematics solution and HMI functions for bodyworks', 
            'Scania Zone, geofencing functionality',
            'Major update of PLC-like domain specific language',
            'Control function and interface for electrical power take off',
            'Cost-reduction by replacing discrete switches to network-based pushbuttons',
            'Introducing new variants of ECU-hardware due to lack of semi-conductors',
          ]"
          :tasks="[
            'Planned and documented architectural changes of user functions, signal flows over network interfaces (CAN, J1939)',
            'Coordinated development with other groups at Scania',
            'Developed and verified requirements',
            'Developed production software in C',
            'Validated software in vehicle and on test bench',
            'Developed tools in C# and Python, ',
            'Developed control panels and other scripts in Canalyzer (CAPL)',
            'Planned and coordinated releases',
            'Onboarded and tutored new coworkers',
            'Supported sales, and Global Technical Support',
            'Responded to and developed solutions for problems found in operating vehicles, and vehicles in the process of being purpose-adapted by third party.',
            'Lead agile activities Backlog refinement and Sprint Planning', 
            'Continious work on FMEA (Failure Mode and Risk Assessment)',
            'Conducted TARA (Threat Analysis and Risk Assessment)',
            ]"
        />
        <TimelineItem 
          period="2017 - 2018" 
          company="InContext AB" 
          role="Development engineer, Consultant"
          role-description="Software development for automotive embedded systems"
          :projects="[
            'Adapted application layer to be independent of powertrain type (Combustion / HEV / BEV)',
            'Introduce new generation electrical system in bus',
            ]"
          :tasks="[
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
        <!-- <TimelineItem 
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
        /> -->
				
			</div>
		</div>
		<div class="resume_item resume_experience">
			<div class="resume_title">Education</div>
			<div class="resume_info">
        <TimelineItem 
          period="2014 - 2017" 
          company="KTH - Royal Institute of Technology" 
          role="H.ing Maskinteknik - Robotics and Mechatronics"
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
