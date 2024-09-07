# sample

## sdf
cuscmvo
## df
- a
- b
- c
- **f**
  
  ```r
    proc template;   
	  define statgraph mean_se; 
    	begingraph;  
			entrytitle textattrs=(size=12pt weight=normal) halign = center 'Coagulation (mean +/- SE) values by visit';
			layout overlay/xaxisopts=(offsetmin=0.05 offsetmax=0.05 linearopts=(tickvaluelist= (0 4 8 12)) label= 'Time (weeks)')
							yaxisopts=(griddisplay=on gridattrs=(thickness= 0.1 color=lightgrey) linearopts=(tickvaluepriority=true TICKVALUESEQUENCE=(START=12 END=16 INCREMENT=1))
  ```
