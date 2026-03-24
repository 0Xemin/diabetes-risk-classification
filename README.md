TEAM LEADER INTERIM REPORT 
Delivery Week: Weeks 1 & 2 Project Name: Diabetes Risk Classification System based on Blood Glucose and BMI 
Team Leader: Muhammed Emin Kardaş 
Delivery Date: 24.03.2026


1. Team Composition and Management Policy :
Our project team consists of five members: Muhammed Emin Kardaş, Mahmut Berhak Tanyıldızı, Şevval Kaya, Umut Ceylan, and Fırat Can Yıldırım. In strict adherence to the Scrum Project Management model, the role of Scrum Master (Team Leader) is performed on a rotating basis every two weeks. This ensures that each member gains leadership experience and takes full responsibility for the reporting and coordination of their respective sprint. As the first Scrum Master, I am responsible for the initial setup, data integration, and the establishment of the technical foundation for the first two weeks.

2. Weekly Goals and Status:
In this initial sprint, we focused on building a rock-solid foundation for our 700,000-row clinical dataset. As the Scrum Master for this rotation, my primary goal was to ensure data integrity and establish the preprocessing pipeline before moving to the modeling phase.

Dataset Acquisition & Validation: We successfully integrated a large-scale diabetes dataset consisting of 700,000 records and 26 features. This ensures our model will have enough "statistical fuel" to minimize overfitting, fulfilling the project's requirement for a non-trivial data volume.

Exploratory Data Analysis (EDA): We implemented a modular analysis system to understand the distribution of categorical variables like Gender, Ethnicity, and Socio-economic status . This step was crucial to confirm that our data is balanced and representative of diverse populations .

Advanced Feature Engineering: Rather than relying solely on raw data, we engineered three new clinical indicators to improve model sensitivity: Pulse Pressure, Cholesterol Ratio, and Age-BMI Interaction . These features are designed to capture complex physiological relationships that individual metrics might miss .

Preprocessing & Encoding Pipeline: We established a automated ColumnTransformer to handle different data types . This includes One-Hot Encoding for nominal categories and Ordinal Encoding for ranked features (like Education and Income), ensuring the machine learning models can interpret the data correctly while preserving its inherent logic .

Collaborative Infrastructure: The team has been successfully onboarded to a centralized GitHub repository, enabling version-controlled development and transparent progress tracking for all five members.

3. Technical Works Conducted:
The primary technical focus of this sprint was the stabilization of the data pipeline and initial feature engineering. We conducted a comprehensive analysis of the dataset, which contains 700,000 entries and 26 clinical features. To enhance the predictive power of the models, we derived several clinical indicators: Pulse Pressure ($Pulse Pressure = Systolic\_bp - Diastolic\_bp$), Cholesterol Ratio ($ldl / hdl$), and Age-BMI Interaction . Furthermore, a categorical encoding strategy was implemented using ColumnTransformer, applying One-Hot Encoding for nominal variables and Ordinal Encoding for hierarchical data such as education and income levels .

4. Problems Encountered and Solutions:
We encountered a technical TypeError during the visualization phase, where the plt.title function became non-callable due to a namespace conflict. The issue was resolved by identifying the improper string assignment and resetting the Python runtime environment. To facilitate simultaneous collaboration among five members, we established a GitHub repository, enabling version-controlled development and progress tracking.

5. Team Leader’s Comments:
The project has successfully completed its first sprint with high team motivation and strict adherence to Scrum principles. The rotation of the Scrum Master role will ensure continuous engagement and shared responsibility. The technical infrastructure is now fully prepared for the upcoming model training phase, with all categorical and numerical data properly preprocessed and versioned on GitHub.
