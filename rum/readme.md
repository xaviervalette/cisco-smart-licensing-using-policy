# Example of a RUM report from STE-7ALD-WLC-1 (C9800-CL)

```
STE-7ALD-WLC-1# sh license rum id all
Smart Licensing Usage Report:
====================================
Report Id,          State,    Flag, Feature Name
1671840750          ACK       N     air-network-advantage
1671840751          ACK       N     air-dna-advantage
1671840752          ACK       N     air-network-advantage
1671840753          ACK       N     air-dna-advantage
1671840754          CLOSED    N     air-network-advantage
1671840755          CLOSED    N     air-dna-advantage
1671840756          OPEN      N     air-network-advantage
1671840757          OPEN      N     air-dna-advantage
```

## How to get RUM ?
### From the device via CLI
```
STE-7ALD-WLC-1# conf t                   
Enter configuration commands, one per line.  End with CNTL/Z.
STE-7ALD-WLC-1(config)# service internal 
STE-7ALD-WLC-1(config)# exit
STE-7ALD-WLC-1# test license smart rum show 1671840757
{"version":"2.0","asset_identification":{"report_id":1671840757,"asset":{"name":"regid.2018-05.com.cisco.WLC_9500C,1.0_85665885-b865-4e32-8184-5510412fcb54"},"instance":{"sudi":{"udi_pid":"C9800-CL-K9","udi_serial_number":"9NTUEA8FIIH"}}},"signature":{"signing_type":"builtin","key":"regid.2018-05.com.cisco.WLC_9500C,1.0_85665885-b865-4e32-8184-5510412fcb54","value":"mrAJAUGq94+dZqnUJ684iGm82E1fCbJVjLN5CoxrM/Q="},"meta":{"entitlement_tag":"regid.2017-08.com.cisco.AIR-DNA-A,1.0_b6308627-3ab0-4a11-a3d9-586911a0d790","utility_enabled":false,"software_version":"17.09.02","ha_udi":[{"role":"Active","sudi":{"udi_pid":"C9800-CL-K9","udi_serial_number":"9NTUEA8FIIH"}}]},"measurements":[{"log_time":1680767427,"metric_name":"ENTITLEMENT","start_time":1680767118,"end_time":1680807618,"sample_interval":40500,"num_samples":46,"meta":{"added_sudi_list":[{"udi_pid":"AIR-AP2802I-E-K9","udi_serial_number":"FDW2109B29P"},{"udi_pid":"AIR-AP2802I-E-K9","udi_serial_number":"FDW2109B2BX"},{"udi_pid":"AIR-AP2802I-E-K9","udi_serial_number":"FDW2028D3SV"}],"removed_sudi_list":[]},"value":{"type":"COUNT","value":"3"}}]}
```