# UiPath-Hub-and-Spoke-Framework

UiPath Hub and Spoke Framework aims for efficient utilization of robots by distributing workload across idle robots(Spoke bots) using a master robot(Hub bot).

On a high level, there are 4 logical components to this framework; <br>a) Hub/Master Robot <br>b) Master Queue <br>c) Master Config<br>d) Spoke/Child Robots <br><br>The Hub robot runs non-stop as a background job checking for requests in Master Queue. The Master Config spreadsheet maintains the framework configuration data such as process to robot mapping, orchestrator details, assets and other configuration parameters. 

A new transaction for a process is triggered by creating a transaction item in the master queue. The transaction item will contain all the inputs for the master bot and well as the inputs required by the intended process. The master bot reads each trasnsactions from the master queue and assigs to a robot based on the availability. The master bot ensures the optimum utilization of robots by keeping robots occupied as more requests arrives.

Features<br>
&nbsp;&nbsp;•	Auto dispatch transactions across multiple robots based on bot availability<br>
&nbsp;&nbsp;•	Work distribution is supported even across Orchestrator and/or Tenant <br>
&nbsp;&nbsp;•	Robot assignment can be setup at process level which provides maximum flexibility and control in workload management<br>
&nbsp;&nbsp;•	Able to manage workload of multiple processes<br>
&nbsp;&nbsp;•	A robot is wake up only when there is a transaction to process<br>
 
