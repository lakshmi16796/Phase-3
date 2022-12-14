pipeline {
  agent any
  stages 
{  
    stage ("User Input Stage")
    {
	    
      steps {	 
	      
	script {
		
                 
	    
		dir("/home/lakshmi/test/local")  
		  {
      	        	sh '''#!/bin/bash
			input=$(printenv choices)
			echo "your input"
			echo "$input"
			
			n=$(grep -rin "###" local.conf | awk '{print $2 }')
			echo "recognised pattern is"
			#echo $n
			x=$(echo $n | sed 's/ /,/g')
			#echo "x is"
			echo $x
			
			echo "feature=$x" >> properties
					
			'''
		  }
		
		 echo "selected parameter is"		      
	         echo "${env.choices}"	
		} 
  }
  }
  }
  
  }

