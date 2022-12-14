pipeline {
  agent any
  stages 
{  
    stage ("User Input Stage")
    {
	    
      steps {	 
	      
	script {
		
            echo "selected parameter is"		      
	    echo "${env.choices}"	      
	    
		dir("/home/lakshmi/test/local")  
		  {
      	        	sh '''#!/bin/bash
			input=$(printenv choices)
			echo "your input"
			echo "$input"
			
			n=$(grep -rin "###" local.conf | head -1 | awk '{print $1 }' | cut -d[A-Z] -f 2)
			echo "recognised pattern is"
			echo $n
			'''
		  }
		} 
  }
  }
  }
  
  }

