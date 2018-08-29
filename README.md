# UiPath-Bot-Manager-Framework

Robotic workload distribution framework enables to distribute transaction items across available robots in a round robin manner. 

On a high level, there are 3 logical components to this framework; a) Master Robot b) Master Queue c) Master Config. The Master Robot runs non-stop as backend robot checking for requests in Master Queue. The Master Config is a configuration spreadsheet contain the settings necessary for the framework like process to robot mapping, orchestrator details, assets and other technical parameters. 

A new transaction for a process is triggered by creating a transaction item in the master queue. The transaction item will contain all the inputs for the master bot and well as the inputs required by the process which we intended to trigger.

Features<br>
&nbsp;&nbsp;•	Build on top of RE Framework<br>
&nbsp;&nbsp;•	Auto dispatch transactions across multiple robots based on bot availability<br>
&nbsp;&nbsp;•	Cross Orchestrator and/or cross Tenant work distribution is supported <br>
&nbsp;&nbsp;•	Process specific Robot assignment allows fine workload control<br>
&nbsp;&nbsp;•	Able to manage workload of multiple different processes<br>
 
