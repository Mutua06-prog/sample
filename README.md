# sample

## sdf
cuscmvo
## df
- a
- b
- c
- **f**
  ```
proc template;   
	define statgraph mean_se; 
    	begingraph;  
			entrytitle textattrs=(size=12pt weight=normal) halign = center 'Coagulation (mean +/- SE) values by visit';
			layout overlay/xaxisopts=(offsetmin=0.05 offsetmax=0.05 linearopts=(tickvaluelist= (0 4 8 12)) label= 'Time (weeks)')
							yaxisopts=(griddisplay=on gridattrs=(thickness= 0.1 color=lightgrey) linearopts=(tickvaluepriority=true TICKVALUESEQUENCE=(START=12 END=16 INCREMENT=1)) offsetmin=0.15 offsetmax=0.1 label='Mean (SE+/-)');          
				seriesplot x= avisitn2 y= mean /group =treatn name= 'trt' ;
				scatterplot x=avisitn2 y=mean/ group=treatn yerrorlower= minus_se yerrorupper=plus_se markerattrs=(symbol= graphdata4)
							datalabel= mean datalabelattrs=(color=brown);
				drawtext textattrs=(size=9pt) "Number of Subjects" /anchor=bottomleft width=22 widthunit=percent 
									xspace=wallpercent yspace=wallpercent x=1 y=11 justify=center ;
			   innermargin/align=bottom pad=0.8;
				axistable x=avisitn value=nsubj / class=treatn   ;
			   endinnermargin;
				discretelegend 'trt' / title= " " titleattrs= (size=9pt weight=normal ) location= inside  halign=left valign=top 
					valueattrs= (size=9pt)  border=false;
			endlayout;
     	endgraph; 
   end;
run; 
  ```
