# Seasonal-Variation-in-Diet-With-Stable-Isotopes
**Motivation**

Understanding seasonal variation in the diet of marine predators is important for interpreting ecosystem dynamics. One common approach for inferring diet and foraging behavior is stable isotope analysis, where shifts in δ¹³C and δ¹⁵N values can reflect changes in prey availability or habitat use. In this project, I ask whether stable isotope values (δ¹³C and δ¹⁵N) can be used to classify dolphins by season. Traditional analyses of isotope data often focus on statistical differences or isotopic niche overlap, commonly using the SIBER framework. However, SIBER assumes elliptical niche shapes, which may not capture more complex patterns in the data. This project explores whether seasonal groups are predictably separable in isotope space, providing a complementary perspective on how strongly dolphin foraging ecology varies over time.

**Data**

The data used in this project come from a publicly available dataset provided by the Gulf of Mexico Research Initiative (GRIIDC):
https://data.griidc.org/data/R6.x809.000:0020

This dataset includes stable carbon (δ¹³C) and nitrogen (δ¹⁵N) isotope values from bottlenose dolphin skin samples, along with associated metadata such as sampling location and time. The data were originally collected to assess potential changes in dolphin diet following the Deepwater Horizon oil spill. For this project, a subset of the dataset containing dolphin isotope values and seasonal information will be used. The data are structured in tabular format (e.g., CSV or Excel), with each row representing an individual sample and columns corresponding to isotope values and metadata.

**Model**

To classify dolphins by season, I will use a random forest classifier, an ensemble learning method that builds on decision trees. Each decision tree partitions the data by applying threshold values to δ¹³C and δ¹⁵N, and the random forest combines predictions from many trees to produce a final classification based on majority vote. By aggregating multiple trees trained on slightly different subsets of the data, random forests reduce overfitting and improve generalization compared to a single decision tree. This model is appropriate because seasonal differences in isotope values may not be separable by a simple linear boundary, and random forests can capture more complex, nonlinear patterns in the data. Rather than optimizing a single global loss function, the model is constructed by selecting splits that improve class separation (e.g., reducing impurity) at each step, making it well-suited for classification tasks.
