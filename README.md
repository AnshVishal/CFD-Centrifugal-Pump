<h1 align='center'>Computing Turbomachinery Flow of Centrifugal Pump </br>
<h4 align='center'>Dynamic Meshing &nbsp | &nbsp Steady State &nbsp | &nbsp Turbulence (k-omega SST) and Turbomachinery &nbsp | &nbsp Data Analysis</h4></h1>

<p align="right">Minor Project 2 - Turbomachinery,</br> Flowthermolab </br>30/10/2025</p>
<h2 align='left'>Project Overview</h2>
<p align = "left">This project presents a comprehensive CFD investigation of centrifugal flow of a centrifugal pump to analyze: </br>
<ul>
      <li>Flow behavior at different mass flow rate</li>
      <li>Head (m)</li>
      <li>Efficiency (%)</li>
      <li>Mesh Convergence</li>
      <li>Validation Study</li>
</ul>
The study evaluates the centrifugal pump under multiple mass flow rate conditions to map a metrics for head and efficiency values, evaluate performance and identify possible design improvements from a CFD engineering perspective.
</p>

<h2 align "left">Problem Statement</h2>
<p align='left'><ul><li>To simulate and analyze the performance of centrifugal pump</li>
  <li>To understand the working of centrifugal pump, evaluate performance and provide some insight on possible design changes/optimization</li></ul></p> 

<h2 align = "left">Software Used</h2>
<p align='justify'>
      1. &nbsp Ansys Space-Claim ------- Geometry Cleanup and refinement </br> 
      2. &nbsp Ansys Fluent Mesher ----- Mesh / Grid Generation </br>
      3. &nbsp Ansys Fluent ------------- Computation </br>
      4. &nbsp Ansys Post Processor ---- Post Processing </br>
      5. &nbsp MATLAB ------------------ Data Analysis & Scientific Plots</p>
    
<h2 align='left'>Methodology</h2>

<h3 align = "left">1. Geometry Cleanup and Refinement</h3>
<p align = "justify">
      <ul><li>Geometry was cleaned and optimized for computation.</li>
            <li>Dimensions of the geometry: 
            <ul><li>Inlet Dia (𝐷1) ---------------------------- 195 mm</li>
              <li>Outlet Dia ------------------------------- 137 mm</li>
              <li>Interface Dia ----------------------------- 562 mm</li>
              <li>Blade Diameter -------------------------- 274 mm</li>
              <li>Impeller Diameter (𝐷2) ------------------ 281 mm</li>
              <li>Inlet Area (𝐴1) --------------------------- 0.0298 𝑚<sup>2</sup></li>
              <li>Impeller Area (𝐴2) ----------------------- 0.248 𝑚<sup>2</sup></li>
              <li>Backward Curved Blade angle (𝛽2) ----- 34<sup>𝑜</sup></li>
              <li>Blade width at tip, b2 ------------------- 0.0142 m</li>
              <li>Blade width at hub, b1 ------------------ 0.008 m</li></ul>
            </li></ul></p>
            
<p align = "center"><img width="360" height="417" alt="image" src="https://github.com/user-attachments/assets/687333b2-9a3f-49d2-8829-520cd4f14f68" /><img width="480" height="571" alt="image" src="https://github.com/user-attachments/assets/6f0307bf-6811-4c0a-bea9-5a7710994019" />
<br/>
    <b>Centrifugal Pump Geometry and Calculations</b></p>

<h3 align = "left">2. Mesh Details</h3>
<p align = "justify">
      <ul><li>Focused on mesh refinement at: Blade region.</li>
        <li>Mesh Details mentioned here are for Volute and Rotor together, however during meshing both volute and rotor were meshed independently. 
            <li>Following Mesh Details are for coarse mesh, medium mesh, and fine mesh: 
                  <ul><li>Reynolds Number ------------------------------------------------------- 2.3e06</li>
                    <li>Y+ ------------------------------------------------------------------------ 1</li>
                    <li>First Layer height -------------------------------------------------------- 8e-06 m</li>
                    <li>Local Sizing, Face Size --------------------------------------------------- 2.7 mm</li>
                    <li>Surface mesh (Min Size, Curvature Normal Angle) --------------------- (2.5 mm, 12),(1 mm, 12),(0.63 mm, 12)</li>
                    <li>Boundary Layer (Offset Method, first height, number of layers) ------- last Ratio, 0.12 mm, 4</li>
                    <li>Volume Mesh (Type, Min Cell length, Max. Cell length) ---------------- (Poly-hexcore, 2.5 mm, 8 mm), (poly-hexcore, 1 mm, 8 mm), (Poly-hexcore, 0.63 mm, 2.52 mm)</li>
                    <li>Total mesh Elements ----------------------------------------------------- 231682, 395832, 649464 </li>
                    <li>Average orthogonality --------------------------------------------------- 0.88, 0.92, 0.94 </li>
                  </ul></li></ul>
</p>
<p align = "center"><img width="360" height="628" alt="image" src="https://github.com/user-attachments/assets/caaf0c7a-7fe7-45e0-9a61-b4a638abe597" /><img width="360" height="623" alt="image" src="https://github.com/user-attachments/assets/5d9ca91f-e90e-496a-8f13-1e8184b634c7" /><br/>
            <b>Centrifugal pump Meshing (Different Mesh Convergence Cases)</b></p>
  

<h3 align = "left">3. Solver Settings</h3>
<table align = "center">
      <tr><th>Parameter</th><th>Setting</th></tr>
      <tr><td>Solver Type</td><td>Pressure-Based</td></tr>
      <tr><td>Time</td><td>Steady</td></tr>
      <tr><td>Turbulence Model</td><td>k-ω SST</td></tr>
      <tr><td>Material</td><td>Water (Liquid)</td></tr>
      <tr><td>Rotational Velocity</td><td>1500 RPM and 1800 RPM</td></tr>    
      <tr><td>Mass Flow rate at outlet</td><td>40 kg/s to 120 kg/s</td></tr>
      <tr><td>Solver Scheme</td><td>Coupled with PRESTO! Pressure Solver</td></tr>
      <tr><td>Momentum Discretization</td><td>second order</td></tr>
      <tr><td>Residuals & Reports</td><td><ul><li>Mass flow rate at inlet and outlet,</li> <li>torque on impeller and</li> <li>velcoity at blade</li></ul></td></tr>
      <tr><td>Initialization</td><td>Hybrid</td></tr>
      <tr><td>Iterations</td><td>2000</td></tr>
</table>

<h3 align = "left">4. Results</h3>

<h4 align = "left">1. Mesh Convergence Test</h4>
<p align = "left">It can be concluded from the Mesh Convergence study that Medium Mesh is good to start the further study, as per the time convergence and computational power criteria.</br>
<b>Note: </b> <ul><li>Convergence Criteria marked when the mass flow rate ratio of outlet to inlet got very close to 1.</li>
  <li>All the simulations were run for 2000 iterations</li>
  <li>Medium type mesh showed ~3% error for head value when compared to Fine Mesh</li>
</ul></p>
  <p align = "center"><img align = "center" width="360" height="397" alt="image" src="https://github.com/user-attachments/assets/a96da878-688f-4455-afd6-31adf3c987cc" /><br/>
<b>Error Percentage (Force and Torque), Surface (Propeller)</b></p>

<h4 align = "left">2. Validation Study</h4>
<p align = "left">Validation Study shows that medium mesh showed maximum resemblance of head value with theoretical value within 81% when simulated pressure-based solver at steady time for 2000 iterations monitoring mass flow rate at inlet and outlet as convergence criteria within 5% difference for results to conclude.</p>
<p align = "center"><img align = "center" width="480" height="926" alt="image" src="https://github.com/user-attachments/assets/d052e6fe-97e4-4b4d-b73d-dcecf5031cbe" /><img align = "center" width="480" height="926" alt="image" src="https://github.com/user-attachments/assets/7102687d-45b2-4abd-869a-0bf566e0ac10" /><br/>
<b>Number of Elements vs Head [m] and Efficiency [%] </b></p>

<h4 align = "left">3. Case Results</h4>
<p align = "left"><ul><li>Optimal Head loss for mass flow rate 80 kg/s at 1500 RPM (1), ratio of theoretical to CFD head is 0.81</li>
  <li>Head loss reduces with increasing mass flow rate.</li>
  <li>Efficiency is max at 80 to 100 kg/s mass flow rate for both 1500 RPM and 1800 RPM</li>
  <li>From the above point we can say, for better efficiency operate centrifugal pump at above specified condition.</li></ul></p>
<p align = "center"><img width="480" height="926" alt="image" src="https://github.com/user-attachments/assets/4364cc3b-6330-4d05-a4d9-a3156416ee4e" /><img width="480" height="926" alt="image" src="https://github.com/user-attachments/assets/10f277e3-a61a-401c-80a2-28f364ce4372" /><br/>
<b>Head [m] and Efficiency [%] vs Mass Flow Rate [kg/s]</b></p>

<h4 align = "left">4. Case Results: Video Animation</h4>
<p align = "center">  <br/>
<b>Velocity and Pressure Conoturs Animation</b></p>

<h3 align = "left">5. Discussion & Future Scope</h3>
<p align='justify'><b>Mapping:</b></br>
<ul><li>Generated full characteristic curves (Head [m] & Efficiency [%] vs. mass flow rate [kg/s]) for 1500 RPM and 1800 RPM.</li>
  <li>Data covers a wide operational range: 40 to 120 kg/s.</li></ul>
<b>Key Performance Benchmark:</b>
<ul><li>Peak Efficiency: 51.13% for 1500 RPM at 100kg/s mass flow rate.</li>
<li>Best Efficiency Point (BEP): Located at 80 kg/s, 90 kg/s, 100 kg/s for 1500 RPM rotational velocity.</li></ul>
<b>Head-Flow Characteristics:</b>
<ul><li>The head-Flow curve shows decreasing trend with increasing flow rate for both 1500 RPM and 1800 RPM, highlighting standard pump behavior.</li></ul>
<b>Efficiency Flow Characteristics:</b>
<ul><li>The peak efficiency for 1800 RPM is lower and occurs at a shifted flow rate compared to 1500 RPM.</li>
  <li>This indicates that the centrifugal pump design (impeller blade angles, volute) is tuned for a specific operating point (~80-100 kg/s at 1500 RPM). When run at 1800 RPM, the increased flow velocities exacerbate losses (friction, shock, recirculation), leading to lower peak efficiency. The pump is inherently designed for its 1500 RPM duty.</li></ul>

</p>

<h2>Recommended Repository Structure</h2>

<pre>
CFD-Study-Globe-Valve/
│
├── README.md
├── Geometry image
├── Mesh images
├── Fluent_Case_Files
├── Results & Data
</pre>

<p><b>Author:</b></br> 
      Ansh Vishal, </br>Aerospace Engineer</br>
      <a href="anshvishal215@gmail.com">anshvishal215@gmail.com</a></br>
      <a href="https://www.linkedin.com/in/ansh-vishal/">LinkedIn</a></p>

