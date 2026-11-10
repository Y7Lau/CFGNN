# CFGNN

This is a repo for the paper CFGNN

## abstract

Graph data analytics is increasingly used in high-stakes applications, where trustworthy decision-making requires principled uncertainty quantification. Although Conformal Prediction (CP) on Graph neural networks (GNNs) provides a remedy through statistically guaranteed uncertainty estimates, it introduces new challenges regarding conformal fairness. Conformal fairness requires achieving parity in both coverage and efficiency across different groups. Our empirical findings reveal that achieving coverage equality with existing methods can lead to efficiency inequality. Further analysis identifies biased representations of sensitive nodes and cross-group distributional inconsistencies in non-conformity scores as two important factors underlying this phenomenon. To address these challenges, we propose the Conformal Fairness Framework for GNNs (CFGNN), which couples cross-group score alignment with coverage-preserving efficiency calibration. Since message passing can cause GNNs to inherit and amplify structural biases in graph data, leading to biased node representations and inconsistent non-conformity score distributions across groups, CFGNN trains a teacher GNN on a Fair Graph constructed through counterfactual edge synthesis and transfers its structural predictive knowledge to an edgeless student through knowledge distillation, encouraging the resulting score distributions to become more closely aligned across groups. To further ensure fairness, we derive an efficiency reference from the calibrated teacher to adjust group-wise prediction-set sizes, while keeping each group’s threshold no lower than its coverage-preserving conformal quantile. Experiments on five real-world graph datasets show that CFGNN consistently achieves the smallest average prediction-set size among all compared methods while maintaining the target coverage level for each group, and reduces cross-group disparities in both coverage and efficiency.

## Example to run

    python main.py 
  

## Acknowledgments

Some of the code was forked from the following repositories:
- [APS](https://github.com/wulongfeng/EqualizedCoverage_CP/tree/main/)
- [PyGDebias](https://github.com/yushundong/PyGDebias)
- [RCP-GNN](https://github.com/CityU-T/RCP-GNN)

