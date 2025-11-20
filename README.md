# PROTEIN-LIGAND-DOCKING-6Y3C-Human-COX-1-Crystal-Structure-
PROTEIN LIGAND DOCKING 6Y3C = Human COX-1 Crystal Structure 
Protein-Ligand Docking: Fluconazole Inhibition of Cyclooxygenase-2 (COX-2) 💊💻

Overview

This repository contains the input, configuration, and result files for a Protein-Ligand Docking simulation performed using AutoDock Vina. The objective was to predict the most stable binding pose and quantify the binding affinity of the small molecule Fluconazole (FLC) within the active site of the enzyme Cyclooxygenase-2 (COX-2).

The protein structure is referenced from the PDB entry 6Y3C. This simulation provides computational insight into the potential inhibitory action of Fluconazole against COX-2, an enzyme involved in inflammation.

Target System Details

Component	Identifier	Description
Protein Target (Receptor)	COX-2 (PDB ID: 6Y3C)	Cyclooxygenase-2, the target enzyme.
Ligand (Inhibitor)	FLC (Fluconazole)	The small molecule drug being docked.
Software Used	AutoDock Vina (or similar suite)	Tool used for predicting binding geometry and scoring.
Simulation Goal	Predict the binding pose and affinity of FLC to COX-2.	

Simulation Results and Configuration

1. Best Binding Affinity

The simulation successfully predicted multiple binding modes. The top predicted affinity score, indicating the predicted strength of the interaction, is:
Mode	Affinity (kcal/mol)
1 (Best Pose)	-5.2

A lower (more negative) binding affinity score suggests a more energetically favorable and stable binding interaction.

2. Docking Grid Parameters

The search space for the docking run was defined by the coordinates and dimensions in the config.txt file, encompassing the binding pocket:
Parameter	Value (Angstroms)
center_x	-32.960
center_y	-51.042
center_z	-5.625
size_x	126
size_y	126
size_z	126

Repository Files

File Name	Description	Category
Cox_Prot.pdb	Prepared PDB structure of the COX-2 receptor protein.	Input
Cox_Prot.pdbqt	Receptor file prepared for AutoDock Vina (includes charges and atom types).	Input
FLC.pdb	Original PDB structure of the Fluconazole ligand.	Input
Lig.pdbqt	Ligand file prepared for AutoDock Vina.	Input
config.txt / config	Configuration file specifying the grid box coordinates and input/output names.	Config
log.txt	AutoDock Vina log file, detailing the execution summary and affinity scores table.	Output/Log
out.pdbqt	Docking results file containing all predicted poses and their scores.	Output
output.txt	Raw console output from the docking process (may contain system information).	Output/Log
6y3c.cif	Crystallographic Information File (CIF) for the reference PDB structure.	Context

Setup and Visualization

To visualize the predicted protein-ligand complex and analyze the molecular interactions:

    Dependencies: Install a molecular visualization tool such as PyMOL or ChimeraX.

    Load Structures:

        Load the prepared receptor structure: Cox_Prot.pdb.

        Load the docking result file: out.pdbqt. (The viewer will display all binding poses; focus on Mode 1.)

    Analysis: Inspect the best pose from out.pdbqt to identify key molecular interactions (e.g., hydrogen bonds, hydrophobic contacts) between Fluconazole and the residues within the COX-2 active site.
