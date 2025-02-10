# README

# Efficiency Metrics Library

This library provides functions to simulate DMU data and calculate efficiency metrics such as MRTS, AUC, HVI, and perform regression analysis.

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