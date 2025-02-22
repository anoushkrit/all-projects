# all-projects
A list with description and images of all the projects that I have worked on


| Project | Description | Result | Stack | 
|---------|-------------|--------|-------|
| [SlicerTracto](https://github.com/anoushkrit/SlicerTracto)     _Dec 2024 - Ongoing_| SlicerTracto is an open-source Slicer 3D extension tool which enables Neuro-Radiologists to visualize, localize, track and segment white matter tracts from Diffusion MRI scans all-in-one stand-alone desktop application. | SlicerTracto runs smoothly as a local extension over Slicer on all devices, Mac, Windows and Linux. Compute can also be transferred to servers.| python, 3DSlicer, dipy, scilpy, pytorch | 
| [Talk2point](https://github.com/anoushkrit/talk2point)    _Feb - May 2024_| Modification in Tokenization of Changeit3D, on ShapeTalk dataset to make editing and generation more granular and region specific.| Using ShapeTalk dataset, we modified ChangeIt3D to learn more granular patch embeddings for text based point cloud reconstruction. SDFusion to reconstruct point clouds from scratch. | python, pytorch, open3d |
| [TrackletGPT](https://github.com/anoushkrit/TrackletGPT)     _Jan 2025 - Ongoing_ | An upgrade on TractoGPT, where we are modifying the point cloud token. Here token resembles a bspline which is a part of streamline. | Results on how it performs are still pending.| python, open3d, pytorch3d, pytorch, plotly, fury.gl | 
| [Sculpt3D](https://github.com/anoushkrit/Sculpt3D)     _Jan 2025 - Ongoing_ | Text to 3D point cloud generation model which uses multimodal input to create 3D point clouds. Using SDFusion for generating through text, sketches, and image. We add the capability of "editing" along with one-time generation, using textual prompts as continuous feedback for editing point clouds. | The project is currently ongoing and we have satisfactory results from the exisiting implementation of SDFusion. We are currently adding LLM editing capabilities. |python, open3d, pytorch3d, pytorch, plotly, fury.gl, LLaMA, GPT | 
| [TractoGPT](https://github.com/anoushkrit/TractoGPT)     _July - Nov 2024_| TractoGPT models Tractography streamlines (3D point sequences) as 3D point clouds where we create patches of point clouds from a bigger point cloud. Patches are encoded as tokens to pretrain GPT on point cloud reconstruction task using dual-masking, which can further fine-tuned for downstream tasks like classification, segmentation etc.| Outperformed Sherbrooke Connectivity Imaging Lab, University of Sherbrooke, Canada(SCIL)'s work, FIESTA. Published in International Symposium on Biomedical Imaging.        https://arxiv.org/abs/2501.15464 | python, open3d, pytorch3d, pytorch, plotly, fury.gl, GPT | 
| [TractoEmbed](https://github.com/anoushkrit/TractoEmbed)    _April - 8 July 2024_ | "From point cloud representation of Tractography Streamlines we learn and extract multiple embeddings from 3 different data representations, self, regional and whole using a CNN, dVAE and PointNet respectively to classify into white matter anatomical tracts." | Outperformed Harvard Medical School’s work on Tract Segmentation, i.e. TractCloud. Published paper in International Conference on Pattern Recognition.       https://link.springer.com/chapter/10.1007/978-3-031-78104-9_17  | python, open3d, pytorch3d, pytorch, plotly, fury.gl |
| TractRL-former _Jan - 17 April 2025_| Tract-RLFormer, a network utilizing both supervised and reinforcement learning, in a two-stage policy refinement process that markedly improves the accuracy and generalizability across various data-sets. By employing a tract-specific approach, our network directly delineates the tracts of interest, bypassing the traditional segmentation process. | Outperformed White Matter Tracking Algorithms from SCIL (Sherbrooke Connectivity Imaging Lab) i.e. Track2Learn and other algos like DeepTract, PFT (Particle Filtering Tracking).         https://link.springer.com/chapter/10.1007/978-3-031-78201-5_17| openai-gym, pytorch, scilpy, python |
| [MedIntel](https://github.com/satyam-kr03/MedIntel)       _Feb - May 2024_ | MedIntel is a chat bot finetuned to perform differential diagnosis using DDx-plus dataset by fine-tuning MedLLaVA (by Microsoft) and med-llama. These pre-trained models were fine-tuned on publicly-available MedQA and MedMCQA dataset. | MedIntel performs some differential diagnosis, i.e. across 49 common pathologies, with 110 symptoms listed in DDX plus dataset. Model was deployed on PARA M Himalaya (Super Computer at IIT Mandi) and inferred on basic Chat GUI using Streamlit. | python, ollama, huggingface, pytorch, peft, streamlit | 
| [VikramUnity](https://github.com/anoushkrit/Chandrayaan)     _Sep - Nov 2023_ | A Unity-based Chandrayaan Rover, Vikram, simulation on the dark side of the moon. Where the Rover is tasked with reaching checkpoints in daytime on moon-surface. Reward policy of the agent incentivizes realtively planar surface of movement, avoiding craters, working in the daytime, planning the task ahead. We used a PPO Reinforcement Learning agent for the Unity ML Agent | Rover was able to reach to the target avoiding obstacles, and in daytime. Suicidal (or resetting the environment) tendencies of the model decreased and it was able to control momentum as it touched the target. | unity-ml, unity, RL, ml-agents, C# |  
| [TractoAware](https://github.com/anoushkrit/TractoAware)     _Oct 2023 - Feb 2024_ | With point clouds as having having only (x,y,z) point information, we add information per point including normals, gradients, theta angle from the starting point of the streamline. With this we pass multiple features to point cloud networks to classify White Matter Tracts | Witnessed 15% jump in classification and segmentation accuracy. Proves that multi-dimensional point cloud data can be processed by Point Cloud Models. Learnable embedding or multi-dimensional features can be more useful, see TractoEmbed.| python, open3d, pytorch3d, pytorch, plotly, fury.gl |
| [ClickVision](https://github.com/anoushkrit/ClickVision)      _June 2021 - June 2022_ |Inspired from MDP (Markov Decision Process) Model, we formulated the solution using transition matrices on clickstream data, where trajectories (sequence of clicks) leading up to the event gets more weightage, and importance of other actions/trajectories/nodes decay over iterations. A score is assigned to each trajectory based on its weight, discount factor and transition probabilities. With this we predict future actions of the user and calculate depositing score and give the verdict. | Reduced wrong incentives given to non-depositing users by approximately 60% as seen on MoEngage. Event "Deposit" prediction time was less than 2 mins of usage on the platform. ClickVision is internally deployed on Gamezop.com to know | clickstream data, pyspark, python, markov chains, pandas |
| [pyCardiograms](https://github.com/Teresa-Tensr/pycardiogram)      _Mar - June 2020_ | Waveform Analysis, Wave Annotation and Inter-wave correlation across ECG and SCG on PhysioBank Dataset. Prediction of SCG waveform for 2 heartbeat cycles using Bidirectional-LSTM on cardiac signals datasets | Annotated SCG waveforms with peak values, using MATLAB and scipy. Extracted correlations among SCG and ECG to understand how rich SCG signals were to ECG signals. | scipy, 
| Teresa Band     _Jan 2020 - June 2021_ | "Teresa Band, a novel Cardiovascular Triaging Wearable Device, for detecting vascular and valvular cardiac conditions (like Arteriosclerosis, Turbulent Blood Flow) early, using mechanical vibrations of the heart, SCG (SeismoCardiogram), of the patient." | "Able to get multiple biomarkers, ECG, SCG, and PPG signals from the body. Without battery, and as a wired connection the device worked on the phone connected though an aux cable and a DC supply to the Arduino Portenta chipset. "| python, scipy, pytorch, wfdb | 
| TableOCR     _Oct - Dec 2019_ | TableOCR is for doing OCR on loosely Tabular Data, which is analogous to documents like menus, bills,invoices etc where there is implicit tabular information but lacks grid lines. For OCR, we used Tesseract and Cloud Vision API, and we match neighbouring bounding boxes on the basis of geometrical heuristics | TableOCR faced certain limitations in correlating multi-columnar data as a single row data to the excel sheet. Output of the model consisted of a json with bounding box coordinates, text inside the box, and spatial relationship of the bounding box with other boxes. This relationship was exploited to map boxes with each other. |
| [CADtnet](https://github.com/anoushkrit/CADt-net)     _Jan - Oct 2019_ | CADtnet is an edge DL app, for triaging Breast Ultrasound Scans based BI-RADS (Breast Imaging Reporting and Data System) scores which ranges from 0-6, where at a score of 3 app alerts the healthcare provider of suspected lesion with a bounding box surrounding the lesion. This app takes phone camera photos of Ultrasound Scans as input and is deployed in LMICs, and was tested in Guadalajara, Mexico. | CADt-net was deployed at the client (Dr. Susan Love Foundation) side in the form of an Android App (CADx) using TF-lite and mobile-net v2. The app deployed in Guadalajara, Mexico successfully classified Ultrasound scans into BI-RADS scores.| python, tf-lite, keras, pytorch, imgaug, edge-ai| 
