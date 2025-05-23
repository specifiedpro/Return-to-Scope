# README

# Efficiency Metrics Library

This library provides demo for the working paper "Returns to Scope Estimation" by Chien Ho & Chia-Yen Lee, contriuting to diversification strategy using Free Dispoal Hull and Hypervolume based approach to evaluate the effect (positive or negative) and the extent of product mix.

## Abstract
Economies of scope refer to the cost advantages that a business achieves by producing a variety of products or services together rather than producing each one separately. The cost savings could arise because shared resources, technologies, or processes can be used across multiple products or services. Particularly, given the same inputs, returns to scope measure the change of productivity resulting from the joint production of multiple outputs compared to producing them separately. This study proposes a novel methodology combining free disposal hull (FDH) analysis with normalized hypervolume (NHV) to estimate returns to scope. Our method enables a more flexible application of hypervolume, allowing for direct consistent comparisons of returns to scope across both convex and non-convex production frontiers in multiple-output scenarios. By leveraging the area under the curve (AUC) and NHV metrics, we quantify the extent of positive or negative returns to scope with improved accuracy and consistency. Through simulation experiments, we demonstrate the capability of our proposed method to identify returns to scope on both convex and non-convex frontiers. This advancement facilitates direct comparisons of the reutrns to scope by using AUC, and provides deeper managerial insights
![threshold](https://github.com/user-attachments/assets/506a151a-be06-4332-ae19-a3da8dd56179)
![ED-S1](https://github.com/user-attachments/assets/6846ff68-3735-4128-9a22-fe3dffcbcdfb)
![Mixxx](https://github.com/user-attachments/assets/e351abaa-3e64-4b66-bbbd-c09a5a8d66ce)



## How to Use

1. Import the library functions in your Python script:
    
    ```python
    from efficiency_metrics import gen_final_data_df, label_frontier, calc_hvi_area, calc_reg
    
    df = gen_final_data_df(n_points=50, wide=[40, 60], x_pow=0.5, y_pow=2, plotting=True)
    df = label_frontier(df, x_headers=['y1'], y_headers=['y2'])
    metrics = calc_hvi_area(df, x_headers=['y1'], y_headers=['y2'])
    print(metrics)
    
    model = calc_reg(df)
    print(model.summary())
    
    ```
