# Advanced Physical Design using OpenLANE & SkyWater 130nm PDK
![Advanced-Physical-Design-using-OpenLANE_Sky130_1](https://user-images.githubusercontent.com/30654675/124450662-47901f00-dda2-11eb-9254-78097d7d8fee.png)



This Repository mainly created to focus on the work-done in  5 Days workshop of Adavance Physical Design using OpenLANE/SkyWater130. The Workshop mainly focus on  to  hands on experience of the efabless OpenLANE VLSI design flow RTL2GDS and the Skywater 130nm PDK. OpenLANE is an open source VLSI flow built around open source tools with the goal to produce clean GDSII with no human intervention. PicoRV32 is a CPU core that implements the RISC-V RV32IMC Instruction Set .In this course this is used as an example to explain the flow . 


<h2>Contents:</h2> 
<h3>Course Agenda: <br/>
  
  <h4>Day1 – Introduction  of open-source EDA, OpenLANE and Sky130 PDK </h4>
  <h5>1.1 How to talk to computers</h5>
<h5>1.2 SoC design and OpenLANE</h5>
<h5>1.3 Commands used in Open-Source EDA Tools</h5>
<h5>1.4 Get familiar to open-source EDA tools</h5>
  
<h4>Day 2 - Understand importance of good floorplan vs bad floorplan and introduction to library cells</h4>

  <h5>2.1 Chip Floor planning considerations</h5>
<h5>2.2 Library Binding and Placement</h5>
<h5> 2.3 Cell design and characterization flows</h5>
<h5>2.4 General timing characterization parameters</h5>
  
<h4>Day 3 - Design and characterize one library cell using Magic Layout tool and ngspice</h4>

<h5>3.1 Labs for CMOS inverter ngspice simulations
<h5>3.2 Inception of Layout – CMOS fabrication process
<h5>3.3 Sky130 Tech File Labs</h5>
  
<h4>Day 4 - Pre-layout timing analysis and importance of good clock tree</h4>

<h5>4.1 Timing modelling using delay tables</h5>
<h5>4.2 Timing analysis with ideal clocks using openSTA</h5>
<h5>4.3 Clock tree synthesis TritonCTS and signal integrity</h5>
<h5>4.4Timing analysis with real clocks using openSTA</h5>
  
<h4>Day 5 - Final steps for RTL2GDS</h4>
<h5>5.1 Routing and design rule check (DRC)</h5>
<h5>5.2 PNR interactive flow tutorial</h5>

  
  <h3>Day 1</h3>
  <h4>How Talk Computers:</h4>
  
  <p> Computers are machine which are only able to understand the binary numbers. Human understandable high  language  will be converted into machine understandable by compiler.</p>
  <br/>
      
![how to talkscomp1](https://user-images.githubusercontent.com/30654675/124459552-e0776800-ddab-11eb-99c6-fd5f1dab84de.PNG)
  
  <p> An figure below will show the high level to low level conversion process </p> 
  
 ![softto hard](https://user-images.githubusercontent.com/30654675/124462560-72cd3b00-ddaf-11eb-8290-3eec5c091f9c.PNG) 
  
  <h4> 1.2 OpenLANE  ASIC Flow- RTL2GDS </h4>
  
  <p> It is a automated process. It consist of several components like OpenROAD,Yosys, Magic,Netgen, TritonRoute, custom scripts, OpenSTA etc. The Below figure will show the OpenLANE flow</P>
  
  ![openlneflow1](https://user-images.githubusercontent.com/30654675/124464407-c771b580-ddb1-11eb-82d4-9c8ff3bf0777.PNG)

  
  
 <p> It consists of several stages. <br/>
  Yosys- It Perform RTL Synthesis <br/>
  abc - It performs Technology mapping <br/>
  OpenSTA- It performs STA <br/>
  
   ioplacer- Places the macros input and output ports <br/>
   pdn- It generates the power distribution network <br/>
   RePLace- It performs Global placement <br/>
   
   TritonCTS- Performs the synthesis of clock distribution network <br/>
   SPEF-extractor- Performs the spem extraction <br/>
   Magic- Streams out final  GDSII layout file from layout DEF <br/>
   </p>
     
  <h3>1.3 The commands used in  OpenSTA tool:</h3>
  prep_design <design> </br>
  run_synthesis</br>
  run_floorplan</br>
  run_placement</br>
  run_cts</br>
  run_routing</br>
  run_magic</br>
  run_magic_drc</br>
  run_lvs</br>
  
 <h3> 1.4 Open-Source EDA tools familirization:</h3>

  The below figure shows the opensource tools to execute and  use the command below nad run as either automatively or interactively </br>
  run ./flow.tcl interactive 
      ![image](https://user-images.githubusercontent.com/30654675/124468495-cbec9d00-ddb6-11eb-9eec-9f2ad693dd12.png)
 
   <p> Next Import the package  with below command and prepare and setup the design </P>
      package requre  openalane</br>
      prep -design picotv32a</br>
     ![image](https://user-images.githubusercontent.com/30654675/124471723-d741c780-ddba-11eb-84bf-b6d63b7ad9b4.png)


    
    
    
    
    
    
    
  <h3>Day 2</h3>
  <h3>Day 3</h3>
  <h3>Day 4</h3>
  <h3>Day 5</h3>

