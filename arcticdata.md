---
layout : datapage
title : Arctic Datapage
ocean: Arctic
---

<section id="hero">
	<div class="hero-container">
		<h1>Explore {{page.ocean}} Ocean Data</h1>
		<h2>Navigate to your desired data below</h2>
		<center><img src="assets/images/cleandatamap.jpg" alt="" class="responsive"></center>
	</div>
</section>
<!-- #hero -->
<section id="call-to-action1">
	<section id="call-to-action3">
		<div class="container wow fadeIn">
			<div class="col-lg-9 text-center text-lg-left" style="flex:0 0 100%;max-width:100%">
				<h3 class="cta-title1" style="text-align:center">About {{page.ocean}} Ocean Data</h3>
				<br>
				<p class="cta-text1" style="text-align:center">Vertical section data from Arctic Ocean and Nordic Seas expeditions from J. Swift's files. The data values for measured parameters are unchanged (with one exception), but the files have been vetted and groomed for improved readability and consistency, and assembled in sensible geographic order.</p>
			</div>
		</div>
	</section>
</section>
<!-- #call-to-action -->
<div style="background-color: black">
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
									<form action="#" method="get">
										<center style="margin-left: 10vw;">
											<select class="custom-select" id="verticalSectionDropdown">
												<option value="All" selected="selected">Vertical Section</option> {% for item in site.data.arcticdata.section%}
												<option value="{{item.title}}">{{item.title}}</option> {% endfor %} </select> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
											<select class="custom-select" id="yearDropdown">
												<option value="All">Year</option> {% for item in site.data.arcticdata.yeardropdown %}
												<option value="{{item.year}}">{{item.year}}</option> {% endfor %} </select> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
											<select class="custom-select" id="fileDropdown">
												<option value="All">File</option>
												<option value="Basin">.csv</option>
												<option value="Sub Basin">.jos</option>
												<option value="Option_3">.txt</option>
												<option value="Option_4">.joa</option>
												<option value="Option_5">.zip</option>
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
								<tbody id="datatable"> {% for item in site.data.arcticdata.section%} {% for entry in item.years%}
									<tr>
										<td class="cell100 column1">{{item.title}}</td>
										<td class="cell100 column2">{{entry.year}}</td>
										<td class="cell100 column4">{{entry.file}}</td>
									</tr> {% endfor %} {% endfor %} </tbody>
							</table>
						</div>
					</div>
				</div>
			</div>
	<hr class="style-two">
	<center style="color: white;font-size: 25px;padding-bottom: 3%;font-family: 'Poppins';"> Data Tree Search</center>
	<section id="tree-search">
	<div class="tree ">
					<ul> <span style="color:white;font-size: 20px;"><b>{{page.ocean}} Ocean</b></span>
				<ul>
					<li> <span style="background:#5cb85c;color:white">Download all {{page.ocean}} Data</span></li> {% for item in site.data.arcticdata.section %}
					<li> <span style="color:white"><i class="fa fa-plus-square" style="color:white"></i>{{item.title}}</span>
						<ul>
							<li> <span style="background:#5cb85c;color:white">Download all {{item.title}} Data</span></li> {% for entry in item.years%}
							<li> <span style="color:white"><i class="fa fa-plus-square" style="color:white"></i>{{entry.year}}</span>
								<ul>
									<li> <span style="color:white">File</span> </li>
									<li> <span style="color:white">File</span> </li>
									<li> <span style="color:white">File</span> </li>
									<li> <span style="color:white">File</span> </li>
								</ul>
							</li> {% endfor %} </ul>
					</li> {% endfor %} </ul>
			</ul>
	</div>
	</section>
</div>
