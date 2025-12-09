[Personal Learning Record](../../personal_learning_record/personal_learning_record.md) | [IT Proposals](../proposals/README.md) 

# Council Proposal 4

## Explanation of this proposal
*What do you think this proposal might mean? How might it be implemented?*

Raspberry Pi microcomputers as Internet of Things (IoT) devices to monitor foot traffic in council-managed spaces such as libraries and museums. The Raspberry Pi would act as a low-cost, programmable sensor hub, collecting data on how many people enter and exit these facilities. Raspberry Pi is highlighted because it is affordable, flexible, and widely used in educational and experimental IoT projects. As IoT devices, the Pis would connect to the council’s network, transmitting data in real time for analysis. This aligns with other modernization proposals on the page (like cloud migration and AI simplification), all aimed at making council operations more efficient and data-driven.Provides accurate visitor counts, helping with staffing, resource allocation, and opening hours. Raspberry Pi devices are inexpensive compared to commercial people-counting systems. Easy to deploy across multiple sites (libraries, museums) without major infrastructure investment Enables the council to analyze usage trends and plan services accordingly.Demonstrates practical use of IoT in public services, aligning with digital-first strategies. Raspberry Pi data can be stored and analyzed in the cloud. Raspberry Pi data can be stored and analyzed in the cloud. Visitor data can inform online service design and resource allocation.AI could analyze traffic patterns to optimize operations.IoT devices must be secured against cyber threats.


Raspberry Pi IoT devices to track visitor numbers in libraries and museums, providing valuable data for resource planning and service improvement. It’s innovative and cost-effective, but requires careful attention to accuracy, privacy, and  This proposal explores the use of the Raspberry Pi in the public space. The presence of
 this machine in public areas allows for the discussion of some key challenges such
 as electronic waste and how it affects distant regions. Another social topic where this
 thesis can be used to create a discussion is the challenge identified by the European
 Commission in providing sufficient programmers for future jobs in the EU. Application
 of this machine in libraries can show how empowering students with – even basic
 skills – allows them to create new concepts where multiple organisations may benefit
 from. This can be done by intensifying contacts between libraries and schools or non
profit organizations focussed on coding. It also helps to raise awareness surrounding
 educational policy. All of these topics are explored and shortly presented, all of the
 used arguments can be popularized to spread the message to a wider audience.integration.
 
 The goal was to provide a program that was easy to use by public visitors and could
 be installed and configured by non-technical users. For this a manual was written and
 Python scripts where used to help users configure the Raspberry Pi. An implicit focus
 on security was present when developing the manual; yet a balance had to be found
 to prevent making installation too difficult. Therefore the focus was on preventing
 remote access by disabling SSH (this was removed out of the final version as this
 was disabled by default in the November release of the Raspbian OS) and changing
 the password of the Raspbian sudo account. Aside from that a non-sudo account had
 to be added so that no harmful commands could be executed by visitors. Doing all
 this proved to be challenging in the first version of the manual which is why the scope
 of programs included to accomplish successful installation had to be expanded by
 adding an assistant tool and some scripts that automated or facilitated file-editing
 tasks. In doing so this thesis wishes to inscribe itself in the DH-tradition of makers and
 Minimal Computing workgroups who have been using this machine in a variety of
 projects. As a concluding remark it was found that the Raspberry Pi is a capable, yet
 cost-effective machine that can be applied in a wide variety of contexts. Yet applying
 the machine itself is not a trivial task. First of all there are some limitations that
 accompany this machine. Secondly this machine is not targeted towards being used
 as an off-the-shelve device, meaning that a moderate amount of effort has to be put
 in to make it run as desired. This can be quite challenging as there’s a learning-curve

Strategic Fit: This aligns with other modernization proposals on the page (like cloud migration and AI simplification), all aimed at making council operations more efficient and data-driven.

Functionality: Equipped with sensors (e.g., infrared, cameras, or motion detectors), the Pi can count people passing through entry/exit points.

## Technologies and research relevant to this proposal
*Which class sessions and personal research refers to technology in this proposal. Link to examples.*

Previously, the description of museum artefacts was largely dependent on tour guides 
and information cards (Marshal at al., 2016). Today, these concepts tend to be digitalised. 
Along with the development of mobile and tangible technologies, museums have started 
to present descriptions of museum artefacts through multimedia content using mobile 
applications or tangible interaction systems. Although the use of multimedia 
presentations in museums has improved the museum visiting experience, the interaction 
between museum artefacts and visitors are still lacking and mostly passive in nature. Most often, the cultural heritage artefacts cannot be touched by visitors. Recent research 
has focused on using physical replicas to overcome this lack of interactions to make 
museums and their artefacts more engaging for visitors. Emerging technologies such as 
3D printing and Internet of Things (IoT) have been used to create tangible smart replicas 
to access an additional layer of content that complements the traditional factual 
information that is generally provided about artefacts in a museum (Marshal at al., 2016). Other research has explored the use of digital technologies with games to improve 
museum visiting experiences. For example, to enhance learners’ motivation to learn 
about fossil in a museum, Yoshida et al. (2015) developed a virtual paleontological 
environment to support experiential learning with entertainment. Such games, designed 
for a primary purpose other than pure entertainment is known as serious games 
(Lamaarti et al., 2014). From the review study conducted by Lamaarti et al. (2014), many 
serious games have been developed for promoting cultural learning (Sagae et al., 2010; 
Froschauer et al., 2011; Bellotti et al., 2012). However, current research studies on 
serious games are still limited to mobile and desktop games where users often learn 
about culture and history from the vicinity of their homes (Susi et al., 2007; Coenen et 
al., 2013; Antoniou et al., 2013). The role of museums itself has changed over the years as education is not the only goal 
for visitors to visit a museum (Kaplan, 1993). Museums now find that they play an 
increasing role in supporting the development of communities other than their traditional 
role of collecting, preserving and sharing rich collections. Museums can help emphasise 
the uniqueness of community’s identity and be able to bring different community groups 
together. By having an open access to objects, information and knowledge visitors can 
see for themselves how cultures may be reflected in ways that encourage new 
connections (Kelly, 2007). Technologies that focus strictly on the learning goal of visitors.

https://eprints.nottingham.ac.uk/60804/1/Thesis_HuangHai_Final_edit.pdf

The technological revolution has had a major impact upon museums, and many of them 
make very effective use of a wide variety of interactive technologies. However, there is 
a paradoxical concern that technologies that focus too much on learning goals can 
distract from the meaning making processes, which are the very things that the 
technology is trying to promote (Cosley et al., 2008). The key issue is to consider how 
the technology promotes discussion and reflection in order to facilitate meaning making.  
Designers have demonstrated an increased interest in designing for reflection (Sengers 
et al., 2005; Baumer, 2015). Reflection can be described as a “generic term for those 
intellectual and affective activities in which individuals engage to explore their 
experiences in order to lead to new understandings and appreciations” (Boud et al., 
1985). Fleck and Fitzpatrick (2010) further synthesized the literature on reflection into a 
framework consisting of different levels of reflection. There have been some examples 
of how technology can be used to support reflection in learning (Lin et al., 1999), teaching 
(Fleck & Fitzpatrick,2009), health (Mamykina et al., 2008), persuasive behaviour 
(Ghajargar et al., 2018), personal informatics (Li et al., 2010) and design (Gaver et al., 
2003). Although, there has been some studies that focussed on exploring possible 
approaches to reflective design in cultural settings, little evidence is provided so far to 
suggest their effectiveness in engaging visitors in reflective thoughts (Baumer et al., 
2014). In times of increasing ethnic tensions throughout the world, the role of museums 
as repositories of heritage is ever more important to help people understand and reflect 
on cultural identities e.g. cultural similarities and differences towards wider national unity. 



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
        <li>Flexible sensor compability</li>
        <li>small Physical Footprint</li>
        <li>low cost and highly accessible</li>
      </ol> 
    </td>
    <td>
      <ol>
        <li>Limited processing Power</li>
        <li>Reliance on External storage</li>
        <li>Network Dependance</li>
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
        <li>Track how many people are inside at any moment.</li>
        <li>Help manage capacity limits, social distancing, or safety regulation</li>
        <li>identity peak hours, seasonal trends, and popular exhibits or sections.</li>
      </ol> 
    </td>
    <td>
      <ol>
        <li>SD card corruption from power loss or frequent writes </li>
        <li>Failure due to heats, dust or humidity</li>
        <li>delay alarts or notification</li>
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
        <li>Adoption of low cost technologies like raspberry Pi</li>
        <li>fire safety occupancy limits</li>
        <li>\Emergency evacuation protocols</li>
      </ol> 
    </td>
    <td>
      <ol>
        <li>low initial cost</li>
        <li>Reduced Operational cost</li>
        <li>cost effecive data analytics</li>
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
        <li>Improve public safety</li>
        <li>Data Transarency and trust</li>
        <li>Encourage of smart and inclusive culture</li>
      </ol> 
    </td>
    <td>
      <ol>
        <li>Software Technology</li>
        <li>Connectivity Technologies</li>
        <li>IOT and egde integration
  
       </li>
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

