<template>
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.4.0/css/font-awesome.min.css">  
<div class="wrapper">
<section class="header">

  <div class="logo-and-nav-wrap">
			
      <div class="logo-wrap">
				<a href="#/global">LOGO</a>
			</div>
      
			<div class="site-nav-wrap">
         <nav class="nav">
					
				
						<div class="breadcrumb-wrap">
							<span class="sep"><i class="fa fa-caret-right"></i></span> <span class="breadcrumb"><a href="#">Universe</a></span>
						</div>
						<div class="breadcrumb-wrap">
							<span class="sep"><i class="fa fa-caret-right"></i></span> <span class="breadcrumb"><a href="#">Milky Way</a></span>
						</div>
						<div class="breadcrumb-wrap">
							<span class="sep"><i class="fa fa-caret-right"></i></span> <span class="breadcrumb"><a href="#">Solar System</a></span>
						</div>
						<div class="breadcrumb-wrap">
							<span class="sep"><i class="fa fa-caret-right"></i></span> <span class="breadcrumb"><a href="#">Earth</a></span>
						</div>						
           <div class="breadcrumb-wrap">
							<span class="sep"><i class="fa fa-caret-right"></i></span> <span class="breadcrumb"><a href="#">Internet</a></span>
						</div>
				</nav>
			</div>
		</div>
	</section>

  <section class="body">
    <div class="content">
      <p>Play with the browser size to see how the breadcrumbs behave.</p>
      <ul>
        <li>Breadcrumbs shrinks when not enough space</li>
        <li>Mouse hover cancels ellipsis to let user read the full text</li>
      </ul>
    </div>
    </section>
  </div>
  </template>
  <script>
      export default{
          name:'Breadcrumbs',
          data(){
              return
          }
      }
  </script>
  