---
layout : joalayout
title : Calculate Parameters
css: joa
---
<center>
	<div id="container" class="tour page  row-fluid" style="max-width:125vh;text-align:left;">
		<div id="main_content" class="contained span8">
			<div id="top"></div>
			<div id="guided_tour" style="font-family:verdana;">
				<h1>Guided Tour of Java OceanAtlas </h1>
				<h2>{{page.title}}</h2>
				<div id="guided_tour_content">
					<p>Oceanographers use parameters calculated from the data to aid interpretation. Java OceanAtlas provides means to calculate a wide range of these derived variables. Calculated parameters are usually re-calculated each time the data set is opened. This is usually not a problem because parameter calculations in OceanAtlas are completed easily and quickly. Selecting 'Parameters...' from the Calculations menu brings up the Parameter Calculations dialog box (Figure 8).</p> <img alt="Gt_fig-08" class="gt_image" src="assets/images/fig8.png">
					<p>In the dialog box in Figure 8 we have already selected the options to calculate the two parameters used most often by physical oceanographers: potential temperature and a density-related parameter called 'sigma-0' or 'sigma-theta'.</p>
					<p class="oceanography_text" style="padding-left:35px;">Potential temperature, written as 'Θ' or 'θ' and therefore often called 'theta' by oceanographers (and abbreviated as THTA internally in Java OceanAtlas) is the temperature a seawater sample would have if raised adiabatically from its collection level ('in situ') to the sea surface. (In fully correct parlance this is 'potential temperature with respect to zero decibars'.) The reason we use potential temperature can be illustrated by this example: If a seawater parcel descends into the deep ocean - perhaps because it entered from a peripheral region where it obtained a higher density than the ambient water in the region it entered - it is slightly heated by compression (by a little less than 0.1'C/1000 db increase in pressure). To properly compare temperatures of seawater samples from different pressures we should reference their temperatures to the same isobar. Zero decibars is the level of choice, though for density calculations potential temperature is calculated (automatically in Java OceanAtlas) with respect to the reference pressure chosen for the density calculation.</p>
					<p class="oceanography_text" style="padding-left:35px;">At this time oceanographers do not have generally available a satisfactory routine methodology for directly measuring density in situ with the accuracy and precision required for ocean circulation and mixing studies. So for many years oceanographers have calculated density based on seawater properties. Oceanographers are interested in the density of seawater for a number of reasons. For example, it is an important consideration in ocean mixing because it is easier to mix water along a surface of constant density (an 'isopycnal') rather than across it. [Consider the difference in work: To a first approximation it takes no work to mix along an isopycnal whereas it does require work to mix across one.] And oceanographers have learned that on a rotating Earth the relative motion of one seawater layer with respect to another sets up small-but-important slopes of isopycnal surfaces with respect to isobaric ones, meaning that by studying the slopes of isopycnal surfaces (and other related dynamic surfaces) we can infer much about ocean circulation.</p>
					<p class="oceanography_text" style="padding-left:35px;">The density of seawater is a nonlinear function of its pressure, temperature, and salinity. To properly compare seawater samples one should reference their densities to the same isobar. Zero decibars (the sea surface) is the most common choice, but due to nonlinearities in the equation of state for seawater it is also common to use deeper reference levels, i.e. reference levels appropriate to the situations under examination.</p>
					<p class="oceanography_text" style="padding-left:35px;">The density of a seawater sample with pressure = 0 db, TEMP = 0&deg;C, and salinity = 35 would be 1028.106 kg m&#179;. Oceanographers subtract '1000' from density as a form of short hand and call this 'sigma' units. When the reference level is zero decibars this becomes 'sigma-0' or sometimes 'sigma-theta' (two names for the same term; SIG0 internally in Java OceanAtlas). Thus our '0, 0, 35' sample - which is already at the reference pressure of 0 decibars - has sigma-0 = 28.106.</p>
					<p>Select 'Parameters...' from the Calculations menu. Click on the boxes for theta and sigma-0 (this is shown in Figure 8), then click 'OK'. The computer will rapidly complete the calculations. When it is done you will notice that the Data Window now shows these two parameters, because these have now been calculated and temporarily stored for every sample in the section.</p>
				</div>
			</div>
		</div>
		<div id="right" class="span4">
			<h1>Guided Tour of Java OceanAtlas</h1>
			<ul>
				<li><a href="basic_features.html">Basic Features</a></li>
				<li><a href="starting_joa.html">Starting JOA</a></li>
				<li><a href="station_maps.html">Station Maps</a></li>
				<li><a href="profile_plots.html">Profile Plots</a></li>
				<li><a href="changing_color_bar.html">Changing Color/Contour Bar</a></li>
				<li class="active"><a href="calculate_parameters.html">Calculate Parameters</a></li>
				<li><a href="property_plots.html">Property-Property Plots</a></li>
				<li><a href="browsing.html">Browsing</a></li>
				<li><a href="modifying_plots.html">Modifying Plots</a></li>
				<li><a href="extracting_selections.html">Extracting Selections</a></li>
				<li><a href="contour_plots.html">Contour Plots</a></li>
				<li><a href="other_features.html">Other Features</a></li>
				<li><a href="more_about_maps.html">More About Maps</a></li>
				<li><a href="how_to_filter_your_data.html">How to Filter Your Data</a></li>
				<li><a href="final_remarks.html">Final Remarks</a></li>
				<li><a href="joa_data_files.html">Java OceanAtlas Data Files</a></li>
			</ul>
			<p><a class="cta-btn align-middle" href="joa.html">Explore</a></p>
		</div>
	</div>
</center>
