# Chapter 2 

## Use of Platforms in Cloud Computing

### Concepts of Abstraction and Virtualization
- **Abstraction**: In cloud computing, abstraction refers to hiding the complexities of the underlying infrastructure from users, allowing them to interact with simplified models. This enables users to focus on application development without worrying about hardware configurations and other lower-level operations.

- **Virtualization**: Virtualization is a technology that allows multiple virtual instances of hardware and software to run on a single physical machine. It optimizes resource usage and improves flexibility, enabling the efficient allocation of resources in cloud environments.

#### Virtualisation

It is the set of activities aimed at creating a virtual version of real components, including computer hardware platforms, operating systems, storage, and networking.

- Virtualization is NOT the same as emulation & simulation.
- Virtualization is the simulation of the software and/or hardware upon which other software runs.
- This simulated environment is called a virtual machine (VM).

#### Challenges:
- OS and Apps in a VM don’t know that the VMM exists or that they share CPU resources with other VMs.
- VMM should isolate Guest SW stacks from one another.
- VMM should run protected from all Guest software.
- VMM should present a virtual platform interface to Guest SW.

#### Levels of virtualization
- Application Virtualization provides a virtual implementation of the application programming interface (API) that a running application expects to use, allowing applications developed for one platform to run on another without modifying the application itself.
- Operating System virtualization provides a virtual implementation of the OS interface that can be used to run applications written for the same OS as the host, with each application in a separate VM container.

#### Full Virtualization
- One or more OSs and the applications they contain are run on top of virtual hardware.
- Each OS and application instance runs in a separate VM called a guest operating system.
- Guest OSs on a host are managed by the hypervisor/virtual machine monitor (VMM).
- Hypervisor controls the flow of instructions between the guest OSs and the physical hardware.
- Some hypervisors run on top of another OS or the host operating system.

#### Paravirtualization
- It is a method for the hypervisor to offer interfaces to the guest OS that the guest OS can use instead of the normal hardware interfaces.
- Paravirtualization is a type of virtualization where software instructions from the guest operating system running inside a virtual machine can use "hypercalls" that communicate directly with the hypervisor.
- Using paravirtualized interfaces, a guest OS can provide faster access for resources such as hard drives and networks.

#### Hardware-assisted Virtualization
- The guest OS runs at ring 0.
- Provides address bus isolation.
- The VMM uses processor extensions (such as Intel®-VT or AMD-V) to intercept and emulate privileged operations in the guest.
- Hardware-assisted virtualization removes many of the problems that make writing a VMM challenging.
- The VMM runs in a more privileged ring than 0, a virtual -1 ring is created.
- **Pros**: It allows running unmodified OSs (so legacy OS can be run without problems).
- **Cons**: Speed and Flexibility - An unmodified OS does not know it is running in a virtualized environment and so, it can’t take advantage of any of the virtualization features.
- It can be resolved using para-virtualization partially.

### Types of Virtualization

#### 1. Full Virtualization
- **Description**: One or more OSs and the applications they contain are run on top of virtual hardware.
- **Guest OS Modification**: Not needed.
- **Critical Instructions**: Emulated by software through binary translation.
- **Performance**: Slower due to binary translation.
- **Example**: VMware (using binary translation).
- **Pros**: No need to modify OS; allows running unmodified OSs (legacy OS can be run without problems).
- **Cons**: Speed and flexibility; an unmodified OS does not know it is running in a virtualized environment and so, it can’t take advantage of any of the virtualization features.

#### 2. Hardware-Assisted Virtualization
- **Description**: Uses processor extensions (such as Intel®-VT or AMD-V) to intercept and emulate privileged operations in the guest.
- **Guest OS Modification**: Not needed.
- **Critical Instructions**: Handled by hardware extensions.
- **Performance**: Better than full virtualization due to hardware support.
- **Example**: Modern implementations of VMware, Hyper-V.
- **Pros**: Allows running unmodified OSs; removes many of the problems that make writing a VMM challenging.
- **Cons**: Speed and flexibility; an unmodified OS does not know it is running in a virtualized environment and so, it can’t take advantage of any of the virtualization features.

#### 3. Paravirtualization
- **Description**: The hypervisor offers interfaces to the guest OS that the guest OS can use instead of the normal hardware interfaces.
- **Guest OS Modification**: Needed.
- **Critical Instructions**: Replaced by hypercalls.
- **Performance**: Faster due to direct communication.
- **Example**: Xen, Denali, VMware ESX.
- **Pros**: Reduces overhead; provides faster access for resources such as hard drives and networks.
- **Cons**: High cost of maintaining a para-virtualized OS; requires modification of the guest OS.

#### Comparison: Full Virtualization vs Hardware-Assisted Virtualization  vs Paravirtualization 

| Feature                  | Full Virtualization       | Hardware-Assisted Virtualization | Paravirtualization        |
|--------------------------|---------------------------|----------------------------------|---------------------------|
| Guest OS Modification    | Not needed                | Not needed                       | Needed                    |
| Critical Instructions    | Emulated by software      | Handled by hardware extensions   | Replaced by hypercalls    |
| Performance              | Slower due to emulation   | Better due to hardware support   | Faster due to direct communication |
| Example                  | VMware (binary translation) | Modern VMware, Hyper-V           | Xen, Denali, VMware ESX   |
| Pros                     | No need to modify OS      | Allows running unmodified OSs    | Reduces overhead          |
| Cons                     | Speed and flexibility     | Speed and flexibility            | High cost of maintaining a para-virtualized OS |



#### Virtualization Technologies
Virtualization technologies are foundational to cloud computing, providing the ability to create and manage virtual environments.

- **Types of Virtualization**:
  - **Access Virtualization**: Allows remote access to applications or data regardless of the client device.
  
  - **Application Virtualization**: Enables applications to run in isolated environments, separate from the underlying operating system.
  
  - **CPU Virtualization**: Involves abstracting the CPU resources, allowing multiple operating systems to run concurrently on a single physical processor.
  
  - **Storage Virtualization**: Combines multiple storage devices into a single logical unit, simplifying storage management and improving efficiency.

#### Resource Mobility Patterns
Mobility patterns refer to the methods of migrating virtual machines and applications across environments. Key patterns include:

- **P2V (Physical to Virtual)**: Converting a physical machine into a virtual machine.
  
- **V2V (Virtual to Virtual)**: Migrating virtual machines from one hypervisor or environment to another.
  
- **V2P (Virtual to Physical)**: Moving a virtual machine back to a physical server.
  
- **P2P (Physical to Physical)**: Transferring data between two physical machines.
  
- **D2C (Device to Cloud)**: Sending data from an end-user device to the cloud.
  
- **C2C (Cloud to Cloud)**: Data migration between two cloud environments.
  
- **C2D (Cloud to Device)**: Sending data from the cloud to an end-user device.
  
- **D2D (Device to Device)**: Direct data transfer between two end-user devices.

#### Load Balancing and Virtualization

- **Basic Concepts**: Load balancing distributes workloads across multiple computing resources to optimize resource use, minimize response time, and avoid overload on any single resource. It ensures high availability and reliability of applications.

- **Network Resources for Load Balancing**: Involves using various network devices (like load balancers) to manage and distribute traffic among servers. This can include DNS-based load balancing, hardware load balancers, and software load balancers.

- **Advanced Load Balancing**: Advanced techniques include:
  - **Application Delivery Controller (ADC)**: A device that manages and optimizes application traffic, ensuring high availability and performance.
  
  - **Application Delivery Network (ADN)**: A system that provides application-aware load balancing, improving application performance and user experience.

- **Example of Load Balancing in Google Cloud**: Google Cloud provides load balancing services that automatically distribute incoming traffic across multiple instances of applications, ensuring optimal performance and reliability.

#### Scheduling Algorithms

##### 1. Round Robin
- **Description**: Distributes client requests to available servers in a circular order.
- **Pros**: Simple to implement; ensures even distribution of requests.
- **Cons**: Does not consider server load or response time.

##### 2. Weighted Round Robin
- **Description**: Similar to Round Robin but assigns a weight to each server. Servers with higher weights receive more requests.
- **Pros**: Allows differentiation between servers with different capacities.
- **Cons**: Still does not consider real-time server load or response time.

##### 3. Least Response Time
- **Description**: Directs requests to the server with the lowest average response time.
- **Pros**: Optimizes for faster response times.
- **Cons**: Requires continuous monitoring of server response times.

##### 4. Least Connections
- **Description**: Sends requests to the server with the fewest active connections.
- **Pros**: Balances load based on the number of active connections.
- **Cons**: May not account for the actual load or processing power of the servers.

##### 5. Weighted Least Connections
- **Description**: Combines the Least Connections method with server weights. Servers with higher weights receive more connections.
- **Pros**: Balances load while considering server capacity.
- **Cons**: Requires accurate weight assignment and monitoring of active connections.

##### 6. Other Customizations Based on Certain Parameters
- **Description**: Custom algorithms that distribute requests based on specific parameters such as server health, geographic location, or application-specific metrics.
- **Pros**: Highly flexible and can be tailored to specific needs.
- **Cons**: Complexity in implementation and maintenance.

##### Comparison Table

| Algorithm                      | Description                                           | Pros                                      | Cons                                      |
|--------------------------------|-------------------------------------------------------|-------------------------------------------|-------------------------------------------|
| Round Robin                    | Distributes requests in a circular order              | Simple; ensures even distribution         | Ignores server load and response time     |
| Weighted Round Robin           | Distributes requests based on server weights          | Differentiates server capacities          | Ignores real-time load and response time  |
| Least Response Time            | Directs to server with lowest average response time   | Optimizes for faster response times       | Requires continuous monitoring            |
| Least Connections              | Sends to server with fewest active connections        | Balances based on active connections      | May not reflect actual server load        |
| Weighted Least Connections     | Combines Least Connections with server weights        | Considers server capacity and connections | Requires accurate weights and monitoring  |
| Customizations                 | Based on specific parameters                          | Highly flexible and tailored              | Complex implementation and maintenance    |

#### Hypervisors

- **Virtual Machine Technology and Types**: Hypervisors allow multiple operating systems to run on a single physical machine by creating and managing virtual machines (VMs).
  - **Type 1 Hypervisor (Bare-Metal)**: Runs directly on the hardware (e.g., VMware ESXi, Microsoft Hyper-V).
  - **Type 2 Hypervisor (Hosted)**: Runs on a conventional operating system (e.g., VMware Workstation, Oracle VirtualBox).

- **VMware**: A leading provider of virtualization technology, offering solutions for creating and managing VMs, including VMware vSphere, which provides a comprehensive platform for virtualization management.

- **vSphere Machine Imaging**: vSphere supports machine imaging, allowing users to create images of virtual machines for rapid deployment. 

- **Open Virtualization Format (OVF)**: A standard for packaging and distributing virtual appliances, ensuring interoperability between different virtualization platforms.

#### Porting Applications in the Cloud

- **Simple Cloud API and AppZero Virtual Application Appliance**: These tools facilitate the migration of applications to the cloud, enabling developers to create applications that can easily integrate with cloud services.

- **Concepts of Platform as a Service (PaaS)**: PaaS provides a platform allowing developers to build, deploy, and manage applications without dealing with the complexities of infrastructure management.

- **Definition of Services**: PaaS offers a suite of services, including development frameworks, database management, and integration capabilities, which developers can leverage to create applications efficiently.

- **Distinction between SaaS and PaaS**:
  - **SaaS (Software as a Service)**: Delivers fully functional software applications over the internet (e.g., Salesforce).
  - **PaaS (Platform as a Service)**: Provides a platform for developers to build and deploy applications (e.g., Force.com). Salesforce.com offers its services as SaaS, while Force.com is its PaaS offering for developers.

- **Application Development Using PaaS Application Frameworks**: PaaS frameworks provide tools and services to streamline application development, offering libraries, templates, and APIs to enhance productivity.

### Discussion of Google Applications Portfolio

- **Indexed Search**: Google’s search engine utilizes advanced algorithms and indexing techniques to provide relevant search results efficiently.

- **Dark Web**: Refers to parts of the internet not indexed by traditional search engines, often requiring special software for access.

- **Aggregation and Disintermediation**: Google’s services aggregate information from various sources, providing users with streamlined access, while disintermediation eliminates intermediaries in transactions.

- **Productivity Applications and Services**: Google offers several productivity tools, including Google Docs, Sheets, and Slides, which allow real-time collaboration and cloud storage.

- **AdWords**: Google AdWords (now Google Ads) is an advertising service enabling businesses to display ads on Google’s search engine and other platforms.

- **Google Analytics**: A web analytics service that tracks and reports website traffic, helping businesses understand user behavior and optimize their online presence.

- **Google Translate**: A service that provides translation between various languages using machine learning algorithms.

- **Google Toolkit**: Includes various Google APIs that developers can use to integrate Google services into their applications.

- **Major Features of Google App Engine Service**:
  - **Automatic Scaling**: Adjusts resources automatically based on traffic.
  - **Integrated Services**: Offers built-in services like data storage and user authentication.
  - **Managed Environment**: Handles infrastructure management, allowing developers to focus on coding.

#### Windows Azure Platform

- **Microsoft’s Approach**: Azure is a cloud computing platform that provides a range of services, including computing, analytics, storage, and networking.

- **Architecture**: Azure’s architecture consists of multiple layers, including infrastructure, platform, and software services, providing flexibility and scalability.

- **Main Elements**:
  - **Compute Services**: Virtual machines, app services, and container services.
  - **Storage Services**: Blob storage, SQL databases, and file storage.
  - **Networking**: Virtual networks, load balancers, and VPN gateways.

- **Overview of Windows Azure AppFabric**: AppFabric provides a suite of middleware services for building and integrating applications in the cloud, enhancing connectivity and management.

- **Content Delivery Network (CDN)**: Azure CDN delivers high-bandwidth content globally, reducing latency and improving user experience.

- **SQL Azure**: A cloud-based relational database service that supports SQL Server capabilities, offering scalability and managed services.

- **Windows Live Services**: A suite of cloud-based services for consumers and businesses, providing tools for communication, collaboration, and data storage.
