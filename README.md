# ocp-cns-gluster-health
Checking CNS Gluster health within an Openshift Cluster, with Ansible.

Several Ansible plays that check the status of healing and balancing in gluster volumes,
used by container-native-storage deployed within an OpenShift cluster. 
Once certain checks are done, and conditions align, gluster nodes can be rebooted without damaging
the integrity of the gluster pool.

For reference:

`gluster volume heal <volume name/id> info` shows healing goings on

`gluster volume heal <volume name/id> info split-brain` checking for split brain 

`gluster volume rebalance <vol name> status` in case rebalancing is happening

`gluster volume info` is the overarching status of the volume

`gluster volume heal <vol name> info failed` checks for healed status

`gluster volume heal <vol name> info summary (--xml)` summary command, that optionally outputs as xml
