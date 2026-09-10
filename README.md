# Etherchannel-layer-2

## Objective
- Configure Layer 2 EtherChannels between switches using static EtherChannel (ON), LACP, and PAgP.
- Bundle multiple physical links into logical Port-Channel interfaces to increase bandwidth and provide redundancy.
- Configure the EtherChannels as 802.1Q trunk links to carry VLAN traffic between switches.
- Verify successful EtherChannel formation and operation for static and dynamic negotiation modes.
- Compare the behavior of static EtherChannel, LACP, and PAgP configurations.
- Verify Port-Channel status and member interfaces using Cisco verification commands.
- Observe how Spanning Tree Protocol (STP) treats each EtherChannel as a single logical link.
- Demonstrate link redundancy by disconnecting a member interface and verifying that network connectivity is maintained.
- Validate traffic distribution and load balancing across the bundled EtherChannel links.

## Configure Static EtherChannel
  - Mode on
 
## Diagram

  <div>
    <img width="758" height="308" alt="image" src="https://github.com/user-attachments/assets/44a19e7c-cfc7-4c57-ae63-1e6fa5eb6755" />
  </div>

## Create Ether Channel group 1 on switch 19

  <div>
    <img width="742" height="253" alt="image" src="https://github.com/user-attachments/assets/9adc13f2-7684-4d5e-8ed2-76e48c1f9fee" />
  </div>

## Create EtherChannel group 1 on switch 20

<div>
  <img width="773" height="249" alt="image" src="https://github.com/user-attachments/assets/bce872bc-7ee8-4426-a850-0cc2942c1d9d" />
</div>

## Show EtherChannel summary Result

<div>
  <img width="713" height="266" alt="image" src="https://github.com/user-attachments/assets/b71cb65c-f82b-4c43-9c62-1807070033ad" />
</div>

## Create a trunk link via a Portchannel on switch 19

  <div>
    <img width="605" height="83" alt="image" src="https://github.com/user-attachments/assets/32f7437f-1078-4723-81ed-a8395a10c93a" />
  </div>

## Create a trunk link via a Portchannel on switch 20

  <div>
    <img width="873" height="342" alt="image" src="https://github.com/user-attachments/assets/ecd78ade-6f36-40fb-be15-3457451f3d2d" />
  </div>

## Show interface port-channel 1 Result

<div>
  <img width="770" height="419" alt="image" src="https://github.com/user-attachments/assets/8469a490-2e72-4076-97af-bd8b8ca0814b" />
</div>

## Result

<div>
  <img width="1096" height="588" alt="image" src="https://github.com/user-attachments/assets/bd988f59-0216-4246-8e37-e1555ef719cb" />
</div>

  ## Configure dynamic EtherChannel

## Lab topology

  <div>
    <img width="1178" height="632" alt="image" src="https://github.com/user-attachments/assets/98d3d139-a770-413a-b037-901d051ef234" />
  </div>

  - LACP
  - Active / Active or   - Active / Passive

    ## Create LACP EtherChannel group 1 on switch 7, we add 3 links, then we'll remove it fa0/2.

    <div> 
      <img width="1290" height="839" alt="image" src="https://github.com/user-attachments/assets/f619d8ec-eb63-4959-80cf-fb74bb955b2e" />
    </div>

    ## Result, we just have 2 links fa0/1, fa0/3 in the etherchannel group 1 on switch 7

    <div>
      <img width="733" height="267" alt="image" src="https://github.com/user-attachments/assets/3d0e394a-ca43-4a61-8a7c-3866b4ac8332" />
    </div>

    ## Create LACP EtherChannel group 1 on switch 8

    <div>
      <img width="879" height="575" alt="image" src="https://github.com/user-attachments/assets/61e73b68-8a7e-422b-a08f-56fc31ac1e07" />
    </div>
    

  - PAGP
  - Desirable / Desirable
  - Desirable / Auto

## Create PACP EtherChannel group 2 on switch 7

<div>
  <img width="562" height="224" alt="image" src="https://github.com/user-attachments/assets/cc3407af-328f-4f39-9ea6-408837647898" />
</div>

## Create PACP EtherChannel group 2 on switch 9

<div>
  <img width="660" height="334" alt="image" src="https://github.com/user-attachments/assets/4a716b57-8aa3-45da-a38d-a670ed818f36" />
</div>

## Create static EtherChannel group 3 on switch 8

<div>
  <img width="518" height="262" alt="image" src="https://github.com/user-attachments/assets/de8497c7-5769-451e-b7c6-203a8fb587f3" />
</div>

## trunk the port-channel 3 on sw 8

<div>
  <img width="454" height="98" alt="image" src="https://github.com/user-attachments/assets/febc5c45-de21-429d-92b6-430649ce3eb5" />
</div>

## Create static EtherChannel group 3 on switch 9

<div>
  <img width="592" height="380" alt="image" src="https://github.com/user-attachments/assets/ee01fb4c-e21a-4698-84b8-2e990fc3e5ef" />
</div>

## trunk the port-channel 3 on sw 9

<div>
  <img width="523" height="305" alt="image" src="https://github.com/user-attachments/assets/90c0a2ff-06f1-4bcf-8396-59dcf8cdefd0" />
</div>

## Result on Switch 7

## port-channel 1

<div>
  <img width="590" height="344" alt="image" src="https://github.com/user-attachments/assets/0e217600-2d3e-4f98-8bdc-00b6cf8e3d63" />
</div>

## port-channel 2

<div>
  <img width="573" height="269" alt="image" src="https://github.com/user-attachments/assets/c0b0ad18-53ff-4d7a-8e0e-a12ba54aa273" />
</div>

## Result on Switch 8

## port-channel 1
<div>
  <img width="554" height="317" alt="image" src="https://github.com/user-attachments/assets/f572bbdb-a1be-4441-805d-c89f7da4074b" />
</div>

## port-channel 3

<div>
  <img width="602" height="272" alt="image" src="https://github.com/user-attachments/assets/8e7ed3fb-5165-45ca-9f09-a73e6b2f416e" />
</div>

## Result on Switch 9

## port-channel 2

<div>
  <img width="715" height="304" alt="image" src="https://github.com/user-attachments/assets/075266ab-d620-4ca8-836b-6767a7cbeb0d" />
</div>

## port-channel 3

<div>
  <img width="667" height="276" alt="image" src="https://github.com/user-attachments/assets/72db9e3f-10ef-4ecc-bc9a-d31f9787b29f" />
</div>

## Demonstrate redundancy on the LINKS.

## Verify EtherChannel Status Before Failure

<div>
  <img width="439" height="188" alt="image" src="https://github.com/user-attachments/assets/c8b6a9ef-1adb-41eb-b110-e0363d953def" />
</div>

## Simulate a Link Failure, we shutdown fa0/1 on switch 7

<div>
  <img width="476" height="128" alt="image" src="https://github.com/user-attachments/assets/8bf034b7-739b-42b0-b676-a053917e16c9" />
</div>

## Verify EtherChannel Status After Failure

<div>
  <img width="463" height="181" alt="image" src="https://github.com/user-attachments/assets/ceeb2a65-bf48-467b-bbf3-5fbe4cbc591e" />
</div>

## Conclusion

- Po1 remains up (SU)
- The remaining interfaces stay bundled (P)
- STP does not block the Port-Channel
