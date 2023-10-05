 
Diversity in Statistics:
========================
The script is intended for use on Linux systems and can assist in various statistical analyses related to diversity.


About:
----------
Diversity analysis is a critical component in various fields of the sciences. 
The script aims to simplify diversity analysis tasks by providing tools to calculate diversity statistics, visualize data, and perform K-Means clustering.

1. Statistics of diversity

The averages and standard deviations of the diversity scores of each animal in `clinical_data.txt` are calculated from `{animal}.diversity.txt`.
The animals with the two highest average diversity scores and the animal with the lowest average diversity score are selected for further analysis.

2. Distance plot visualization

Scatter plots of the distance coordinates from the respective `{animal}.distance.txt` files in the `distanceFiles` directory are plotted and saved to `{animal}.pdf`.

3. K-Means clustering
	
The Elbow Method determines the optimal number of clusters (k) for K-Means clustering by identifying the point where the rate of distortion reduction changes significantly. The Elbow method analysis graphs are saved as `{animal}_elbow.pdf`.

K-Means cluster analysis is performed on the three selected animals to visualize clusters. Clusters and centroids are plotted and saved as `{animal}_k.pdf`. 


Execution in Ubuntu/Linux:
--------------------------
1. Replace `{user}` with your actual username and verify paths based on your directory structure.

2. Ensure that the following files are located in the correct directory.

	The `diversity.py` script should be located in the working directory

	The `{animal}.distance.txt` files are in the `/inputfiles/distanceFiles` directory

	The `{animal}.diversity.txt` files are in the `/inputfiles/diversityScores` directory
	
	The `clinical_data.txt` is located in the `/inputfiles` directory
	
3. Install dependencies

pip install scikit-learn

4. Open a terminal and navigate to the working directory

5. Provide executable permissions to the script:

chmod +x diversity.py

6. Execute the script with the following command:  
 
python3 diversity.py

7. The following output files are created:

	`{animal}.pdf` contains the scatter plot image with distance data plotted

	`{animal}_k.pdf` contains the K-Means clustering plot of the distance data

	`{animal}_elbow.pdf` contains the graph of the Elbow Method analysis of the distance data

	`clinical_data.stats.txt` contains data from `clinical_data.txt`, as well as averages and standard deviations of the diversity scores for each animal
