# sdran-onos-a1t---policy-concurency-issue

Proof of Concept of a  DoS by  replaying mulitple concurent policies to the Sdran-in-a-box Onos a1t component
The ONOS A1 Termination component of  SD RAN ORAN deployment  was susceptible to a Denial of Service attack through the continuous replay of concurrent HTTP policies. This attack resulted in the termination of the service, impacting the management of A1 policies.

Attack Reproduction :  We tested the SDRAN-in-a-Box (RiaB) v1.4.3, specifically the RAN Simulator and Rimedo Traffic Steering xApp edition ( https://docs.sd-ran.org/master/sdran-in-a-box/docs/Installation_RANSim_RIMDEO_TS.html ). The attack consists of replaying the JSON-based Traffic Steering Policies (ORAN_TrafficSteeringPreference_2.0.0) by scripting a multithreaded curl command. Please download and setup the deployment as instructed on their release page, once completed. proceed to identify the Ip and port of the a1t by running make test-rnib. Replace that ip and port in the provided a1dos.py script provided in this repository. You can modify the intensity of the attack by manipluating the number of threads,  Wait and observe as the a1t crashes.   You can run Kubectl get pods -n riab to confirm this. 

the following video shows the POC running on a vagrant vm running ubuntu 20.04

