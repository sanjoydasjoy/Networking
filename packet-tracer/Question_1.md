> Configure the network shown in the diagram so that all PCs in the **172.10.5.0/24** network can communicate with the server in the **172.10.10.0/24** network through **Router R1**.
>
> Perform the following tasks:
>
> 1. Rename the router as **R1** and the switch as **SW1**.
> 2. Assign the following IP addresses:
>
>    * Router **G0/0** → `172.10.10.1 /24` (connected to the server)
>    * Router **G0/1** → `172.10.5.126 /24` (connected to the switch)
>    * Server → `172.10.10.126 /24`, Default Gateway → `172.10.10.1`
>    * PC#10 → `172.10.5.10 /24`, Default Gateway → `172.10.5.126`
>    * PC#20 → `172.10.5.20 /24`, Default Gateway → `172.10.5.126`
>    * PC#30 → `172.10.5.30 /24`, Default Gateway → `172.10.5.126`
> 3. Activate all router interfaces using the command:
>
>    ```bash
>    no shutdown
>    ```
> 4. Save the configuration.
> 5. Finally, **ping** from **PC#20** to the **Server (172.10.10.126)** to verify full connectivity.

<br>

___

<br>
