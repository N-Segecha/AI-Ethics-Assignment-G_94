# COMPAS Recidivism Algorithm Bias Audit
## Overview
This project conducts a comprehensive bias audit of the COMPAS recidivism risk assessment algorithm using IBM's AI Fairness 360 toolkit. The analysis focuses on racial disparities in risk scores between African-American and Caucasian defendants, following ProPublica's methodology for dataset preprocessing.

## 🎯 Purpose

To simulate or analyze an AI system with built-in **ethical auditing features** focused on fairness, transparency, and accountability across real-world decision-making.

## Key Features
*Rigorous Data Validation:* Implements ProPublica's filtering criteria with enhanced data quality checks

*Comprehensive EDA:* Demographic analysis, risk score distributions, and correlation matrices

*Fairness Metrics:* Calculates 12+ bias metrics including disparate impact, FPR/FNR differences, and average odds difference

*Mitigation Techniques:* Implements and compares multiple debiasing approaches:

*Pre-processing:* Reweighing, Disparate Impact Remover

*In-processing:* Adversarial Debiasing

*Post-processing:* Calibrated Equalized Odds

*Professional Reporting:* Generates audit report with severity rating and actionable recommendations

*Deployment Roadmap:* Provides implementation timeline for bias mitigation

---

## 🔗 Access the Notebook

👉 [Open Colab Ethical Audit Notebook](https://colab.research.google.com/drive/19U7YhY52zovQjpiWANK8JfpBJTiEKylW) 

---

# Install dependencies
pip install -r requirements.txt

### Running the Analysis
Open COMPAS_Bias_Audit.ipynb in Jupyter or Google Colab

Run all cells sequentially

Key outputs:

Visualizations (saved as PNG)

Fairness metrics comparison tables

Audit report (compas_bias_audit_report.txt)

Mitigation deployment roadmap

https://colab.research.google.com/assets/drive/19U7YhY52zovQjpiWANK8JfpBJTiEKylW.svg

## CRITICAL FINDINGS:

1. *FALSE POSITIVE RATE DISPARITY:* African-American defendants experience a 15.8% higher false positive rate compared to Caucasian defendants, meaning they are systematically more likely to be incorrectly flagged as high-risk for reoffending.

2. *PREDICTION RATE IMBALANCE:* The algorithm assigns high-risk classifications to 38.6% of African-American defendants versus 17.1% of Caucasian defendants, despite comparable actual recidivism base rates.

3. *ACCURACY VARIATIONS:* The predictive model shows inconsistent performance across racial groups, with some populations receiving systematically less reliable risk assessments than others.

## 🛠️ REMEDIATION RECOMMENDATIONS:

1. *ALGORITHMIC DEBIASING:* Implement fairness-aware machine learning techniques including adversarial debiasing, demographic parity constraints, and equalized odds optimization during model retraining.

2. *FEATURE ENGINEERING AUDIT:* Conduct thorough review and removal of features that may serve as proxies for protected characteristics, including geographic, socioeconomic, and historical factors that correlate with race.

3. *THRESHOLD CALIBRATION:* Establish group-specific decision thresholds to equalize false positive rates across racial groups, ensuring equal treatment standards.

4. *CONTINUOUS MONITORING FRAMEWORK:* Deploy automated bias detection systems with real-time monitoring, quarterly fairness audits, and transparent public reporting of algorithmic performance metrics.

5. *STAKEHOLDER GOVERNANCE:* Establish multi-stakeholder oversight committees including community representatives, legal experts, data scientists, and affected population advocates to guide algorithm development and deployment decisions.

## ⚖️ LEGAL AND ETHICAL IMPLICATIONS:
The documented bias patterns may violate constitutional equal protection principles and fair lending practices. Immediate corrective action is recommended to ensure compliance with anti-discrimination laws and maintain public trust in automated decision-making systems.

This audit underscores the urgent need for algorithmic accountability in high-stakes criminal justice applications where biased predictions can perpetuate systemic inequalities and compromise individual rights.

## 🔧 BIAS MITIGATION STRATEGIES

1. Threshold Optimization for Equalized Odds
   • Other: Optimal threshold = 10
   • African-American: Optimal threshold = 10
   • Caucasian: Optimal threshold = 10
   • Hispanic: Optimal threshold = 10
   • Native American: Optimal threshold = 10
   • Asian: Optimal threshold = 9

2. Synthetic Data Augmentation for Balance
   • Current data distribution: {'African-American': 3696, 'Caucasian': 2454, 'Hispanic': 637, 'Other': 377, 'Asian': 32, 'Native American': 18}
   • Recommendation: Augment underrepresented groups

3. Feature Bias Analysis
   • Features most correlated with race should be reviewed
   • Consider removing indirect proxies for protected attributes

## Mitigation Effectiveness:

Calibrated Equalized Odds reduced FPR disparity by 68%

Reweighing improved disparate impact ratio to 0.82

*Recommendations*
### Immediate Actions:

Implement Calibrated Equalized Odds post-processing

Remove ZIP code and neighborhood features

Establish human review for high-risk classifications

### Long-Term Strategies:

Create Algorithmic Review Board

Develop continuous bias monitoring dashboard

Establish quarterly audit process


# 📊 Analysis Summary: COMPAS BIAS AUDIT
   • Dataset size: 7214 records
   • Racial groups analyzed: 6
   • Key bias indicators calculated: FPR, FNR, Accuracy disparities
   • Visualizations generated: 4-panel bias dashboard
   • Professional audit report: Generated

🎯 Key Takeaways:
   • Significant algorithmic bias detected against African-American defendants
   • False positive rate disparities exceed acceptable thresholds
   • Immediate mitigation strategies required
   • Ongoing monitoring and governance frameworks needed

📋 Next Steps:
   1. Share audit report with stakeholders
   2. Implement recommended mitigation strategies
   3. Establish continuous monitoring systems
   4. Conduct regular bias audits (quarterly recommended)
   5. Engage with affected communities for feedback

🔗 Additional Resources:
   • AI Fairness 360 Documentation: https://aif360.mybluemix.net/
   • Fairness in Machine Learning: https://fairmlbook.org/
   • COMPAS Dataset: https://github.com/propublica/compas-analysis

License
This project is licensed under the MIT License - see LICENSE for details.