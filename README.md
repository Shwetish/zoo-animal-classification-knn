
# Zoo Animal Classification using KNN
A supervised machine learning solution utilizing the K-Nearest Neighbors (KNN) algorithm to automatically segregate and classify animal species based on physical and biological attributes.

## 1. Business Problem
### 1.1 Business Objective
A National Zoopark in India deals with the challenge of segregating and categorizing animals based on their unique physical attributes and biological characteristics. The goal is to build an automated KNN classification model that accurately categorizes animals into pre-defined classes (e.g., mammals, birds, reptiles, fish) based on distinct traits.

### 1.2 Constraints
* Categorical and boolean attributes must be properly encoded to ensure distance calculations in KNN function effectively.
* The model must handle multi-class predictions accurately without bias toward majority classes.

---

## 2. Data Dictionary
| Feature Name | Data Type | Relevance | Description / Reason for Inclusion/Exclusion |
| :--- | :--- | :--- | :--- |
| `animal_name` | String | Irrelevant | Unique string identifier for each animal; dropped prior to training to prevent overfitting. |
| `hair` | Boolean | Relevant | Presence or absence of hair/fur. |
| `feathers` | Boolean | Relevant | Presence or absence of feathers. |
| `eggs` | Boolean | Relevant | Whether the animal lays eggs. |
| `milk` | Boolean | Relevant | Whether the animal produces milk. |
| `airborne` | Boolean | Relevant | Whether the animal can fly. |
| `aquatic` | Boolean | Relevant | Whether the animal lives primarily in water. |
| `predator` | Boolean | Relevant | Whether the animal is a predator. |
| `toothed` | Boolean | Relevant | Presence of teeth. |
| `backbone` | Boolean | Relevant | Presence of a spine/backbone. |
| `breathes` | Boolean | Relevant | Whether the animal breathes with lungs/gills. |
| `venomous` | Boolean | Relevant | Whether the animal is venomous. |
| `fins` | Boolean | Relevant | Presence of fins. |
| `legs` | Integer | Relevant | Number of legs (0, 2, 4, 5, 6, 8). |
| `tail` | Boolean | Relevant | Presence of a tail. |
| `domestic` | Boolean | Relevant | Whether the animal is domesticated. |
| `catsize` | Boolean | Relevant | Relative size compared to a cat. |
| `class_type` | Integer | Target | Target variable indicating the taxonomic animal class. |

---

## 3. Exploratory Data Analysis (EDA)
* **Summary:** Inspected class imbalances across different animal types and verified attribute distributions.
* **Univariate Analysis:** Evaluated the frequency of binary traits (e.g., proportion of egg-laying vs. milk-producing animals).
* **Bivariate Analysis:** Explored correlations between physical attributes (e.g., `airborne` vs. `feathers`).

---

## 4. Data Pre-processing
* **Data Cleaning:** Ensured binary features were correctly encoded as numeric (0 and 1).
* **Feature Scaling:** Applied normalization/scaling where appropriate to balance numerical attributes like `legs` against binary indicator features.

---

## 5. Model Building & Evaluation
* **Model Training:** Built multiple KNN classifier variations using different distance metrics (Hamming distance for binary features vs. Euclidean distance).
* **Cross-Validation:** Used exhaustive cross-validation techniques to determine the optimum value of $K$.
* **Performance Comparison:** Compared accuracies, precision, and recall across training and test splits, documenting performance inferences.

---

## 6. Business Impact & Benefits
* **Operational Efficiency:** Streamlines animal inventory management, species tracking, and educational documentation for zoopark administration.
* **Data-Driven Insights:** Provides a robust framework for taxonomic classification that can easily scale to include new species records.
