[Personal Learning Record](../../personal_learning_record/personal_learning_record.md) | [IT Proposals](../proposals/README.md) 

# Council Proposal 2

## Explanation of this proposal
*What do you think this proposal might mean? How might it be implemented?*
The council runs software locally in its own server room. This means hardware, power, cooling, and maintenance are all managed on-site.Move these applications into the cloud (e.g., Microsoft Azure, AWS, Google Cloud). Instead of owning and maintaining servers, the council would consume computing resources as services.This aligns with other modernization proposals on the page (like hot desking, VPN access, and digital-first services), all aimed at making IT more flexible, scalable, and cost-efficient.Scalability: Cloud platforms can expand or shrink resources based on demand.

Cost Efficiency: Reduces capital expenditure on hardware; shifts to pay-as-you-go operational costs.

Resilience: Cloud providers offer redundancy, backups, and disaster recovery.

Accessibility: Staff can access applications from anywhere, supporting hybrid work models.

Focus: IT teams spend less time maintaining hardware and more time improving services.Data Security: Sensitive council data must be protected; cloud migration requires strong compliance measures.

Vendor Lock-in: Choosing one provider may limit flexibility later.

Connectivity: Reliable Internet access becomes critical, since services are no longer local.

Change Management: Staff training and process adjustments are needed to adapt to cloud-based workflows.is about modernizing IT by replacing on-premises servers with cloud services, reducing physical infrastructure dependence while increasing flexibility, scalability, and resilience. Transition existing software to a secure, cloud-native environment.
Reduce operational and hardware maintenance costs.
Improve application performance, availability, and scalability.
Enable remote collaboration and access for employees.
Establish a foundation for AI, analytics, and cloud-native innovation. Inventory of software, databases, and applications running on-premises.
Analysis of application dependencies and interconnections.
Assessment of server resources, storage architecture, and network capacity.
Identification of legacy systems requiring refactoring or replacement.The proposed cloud migration will utilize a phased, hybrid approach:
Rehost (Lift-and-Shift): Initial migration of low-complexity applications with minimal modification.
Replatform: Optimize selected applications for cloud-native services (e.g., managed databases, containerization).
Refactor/Re-architect: Gradually modernize legacy software that requires structural changes to leverage cloud elasticity and automation.Deployment Model: Hybrid cloud solution to balance sensitive on-prem workloads with scalable public cloud services.
Primary Providers: AWS, Microsoft Azure, or Google Cloud Platform, selected based on SLA, global coverage, security, and cost efficiency.
Tools & Services: Managed migration tooling (e.g., AWS DMS, Azure Migrate), container services, automated backups, monitoring, and disaster recovery.
Phased Migration Plan
Planning & Design: Define objectives, KPIs, and a detailed roadmap.
Pilot Migration: Move non-critical applications to validate migration tools, test connectivity, and minimize risk. Full Migration: Sequentially migrate remaining workloads, implementing dependencies and validation checks.
Testing & Optimization: Conduct performance, load, and security testing; tune cloud resources.
Operational Handover: Establish monitoring, access controls, and ongoing cloud governance procedures.Infrastructure provisioning & cloud subscriptions
Migration tools and licensing
Professional services (Cloud Architects, DevOps, security specialists)
Contingency fund for unexpected complexity

Approve the migration plan and budget.
Schedule project kickoff and assemble migration team.
Conduct detailed application audit and dependency mapping.
Initiate pilot phase with selected applications.

This proposal provides a structured approach to ensure a secure, scalable, and cost-efficient migration to the cloud, positioning [Client.Company] for ongoing digital transformation and operational resilience.

## Technologies and research relevant to this proposal
*Which class sessions and personal research refers to technology in this proposal. Link to examples.*

Under the traditional model, the enterprises need to purchase not only infrastructure such as hardware 
but also software licenses to establish an IT system, and need specialized personnel to maintain. It needs 
to upgrade various facilities including hardware and software to meet the demands when the scale of 
business extends. For the enterprises, what they really need is only the tool which can complete the work 
and improve efficiency but the hardware and software themselves. 

For the individuals, we need to install much software to use the computer normally, but much software isn’t free, so it is very uneconomical for the users who don’t often use the software. Could have a kind of service that provides all the software we 
need for us to rent? Thus we only need to pay a small amount of rent while we using it, so we can save 
much money. We use electricity every day, which is supplied by the power station instead of our own 
generators; we use water every day, which is supplied by the water plants instead of our own wells. This 
mode saves resources greatly and facilitates our lives. Facing the problems brought by the computer, can 
we use the computer resources like using water and electricity? These ideas eventually lead to the 
emergence of cloud computing.  

Cloud computing is a new kind of commercial computing model developed on the basis of grid 
computing, public computing and SaaS. It can distribute computing tasks to the resources pool consisting 
of massive computers, enabling different application systems to acquire computing power, storage space 
and various software services according to needs. The ultimate goal of cloud computing is to provide 
calculation, services and applications as a public facility for the public, So that people can use the 
computer resources just like using water, electricity, gas and telephone. Therefore, the enterprises can 
save many costs purchasing hardware and software. This paper introduces the definition of could 
computing and its main service patterns, summarizes the characteristics, and focused on the key 
technologies such as the data storage, data management and programming model. 

Proposals focused on educational technology might address how digital learning platforms (like Moodle or Zoom) affect student engagement or learning outcomes. This could include case studies on technologies implemented in classroom settings.In proposals related to data science, technology is key; specifying the software (like Python, R, or machine learning frameworks) used in your research methodology communicates advanced technical understanding.proposals addressing climate change or environmental science might examine technological interventions such as renewable energy systems (solar panels, wind turbines) or environmental monitoring tools (IoT devices for data collection).


Zhang, S., Yan, H. and Chen, X., 2012. Research on key technologies of cloud computing. Physics Procedia, 33, pp.1791-1797.

https://www.sciencedirect.com/science/article/pii/S1875389212015994


## Initial Analysis of the Proposal
*Use some simple analysis tools to help you think through whether the proposal is a good idea*

### SWOT Analysis
*You can use html tables in markdown*
 <table>
  <tr>
    <th>Strength</th> 
    <th>Weakness</th>
  </tr>
  <tr>
    <td>
      <ol>
        <li>you can increase or decrease computing power, storage, or network capacity instantly</li>
        <li>No need to buy new hardware for growth or worry about overbuilding for future need</li>
        <li>idea</li>
      </ol> 
    </td>
    <td>
      <ol>
        <li>Cloud can become more expensive than on prem if not managed well</li>
        <li>Continious usage, data transfer fees, and scaling resources can lead to unnexpected bills</li>
        <li>long term heavy workload may cost less on owned hardware</li>
      </ol> 
    </td>
  </tr>
  <tr>
    <th>Opportunity</th>
    <th>Threat</th>
  </tr>
  <tr>
    <td>
      <ol>
        <li>Running server in the cloud opens acesss to modern tools,Artificial intelligence,Big data and analytics,Automation and develop tools</li>
        <li>low latency service for global user</li>
        <li>idea</li>
      </ol> 
    </td>
    <td>
      <ol>
        <li>Data breaches from attackers exploiting misconfigurations or stolen credentials.</li>
        <li>Account hijacking compromised admin account </li>
        <li>Knock critical service offline</li>
      </ol> 
    </td>
  </tr>
</table> 

### PEST Analysis
*You can use html tables in markdown*

 <table>
  <tr>
    <th>Political</th>
    <th>Economic</th>
  </tr>
  <tr>
    <td>
      <ol>
        <li>Where data can be stored data residency</li>
        <li>What data may leave the country</li>
        <li>Acess to cloud regions in certain countreis</li>
      </ol> 
    </td>
    
      <ol>
        <li>Capital expanditure buying hardware, server UPS, cooling </li>
        <li>operational expanditure montthly cloud service fees</li>
        <li>idea</li>
      </ol> 
    </td>
  </tr>
  <tr>
    <th>Social</th>
    <th>Technological</th>
  </tr>
  <tr>
    <td>
      <ol>
        <li>Upskilling IT staff in cloud technologies</li>
        <li>Training employees to use cloud platforms and tools</li>
        <li>idea</li>
      </ol> 
    </td>
    <td>
      <ol>
        <li>New computer options</li>
        <li>Ai and machine learning tools</li>
        <li>Advanced data analytics</li>
      </ol> 
    </td>
  </tr>
</table> 

## Questions to ask about the proposal
*Without knowing how exactly the council will implement this proposal, what questions should be raised?*

* question 1
* question 2

## Evaluation of the proposal
*Povide a breif evaluation based on what you know*

