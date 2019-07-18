# calm-bp-elastic

  - Download Nutanix Calm blueprint (.json) in order to run blueprint in Nutanix Prism Central hosted Calm service.
  - On upload to Calm service all previous blueprint credentials are invalidated
  - Create new private/public key pair
  - Populate blueprint credentials (with private key) and application profile variables (with public key string)
   
Github has an excellent guide on generating SSH keys: https://help.github.com/articles/generating-ssh-keys

* The macros below are resolved in the RUNNING application - see overview section of the application instance in Calm service.

>Blueprint VM/App access info :
>
>Complete Multi-VM (Workload Driver/Generator - Data Visualisation - Search/Index) stack
>
>Access:
>* esrally VM : ssh -i ./keys.pem -l centos @@{Workload_Driver.address}@@
>
>* Elasticsearch VM Access : ssh -i ./keys.pem -l centos @@{Search_Index.address}@@
>
>* Kibana VM Access : ssh -i ./keys.pem -l centos @@{Data_Visualisation.address}@@
>
>* Kibana GUI : @@{Data_Visualisation.address}@@:@@{Data_Visualisation.kibana_port}@@
