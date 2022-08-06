
Changes in site.vm


#macro ( links $links )

changed:

 #link( $currentItemHref $item.name )
 
into:

    #if ( $project.name == $item.name )
      <span class="selected">$item.name</span>
 	#else
      #link( $currentItemHref $item.name )
 	#end
 	
CSS added in maven-theme.css

#breadcrumbs .xleft .selected {
	font-weight: bold;
	color: #2D302C;
	border: 0px;
	background-color: #FFF;
	font-size: 12px;
	padding: 3px;
}