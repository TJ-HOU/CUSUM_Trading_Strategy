# CUSUM Trading Strategy
## Objective
- Use CUSUM techniques to trade securities
## Data 
- SPY,SPYV,SPYG,HSI daily adj. close from Yahoo Finance
## Walk through the code
### Part 1: EDA
- Step1: Download SPY,SPYV,SPYG,HSI daily adj. close
- Step2: Plot time series, cumulative, and kde of log-return
<img width="586" alt="image" src="https://user-images.githubusercontent.com/66891102/210094573-faedd9ce-6960-40b0-8cfa-5ea72b3f85e8.png">
<img width="578" alt="image" src="https://user-images.githubusercontent.com/66891102/210094586-7eb11d61-ef5d-41a2-89f1-38e0c64c52fb.png">

- Step3: Calculate basic statistics of log-return
<img width="594" alt="image" src="https://user-images.githubusercontent.com/66891102/210094487-41e3e77c-4ac2-4459-b8de-2676f6ab18c6.png">

### Part 2: Implement CUSUM strategy on SPY vs HSI, SPYV vs SPYG
- Step1: Set length of the rolling window, trading period, cusum threshold
- Step2: Get the today's data and the last window-length data
- Step3: Calibrate parameters of the distribution functions
- Step4: Calculate cusum statistics
- Step5: Determine positions based on cusum statistics relative to the threshold
- Step6: Calculate the cumulative return
- Step7: Plot cusum statistics and cumulative return marked with trading signals
<img width="565" alt="image" src="https://user-images.githubusercontent.com/66891102/210153301-bbc6fc37-9fb5-49ce-bca1-fe7acabdce58.png">
<img width="567" alt="image" src="https://user-images.githubusercontent.com/66891102/210153305-dc8b6862-d3f3-414d-a256-5e33765c607c.png">

- Step8: Compare results of SPY vs HSI
<img width="605" alt="image" src="https://user-images.githubusercontent.com/66891102/210153332-cbf36b3d-56cf-466f-bd02-54584ed109f2.png">

- Step9: Compare results of SPYG vs SPYV
<img width="569" alt="image" src="https://user-images.githubusercontent.com/66891102/210153333-8c479b04-97e6-4045-a711-8ad3b358af30.png">

## Output
- [Report](https://github.com/TJ-HOU/CUSUM_Trading_Strategy/blob/07862bb5ea6a0fb1129fd8f52a244ecae06ab7c1/6740_Project_Report.pdf)
