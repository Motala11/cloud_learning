# Autoscaling


![alt text](images/HA_HS_Diagram.png)
In the example above, if the CPU load exceeds 75% (defined in the custom autoscale)then the scale set will launch a new instance. <br>
By default, there is a minimum of 2 VMs which means if one does go down, the other one will remain running.
- [Autoscaling](#autoscaling)
    - [High availability](#high-availability)
    - [High scalability](#high-scalability)
    - [Load balancers](#load-balancers)

Virtual Machine scale sets are used to improve both availability and scalability. <br> <br>

### High availability
They improve availability by having different VM's in different availability zones, thus ensuring there is still production incase of a failure. <br>

### High scalability
A scale set also improves scalability, as there are now a minimum of 2 VM's operating, as opposed to just one. An increase in VMs allows for horizontal scaling, which is when you increase the number of servers. <br>

### Load balancers
Load balancers can be used in conjunction with the virtual machine scale set. They are separate entities, but can be used together. <br> <br>
Using a load balancer will increase scalability, as the load balancer ensures that there is even distribution amongst the virtual machines, hence the load is balanced.



### Prerequisites of making a Scale set
Before you make a Scale set, you must have the following:
1. A custom Image to create the Scale set, alongside the user data needed for this.
2. Ensure your custom Image works and creates a VM functioning as intended.
3. Ensure your user data provides the results required.
### How to make a Scale set
To make a Scale set, you need to:
1. Click create new Scale set.
   ![alt text](images/create-vmss.png)
2. Name it appropriately.
3. Choose whether you want the orchestration mode to be flexible or uniform.
   ![alt text](images/orchestration.png)
4. Choose what type of scaling you desire, outline the custom scaling parameters.
5. Choose the instance count.
   ![alt text](images/scaling-condition.png)
6. Choose your custom Image.
7. Fill out security details as appropriate.
8. Choose the correct Network details.
9.  Create a load balancer, to use the ports you need.
    ![alt text](images/lb.png)
10.  Select "Enable health monitoring" and "Enable automatic repairs".
11. Input your user data in the Advanced section.
12. Review all your details are correct, and create.
 
### How to test the Scale set works
To test the scale set works, you can check the public IP address. If it works as intended, it should redirect you to your homepage.
### How to manage instances
Reimaging is when you restore a server back to its original state. Upgrading involves updating the existing software to a newer version, whilst retaining user data and configurations.
### Steps on how to create an unhealthy instance (for testing) and WHY it is considered healthy/unhealthy
To create unhealthy instances, you need to implement failure conditions, such as:
- Resource overload
- Network issues
- Service outages
- Application-level failures

Creating an intentionally unhealthy instance for testing purposes helps evaluate the resilience and fault tolerance of your system.<br> You can identify weaknesses, optimize recovery strategies, and ensure that your system behaves predictably under adverse conditions.<br> The reasons an instance is marked as healthy or unhealthy often depend on predefined criteria, thresholds, and the specific health checks implemented in your system's monitoring and management processes.
### How to SSH into an instance in your Scale set
To SSH into your instance, you must do the following:
1. Copy and paste the provided code by Azure, when you click on the "Connect" tab.
2. You need to change the private IP address that Azure provide, to the public IP address of the load balancer.
3. Include the code `-p <port number>` before you specify the IP address. This will specify what port you are going to use, so you can access the instance in particular.
### How to delete a Scale set and all of the connecting parts
To delete a Scale set, you need to delete 3 items:
1. The Scale set itself.
2. The load balancer
3. The public IP used by the Scale set.
It has to be in this order, as the public IP is not deletable whilst it is in use by the load balancer.