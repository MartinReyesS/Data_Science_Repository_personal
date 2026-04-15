### MiniBooNE Neutrino Identification: A Data Science Approach to Particle Physics Classification

#### Physical Context

The MiniBooNE (Mini Booster Neutrino Experiment) at Fermilab was designed to investigate neutrino oscillations, particularly the transition of muon neutrinos ($\nu_\mu$) to electron neutrinos ($\nu_e$) – a phenomenon that implies physics beyond the Standard Model. The detector records charged-current interactions where a neutrino scatters off a carbon nucleus, producing an outgoing lepton (electron or muon) and a hadronic shower. The experimental challenge is to discriminate between $\nu_e$ (signal) and $\nu_\mu$ (background) events based on the pattern of Cherenkov light recorded by photomultiplier tubes.

The dataset used in this work (UCI MiniBooNE Particle Identification) contains 130,065 simulated events, each described by 50 continuous features that represent the topological and energy distribution of the detected particles. These features are derived from the observed ring patterns and include variables such as the number of photoelectrons, the opening angles of Cherenkov rings, and the invariant mass of the hadronic system. The target variable is binary: $1$ for $\nu_e$ (signal) and $0$ for $\nu_\mu$ (background).

#### Problem Formulation

From a physical perspective, the classification problem can be stated as: given a set of detector observables $\mathbf{x} \in \mathbb{R}^{50}$, estimate the conditional probability $P(\nu_e \mid \mathbf{x})$ that the event originates from an electron neutrino. This is a supervised binary classification task complicated by:
- **Imbalanced classes**: the signal (electron neutrino) constitutes only ~30% of the events.
- **Correlated, high-dimensional features**: many variables are physically correlated (e.g., energy and ring radius).
- **Noisy and non-Gaussian distributions**: the detector response introduces fluctuations and outliers.

#### Methodology

We develop an end‑to‑end machine learning pipeline:
1. **Data cleaning**: removal of duplicates, outlier clipping (IQR factor = 3) to preserve rare but physical extreme events.
2. **Feature engineering**: Yeo–Johnson transformation for skewed features (handling negative values), creation of ratio features and interaction terms, and inclusion of principal components to capture latent correlations.
3. **Modelling**: comparison of Logistic Regression (baseline), Random Forest, and XGBoost – the latter optimised via manual cross‑validation and hyperparameter tuning (max depth, learning rate, number of trees) with class imbalance handled using `scale_pos_weight`.
4. **Interpretation**: SHAP (SHapley Additive exPlanations) values to quantify feature importance and explain individual predictions in terms of physical observables.

#### Results and Physical Interpretation

The final XGBoost model achieves a test AUC‑ROC of **0.9848**, significantly outperforming random guessing (0.5) and the baseline logistic regression (0.966). SHAP analysis suggests that features associated with topological variables can differentiate between electromagnetic (electron) and hadronic (muon) showers. The model’s decision threshold can be tuned to optimise signal efficiency versus background rejection – a crucial trade‑off in rare‑event searches.

#### Conclusion

This project demonstrates that modern machine learning techniques provide a powerful tool for neutrino identification. The work bridges my academic background in high‑energy physics with practical data science skills, forming a robust portfolio entry for roles in scientific computing, data analysis, and machine learning applied to physical sciences.

**Keywords**: MiniBooNE, neutrino oscillations, particle identification, XGBoost, SHAP, imbalanced classification, feature engineering.
