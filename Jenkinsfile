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
	    
		dir("/home/lakshmi/dell_pods/poky/build/conf")  
		  {
      	        	sh '''#!/bin/bash
			input=$(printenv choices)
			echo "your input"
			echo "$input"
			
			n=$(grep -rin '###' local.conf | head -1 )
			echo "recognised pattern is"
			echo $n
			'''
		  }
		} 
  }
  }
  }
  
  }

