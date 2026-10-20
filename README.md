### BBBC018 · Cytoskeleton and Cell Morphology Lab
Student ID: BBBC018_largespread_13362
Course Context: Karp, Chapter 9 — The Cytoskeleton and Cell Motility
Tools: Fiji/ImageJ, R, Posit Cloud, GitHub
Dataset: Broad Bioimage Benchmark Collection (BBBC018) — HT29 Human Colon Cancer Cells
### 1. Image Selection and Registration
I reviewed the 14 morphological phenotype categories in the BBBC018 dataset and selected the Large spread phenotype for analysis. After downloading and extracting the image archive, I opened the corresponding F-actin and DNA channels in Fiji.
I selected image field 13362 (13362-actin.DIB and 13362-DNA.DIB) because its cellular morphology appeared consistent with the Large spread reference phenotype. I then registered the image field in the class spreadsheet and verified that it had not been selected by another student.
### 2. Image Import and Preparation in Fiji
I imported both image channels into Fiji to examine the F-actin cytoskeleton and nuclear staining. After inspecting the field, I selected five intact, distinguishable cells that did not overlap or touch the image borders for morphological measurement.
### 3. Morphological Measurements in Fiji
I configured the measurement settings to record area, mean gray value, shape descriptors, and ROI labels. Using the Freehand Selection tool, I traced each cell boundary in the actin channel and used the DNA channel as a reference when needed. I saved the five ROIs in the ROI Manager and measured them using Fiji's measurement function.
The measurements included:
Area: The size of the traced cell region in pixels².
Mean gray value: The average fluorescence intensity within the traced region, expressed in arbitrary image units.
Circularity: A measure of cell roundness, ranging from 0 to 1, with values closer to 1 indicating a more circular shape.
Aspect ratio: The ratio of the major axis to the minor axis, with higher values indicating greater elongation.
I exported the measurements to data/fiji_results.csv and saved an annotated image of the selected cells as figures/measured_cells.png.
### 4. Data Analysis in R
I organized the project into data/, scripts/, results/, and figures/. I saved the Fiji measurements in the data/ folder and prepared scripts/analyze_cells.R for analysis in R through Posit Cloud.
I configured the script with the selected phenotype (Large spread) and image field ID (13362), then ran the analysis to generate summary statistics and visualization plots. The outputs were organized in the appropriate project folders for documentation and reproducibility.
### Answers to the questions 
Q1. What phenotype did you choose, and what image field ID did you register?
I selected the Large spread phenotype and registered image field 13362, using 13362-actin.DIB as the primary image.
Q2. Why did you choose this field, and how does the actin staining compare with the reference phenotype?
I chose field 13362 because the cells appeared flattened, with broadly extended F-actin structures consistent with the Large spread reference phenotype.
Q3. Why is it important not to compare raw mean fluorescence intensity directly across different image fields?
Raw fluorescence intensity can vary with exposure settings, detector gain, illumination, and staining conditions. Therefore, differences in intensity may reflect technical variation rather than actual differences in protein abundance.
Q4. What do the morphological measurements tell you about the selected cells?
Area, circularity, and aspect ratio describe cell size and shape, while mean gray value measures average fluorescence intensity. Together, these parameters help characterize cellular morphology and F-actin staining in the selected cells.
