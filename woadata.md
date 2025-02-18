---
layout : datapage
title : World Ocean Atlas datapage
ocean: World Ocean Atlas
---

<section id="hero">
	<div class="hero-container">
		<h1>Explore {{page.ocean}} Data</h1>
		<h2>Navigate to your desired data below</h2>
		<center><img src="assets/images/woamap.jpg" alt="" class="responsive"></center>
	</div>
</section>
<!-- #hero -->
<section id="call-to-action1">
	<section id="call-to-action3">
		<div class="container wow fadeIn">
			<div class="col-lg-9 text-center text-lg-left" style="flex:0 0 100%;max-width:100%">
				<h3 class="cta-title1" style="text-align:center">About {{page.ocean}} Data</h3>
				<br>
				<p class="cta-text1" style="text-align:center">The NOAA World Ocean Atlas (WOA) quality-controlled mean temperature, salinity, dissolved oxygen, and nutrient data were originally released by layer by layer on standard level surfaces on a 1-degree positional grid for the World Ocean. We have WOA data from NOAA WOA releases from 1998, 2005, 2009, 2013, and 2018. We reassembled the data at each grid point into vertical profiles, with data at each WOAyy standard level for which there are reported values. We provide some of the WOAyy data as areal, gridded data at the original 1-degree grid spacing, and most at a sub-grid spacing which provides adequate basin-scale visualization with reduced computer resource requirements. Various collections of these grids and sub-grids are provided. We also provide vertical sections taken from WOAyy at 5-degree intervals of latitude and 10-degree intervals of longitude.</p>
			</div>
		</div>
	</section>
</section>
<!-- #call-to-action -->
<div id="collapseDVR3" class="panel-collapse collapse in" style="background-color: black">
		<div class="container h-100">
			<center style="color: white;font-size: 25px;font-family: 'Poppins';margin-top: 7%;"> Pick a Search Functionality</center>
			<center style="color: white; padding-top: 5%;"><a class='button-func' href="#tree-search"> Tree Search </a>
			<a class='button-func' href="#dropdown-search"> Dropdown Search </a></center>
			<hr class="style-one">
			<center style="color: white;font-size: 25px;font-family: 'Poppins';margin-top: 7%;"> Dropdown Search</center>
			<section id="dropdown-search">
			<div class="row h-100 align-items-center justify-content-center">
				<div class="col-12 col-md-10">
					<div class="hero-search-form">
						<div class="tab-content" id="nav-tabContent">
							<div class="tab-pane fade show active" id="nav-places" role="tabpanel" aria-labelledby="nav-places-tab">
								<h6>What data are you looking for?</h6>
								<div class="row">
									<form action="#" method="get" >
										<center style="margin-left: 10vw;">
											<select class="custom-select" id="verticalSectionDropdown">
												<option value="All" selected="selected">Vertical Section</option> {% for item in site.data.woadata.section_1%}
												<option value="{{item.title}}">{{item.title}}</option> {% endfor %} </select> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
											<select class="custom-select" id="yearDropdown">
												<option value="All">Year</option> {% for item in site.data.woadata.yeardropdown %}
												<option value="{{item.year}}">{{item.year}}</option> {% endfor %} </select> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
											<select class="custom-select" id="fileDropdown">
												<option value="All">File</option>
												<option value=".csv">.csv</option>
												<option value=".jos">.jos</option>
												<option value=".txt">.txt</option>
												<option value=".joa">.joa</option>
												<option value=".zip">.zip</option>
											</select>
										</center>
									</form>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
			</section>
		</div>
			<div class="container-table100">
				<div class="wrap-table100">
					<div class="table100 ver3 m-b-110">
						<div class="table100-head">
							<table>
								<thead>
									<tr class="row100 head">
										<th class="cell100 column1">Vertical Section</th>
										<th class="cell100 column2">Year</th>
										<th class="cell100 column4">File</th>
									</tr>
								</thead>
							</table>
						</div>
						<div class="table100-body js-pscroll" style="max-height:1500px">
							<table class="table" id="datatable1">
								<tbody id="datatable"> 
									{% for item in site.data.woadata.section_1%} 
										{% for entry in item.subsections%} 
											{% for file in entry.files%}
												<tr>
													<td class="cell100 column1">{{item.title}}</td>
													<td class="cell100 column2">{{entry.subsection}}</td>
													<td class="cell100 column4"><a href="{{file.path}}">{{file.name}}</a></td>
												</tr> 
											{% endfor %} 
										{% endfor %} 
									{% endfor %} 
									{% for item in site.data.woadata.section_2%} 
										{% for entry in item.subsections%} 
											{% for subentry in entry.subsubsections%}
											{% if subentry.seasons[0] %}
											{% for subsubentry in subentry.seasons%}
											{% for file in subsubentry.files%}
												<tr>
													<td class="cell100 column1">{{item.title}}</td>
													<td class="cell100 column2">{{subsubentry.season}}</td>
													<td class="cell100 column4"><a href="{{file.path}}">{{file.name}}</a></td>
												</tr> 
											{% endfor %} 
											{% endfor %} 
											{% else %}
											{% for file in subentry.files%}
												<tr>
													<td class="cell100 column1">{{item.title}}</td>
													<td class="cell100 column2">{{subentry.subsubsection}}</td>
													<td class="cell100 column4"><a href="{{file.path}}">{{file.name}}</a></td>
												</tr> 
											{% endfor %}
											{% endif %}
											{% endfor %} 
										{% endfor %} 
									{% endfor %} 
								</tbody>
							</table>
						</div>
					</div>
				</div>
			</div>
			<hr class="style-two">
			<center style="color: white;font-size: 25px;padding-bottom: 3%;font-family: 'Poppins';"> Data Tree Search</center>
			<section id="tree-search">
			<div class="tree ">
				<ul> <span style="color:white;font-size: 20px;"><b>{{page.ocean}} Data</b></span>
				<ul>
					<li><a href="#"><span style="background:#5cb85c;color:white">Download all World Ocean Atlas Data</span></a></li>
					<li><a href="assets/documents/About the WOA Data Files.pdf"><span style="color:white">About the WOA Data Files.pdf</span></a></li>
					<li> <span style="color:white"><i class="fa fa-plus-square" style="color:white"></i>Vertical Section Data</span>
						<ul> {% for item in site.data.woadata.section_1 %}
							<li> <span style="color:white"><i class="fa fa-plus-square" style="color:white"></i>{{item.title}}</span>
								<ul>
									<li><a href="{{item.zip_path}}"><span style="background:#5cb85c;color:white">Download all {{item.title}} </span></a></li> {% for entry in item.subsections%}
									<li> <span style="color:white"><i class="fa fa-plus-square" style="color:white"></i>{{entry.subsection}}</span>
										<ul> {% for file in entry.files%}
											<li><span style="color:white"><a href="{{file.path}}">{{file.name}}</a></span></li> {% endfor %}
										</ul>
									</li> {% endfor %} 
								</ul>
							</li> {% endfor %} {% for item in site.data.woadata.section_2 %}
							<li> <span style="color:white"><i class="fa fa-plus-square" style="color:white"></i>{{item.title}}</span>
								<ul>
									<li><a href="{{item.zip_path}}"><span style="background:#5cb85c;color:white">Download all {{item.title}} </span></a></li>
									<li><a href="assets/documents/Guide to the WOA18 Data Files v2.pdf"><span style="color:white">Guide to the WOA18 Data Files v2.pdf</span></a></li>
									<li><a href="assets/documents/Important warning about WOA18 oxygen units.pdf"><span style="color:white">Important warning about WOA18 oxygen units.pdf</span></a></li>
									{% for entry in item.subsections%}
									<li> <span style="color:white"><i class="fa fa-plus-square" style="color:white"></i>{{entry.subsection}}</span>
										<ul> {% for subentry in entry.subsubsections%}
											<li> <span style="color:white"><i class="fa fa-plus-square" style="color:white"></i>{{subentry.subsubsection}}</span> {% if subentry.seasons[0] %}
												<ul> {% for subsubentry in subentry.seasons%}
													<li> <span style="color:white"><i class="fa fa-plus-square" style="color:white"></i>{{subsubentry.season}}</span>
														<ul> {% for file in subsubentry.files%}
															<li><span style="color:white"><a href="{{file.path}}">{{file.name}}</a></span></li>{% endfor %} 
														</ul>
													</li> {% endfor %} 
												</ul> 
											{% else %}
												<ul> {% for file in subentry.files%}
													<li><span style="color:white"><a href="{{file.path}}">{{file.name}}</a></span></li> {% endfor %} 
												</ul> 
											{% endif %} 
											</li> {% endfor %}
										</ul>
									</li> {% endfor %} 
								</ul>
							</li> {% endfor %} 
						</ul>
					</li>
				</ul>
			</ul>
			</div>
			</section>
</div>
