## Task 1: Configure the production site (GROUP\#-AVS1-SDDC)

In this task you will create a network segment in the production site and deploy
a test VM to be protected with Site Recovery Manager.

*This task requires a DHCP profile to be available in the private cloud. DHCP
profiles have been configured in Module 1 for both GROUP\#-AVS1-SDDC and
GROUP\#-AVS2-SDDC. If you did not complete the corresponding steps in Module 1,
please go back to it and configure DHCP profiles before proceeding.*

Log into NSX-T client for the protected/primary site GROUP\#-AVS1-SDDC. Click on
the **Segments** item in the left-hand menu and then click the **ADD SEGMENT**
button in the main tile. Enter the following configuration settings:

-   Segment Name: **SRM-LAB**

-   Connected gateway: Select the private cloud’s default Tier1 gateway

-   Transport Zone: Select the private cloud’s default **overlay** transport
    zone

-   Gateway CIDR IPv4: **10.\#.60.1/24**

![](media/367712fc63544d3aac43e67cd75c5220.png)

Click on the **SET DHCP CONFIG** button and provide the following settings:

-   DHCP Type: **Gateway DHCP Server**

-   DHCP Profile: Select the profile created in Module 1

-   DHCP Config: Set the toggle to **Enabled**

-   DHCP Ranges: **10.\#.60.100-10.\#.60.120**

![](media/3fc2f1868be7edaa9625e29e5b5efe32.png)

When done, click on the **APPLY** button to close the DHCP Configuration window.
Then scroll down and click on the **SAVE** button to commit the segment
configuration.

![Graphical user interface, text, application, email, website Description
automatically generated](media/27e39ac4a19c0d7b2200f30f7b9f0605.png)

Click **NO** to close the configuration window. Confirm the segment is
successfully configured by checking that it appears in the segments list.

![A computer screen capture Description automatically generated with medium
confidence](media/cee6bdc13e1efc967011ebbe78b0a1f8.png)

Optionally, you can confirm that the newly created segment is also visible in
the Azure portal. It may take up to 2-3 mins to show up in the portal.

Navigate to GROUP\#-AVS1-SDDC AVS Private Cloud and select the **Segments** item
in the Workload Networking menu on the left-hand side.

![](media/c44d19dd3dac0b8ba66c71197309b9a6.png)

## Next Steps

[Module 3, Task 2](module-3-task-2.md)

[Module 3 Index](module-3-index.md)

[Main Index](index.md)