# Etherchannel-layer-2

## Objective
- Configure three Layer 2 EtherChannels between Switch7, Switch8, and Switch9.
- Bundle multiple physical links into logical Port-Channel interfaces.
- Configure the EtherChannels as trunk links to carry VLAN traffic.
- Verify EtherChannel formation and operational status.
- Observe how Spanning Tree Protocol (STP) treats each EtherChannel as a single logical link.
- Demonstrate redundancy by verifying connectivity when a member link fails.
- Validate load balancing across the EtherChannel links using verification commands.

## Configure Static EtherChannel
  - Mode on
 
## Diagram

  <div>
    <img width="758" height="308" alt="image" src="https://github.com/user-attachments/assets/44a19e7c-cfc7-4c57-ae63-1e6fa5eb6755" />
  </div>

## Create the Ether Channel group 1 on switch 19

  <div>
    <img width="742" height="253" alt="image" src="https://github.com/user-attachments/assets/9adc13f2-7684-4d5e-8ed2-76e48c1f9fee" />
  </div>

## Create the EtherChannel group 1 on switch 20

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

    ## Create Ether Channel group 1 on switch 7, we mistakenly add 3 links, then we remove it.

    <div> 
      <img width="1290" height="839" alt="image" src="https://github.com/user-attachments/assets/f619d8ec-eb63-4959-80cf-fb74bb955b2e" />
    </div>

    ## Result, we just have 2 links fa0/1, fa0/3 in the etherchannel group 1 on switch 7

    <div>
      <img width="733" height="267" alt="image" src="https://github.com/user-attachments/assets/3d0e394a-ca43-4a61-8a7c-3866b4ac8332" />
    </div>

    ## Create Ether Channel group 1 on switch 8

    <div>
      <img width="879" height="575" alt="image" src="https://github.com/user-attachments/assets/61e73b68-8a7e-422b-a08f-56fc31ac1e07" />
    </div>
    

  - PAGP
  - Desirable / Desirable
  - Desirable / Auto
