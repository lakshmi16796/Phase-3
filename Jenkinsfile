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
			
			n=$(grep -rin "###" local.conf | awk '{print $2 }')
			echo "recognised pattern is"
			echo $n
			
			#echo "$n" >> properties
			sed -i "=\$n" properties
			
			#sed -n "/"###"/p" local.conf | awk '{print $2 }' properties <<< "="
        		#echo "$line"
			'''
		  }
		} 
  }
  }
  }
  
  }

