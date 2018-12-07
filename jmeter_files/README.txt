 # (C) Copyright IBM Corporation 2015.
 #
 # Licensed under the Apache License, Version 2.0 (the "License");
 # you may not use this file except in compliance with the License.
 # You may obtain a copy of the License at
 #
 # http://www.apache.org/licenses/LICENSE-2.0
 #
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 

daytrader3.jmx is an Apache JMeter script that may be used for running the DayTrader3 benchmark.

Jmeter version 3.3 or later is highly recommended.

The script has the following options:
	-JHOST	    The name of the machine running the DayTrader Application. The default is localhost.
	-JPORT	    The HTTP port of the server running the DayTrader Application. The default is 9083.
	-JTHREADS   The number of jmeter threads to start. The default is 50.
	-JDURATION  The time (in seconds) to run jmeter.
	-JSTOCKS    The total amount of stocks/quotes in the database, minus one. The default is 9999, which assumes there are 10,000 stocks in the database.
	-JBOTUID    The lowest user id. The default is 0.
	-JTOPUID    The highest user id. The default is 14999, which assumes there are 15,000 users in the database.
	
Example: ./jmeter -n -t daytrader3.jmx -JHOST=myserver -JPORT=9083 -JDURATION=300