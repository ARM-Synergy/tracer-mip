# Tracking Aerosol Convection Interaction Experiment (TRACER) Model Intercomparison Project (MIP) Roadmap


## 1. Introduction
The DOE ARM [Tracking Aerosol Convection Interaction Experiment (TRACER) campaign](https://www.arm.gov/research/campaigns/amf2021tracer) took place in the Houston, TX region from 01 October 2021 through 30 September 2022, with an IOP from June-September 2022, which collected a comprehensive data set focused on the evolution of convective clouds and their environment (including aerosol, cloud, thermodynamics, and lightning). A unique component of TRACER is that a large number of individual, isolated convective cells will be tracked and measured with high spatial and temporal resolution. These comprehensive, unique observational datasets can help evaluate model and parameterization performance, identify model and parameterization deficiencies, and gain new insights to improve models. This provides the motivation for conducting an additional community model intercomparison project (MIP) based on the previous Aerosol Cloud Precipitation Climate (ACPC) Deep Convective Cloud (DCC) MIP (ACPC-MIP; van den Heever et al. 2017; Marinescu et al. 2021; Saleeby et al. 2025; van den Heever et al. 2025), which is referred to as the TRACER-MIP.


## 2. Goals and Hypotheses of the TRACER-MIP

### Goals:
1. Quantify the inter-model spread in representation of aerosol-convection interactions (ACI), identify model deficiencies, and measure model performance.
2. Examine factors/processes leading to the model biases and large model spread, both of which were less emphasized in the previous ACPC-MIP. This effort will ultimately help reduce the ACI uncertainty. 

### Hypotheses:
1. The different representations of condensation and ice microphysics are a major source of  inter-model spread, thus, leading to the main model differences in the simulation of ACI.
2. The models that reproduce the observed cases and employ explicit calculation of condensation give qualitatively consistent ACI effects, particularly for the effect of ultrafine particles.


## 3. Approach and Cases
The TRACER-MIP follows and builds upon the ACPC-MIP. The ACPC-MIP roadmap document can be found at this [link](http://acpcinitiative.org/Docs/ACPC_DCC_Roadmap_171019.pdf). The TRACER-MIP has the following new features:

* Extensive model evaluation against observations. 
* Two golden cases with varying dynamic, thermodynamic, and aerosol conditions. Ultrafine aerosol will be considered. Two tiers: prescribed and prognostic aerosols.
* More detailed focus on factors/processes leading to model biases and large model spread.

Two cases were chosen to simulate from among several 'Golden' TRACER cases, which are June 17 and August 7, 2022 (Figures 1 and 2). Cases below were chosen since they met the following criteria:

* Data available - SMPS aerosols (with ultrafine aerosols measured), soundings (5 per day), NEXRAD CAPPI, C-SAPR cell tracking.
* Seabreeze present, convection observed, and cells tracked.

![TRACER MIP Figure 1](figures/TRACER_MIP_Fig1.jpeg)
***Figure 1. The soundings (left), Stage IV precipitation (middle), and the pre-convective aerosol size distribution (right) measured at the TRACER main site by SMPS for the June 17 case.***

The June 17 case has widespread convection, featured with an afternoon sea breeze induced thunderstorm in the Houston area (Figure 1) with a high aerosol condition (~ 4000 cm<sup>-3</sup>; > 10 nm). This case has aircraft measurements from the co-current NSF ESCAPE field campaign. The August 7 case has a morning sea breeze front and a thunderstorm in the early afternoon in the Houston area with relatively cleaner aerosol conditions (~1700 cm<sup>-3</sup>; > 10 nm).

![TRACER MIP Figure 2](figures/TRACER_MIP_Fig2.jpeg)
***Figure 2: The soundings (left), Stage IV precipitation (middle), and the pre-convection aerosol size distribution (right) measured at the TRACER main site by SMPS for the August 17 case.***


A [TRACER-MIP GitHub page](https://github.com/ARM-Synergy/tracer-mip) has been established for sharing this roadmap document as well as other documentation and updates, analysis codes, model & parameterization descriptions, etc.


## 4. Simulations Summary
For each case described above, we are requesting three simulations:
* Control simulation using the pre-convective aerosol profiles with the 2 aerosol modes. (See the dual modes represented in the right panels of Figures 1 & 2.)
* Same as control but with aerosol number concentration of each mode **3x higher**.
* Same as control but with aerosol number concentration of each mode **3x lower (i.e., multiple by a coefficient of 0.3)**.

Details of the simulation design and initialization are provided in the sections that follow.


## 5. Model Setup
We ask all participants to use the following model configuration given in the table below. The nested grid domains are shown below in Figure 3. The inner domain Grid-2 is the same as the innermost nest from the ACPC-MIP. Table 1 presents model setup details. For each of the aerosol sensitivity simulations discussed below, to avoid the complications from size distribution change, we ask to keep the shape of the aerosol size distributions identical. We will solely change the initial aerosol number concentration vertical profiles by multiplying the observed surface number concentration by the coefficients (3x and ⅓ x) and generating the associated initialization vertical profiles for the sensitivity simulations. This means we are exploring the effect of aerosol number changes on clouds only. We also ask that all participants provide a file that contains a description of their model, descriptions of the parameterizations (i.e., microphysics, turbulence, land surface, etc.) used with associated references, and an overview of the output variable names and units. The table of requested output variables and units is provided in Table 2 . Please conform to this request of variables and units as much as possible.

<<<<< Fig-3

<<<<< Table-1


## 6. Output of Model Variables
Table 2 describes the necessary model variables to output and the associated units. If your model writes all variables for each grid and time to an individual file, then please provide the full output files (one file per grid per time for each grid). Please also provide a separate document that outlines (1) assumptions and parameters used to define the hydrometeor and aerosol size distributions and the aerosol Tier option, (2) mass-diameter relationships and fall speed equations for each hydrometeor class (or equivalent for your model), and (3) ice category properties. Please note the details regarding the output diagnostic microphysical process rates and their units. For models to participate in the process rate analysis, these rates need to be provided in the requested units.

<<<<< Table-2


## 7. Data Submission and Timeline
Data storage will be provided by the DOE, and we are in the process of establishing this storage space and granting user access. Detailed  information about data submission will be provided to the participants. Please let Steve Saleeby (Stephen.Saleeby@colostate.edu) and Jiwen Fan (fanj@anl.gov) know if you want to participate so that you can receive further guidance from us about this MIP.

***Timeline:*** We plan to show some preliminary results in the next ACPC workshop (May 2025). For teams that wish to have their model results included in a TRACER-MIP preliminary presentation at the ACPC meeting, we need to receive data submissions by February 1, 2025. The final deadline for submitting TRACER-MIP model results is July 1, 2025.


## 8. Aerosol Initialization
The aerosol initial conditions for each case have been constructed via a combination of (1) the surface aerosol particle size distributions from the SMPS at the TRACER AMF1 site in LaPorte, TX (courtesy of Tamanna Subba and Chongai Kuang from BNL) and (2) the aerosol vertical shape profile derived from coincident micropulse lidar and radiosonde data that are used to compute the cloud-free aerosol backscatter coefficient profile (courtesy of Bo Chen, Anita Rapp, & Sarah Brooks from Texas A&M Univ). For details, please refer to Chen et al. (2024). The 2-mode aerosol size distribution is shown in Table 3 and Figure 4 with an ultrafine aerosol mode peaking at 30 nm (June 17) and 50 nm (Aug. 7) in diameter, and an accumulation mode peaking at 135 nm (June 17) and 175 nm (Aug. 7). Aerosol mode characteristics for each case are shown in Appendices A & B and summarized in Table 3.

<<<<< Table-3

The aerosol number concentrations were originally provided in volume units of cm<sup>-3</sup>. To apply this to models that carry aerosols in number and mass units of kg<sup>-1</sup> and kg kg<sup>-1</sup>, we convert the volume units to mixing ratio units using a representative surface air density (1.159 kg m<sup>-3</sup>) near the AMF1 site. 

The left panel of Figure 4, below, shows the idealized vertical profile of normalized aerosol concentration derived from the Chen et al. (2024) methodology above using the TRACER observations from 1200-1400 LT on 7 Aug 2022 (data for this type of analysis were not available on 17 June, so we use this profile as being reasonably representative of the Houston area during the IOP). The middle and right panels display the respective applied profiles to be used in the control simulations for the two aerosol modes identified from the pre-convective time periods on 17 June and 7 August.

<<<<< Fig-4

The shape profile in the left panel above is represented by the following function fit to the dry aerosol backscatter (and then scaled from 0 to 1):

<<<<< Equation-1

The aerosol surface concentrations in # mg<sup>-1</sup> were then applied to the idealized vertical shape profile (Figure 4, left) to arrive at the case study control simulation shape profiles in Figure 4 (center, right). The vertical profiles apply an additional constraint such that the total (mode-1 + mode-2) number concentration does not drop below 50 mg<sup>-1</sup> at any altitude and scales with the surface aerosol number concentrations. Details of this application can be found in the Jupyter notebook linked below.

The link to the Jupyter notebook with aerosol number concentration control simulation vertical profiles is found at: [Pyplt.TRACER_Aerosol_Profiles_MIP.ipynb](https://drive.google.com/file/d/1Oz7Eb3TLnWkH3N1gY0FXUnQYWSKc_N3J/view?usp=drive_link). It is used for plotting the initial aerosol vertical profiles and for viewing the precise aerosol concentration at each vertical level for each aerosol mode. This code can be readily adapted to individual MIP model coding language (e.g., Fortran) for initializing aerosol profiles. Aerosol profiles are to be initialized horizontally, homogeneously across the domains of both grid nests.

Initialization of aerosol vertical profiles for the **3 x higher** and **3 x lower** sensitivity simulations simply requires **3 x** or **⅓ x** of the provided surface aerosol concentrations (# cm<sup>-3</sup>) of each mode, conversion to mixing ratio units based on provided air density (# mg<sup>-1</sup>), and then re-creation of the vertical profiles based on those updated numbers.

If your model can represent the aerosol distribution **mode sigma**, please use the sigma values provided in the table; otherwise use your model’s default values.

For models that can represent **aerosol hygroscopicity**, we are using a single and constant bulk **kappa value of 0.26** (Figure 5) which corresponds to the full TRACER campaign 50th percentile value of the bulk kappa derived from the AMF1 Aerosol Observing System (AOS) at LaPorte, TX (courtesy of Maria Zawadowicz, BNL).

<<<<< Fig-5


## Appendix A: Additional summary of June 17, 2022 case study event  

* Seabreeze convection and large-scale convection scattered over the Houston area domain. 
* Overlaps with ESCAPE (aircraft & ground operations).
* Mostly clean marine aerosols.
* SMPS data collected. ACSM data not collected.
* NU-WRF realtime modeling skill score: 71

The figures that follow provide information for the July 17 event including daily soundings (Fig. A.1), observed precipitation (Fig. A.2), GOES GeoColor imagery 2-hourly (Fig A.3), NEXRAD composite reflectivity 2-hourly (Fig. A.4), cell distribution from NEXRAD data using MCIT cell tracking (Fig. A.5), and SMPS aerosol conditions for the day and for model initial surface aerosol concentration (Fig A.6).

<<<<< Figs-A1, A2, A3, A4, A5, A6


## Appendix B: Additional summary of August 7, 2022 case study event

* Early sea-breeze, consistent onshore flow. Isolated convection day.
* Moist throughout the column.
* CHIVO Radar available and TAMU Observations available.
*  Polluted aerosols early, clean marine after sea-breeze.
*  SMPS & ACSM data were collected.
*  NU-WRF realtime modeling skill score: 70

The figures that follow provide information for the July 17 event including daily soundings (Fig. B.1), observed precipitation (Fig. B.2), GOES GeoColor imagery 2-hourly (Fig B.3), NEXRAD composite reflectivity 2-hourly (Fig. B.4), cell distribution from NEXRAD data using MCIT cell tracking (Fig. B.5), and SMPS aerosol conditions for the day and for model initial surface aerosol concentration (Fig B.6).

<<<<< Figs-B1, B2, B3, B4, B5, B6


