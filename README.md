# UiPath-Bot-Manager-Framework

UiPath Bot Manager Framework aims to function as a workload manager for robots by distributing transactions across available robots. 

On a high level, there are 3 logical components to this framework; a) Master Robot b) Master Queue c) Master Config. The Master Robot runs non-stop as a backend job checking for requests in Master Queue. The Master Config spreadsheet maintains the framework configuration data such as process to robot mapping, orchestrator details, assets and other configuration parameters. 

A new transaction for a process is triggered by creating a transaction item in the master queue. The transaction item will contain all the inputs for the master bot and well as the inputs required by the intended process. The master bot reads each trasnsactions from the master queue and assigs to a robot based on the availability. The master bot ensures the optimum utilization of robots by keeping more robots occupied as more requests arrives.


Features<br>
&nbsp;&nbsp;•	Build on top of RE Framework<br>
&nbsp;&nbsp;•	Auto dispatch transactions across multiple robots based on bot availability<br>
&nbsp;&nbsp;•	Work distribution is supported across Orchestrator and/or Tenant <br>
&nbsp;&nbsp;•	Robot assignment can be setup at process level which provides flexible control on workload management<br>
&nbsp;&nbsp;•	Able to manage workload of multiple different processes<br>
 
