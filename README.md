# BSM-IV-Estimation-with-Surface-Plot
Created as a study into Greeks for the BSM model, with 3d Plotly Graphs showing the Greeks Surfaces, options data extracted from Yahoo Finance. Since it cannot be displayed in the file, they will be uploaded here.

## Greeks Surface Plots

### IV
<img width="500" height="500" alt="iv plot 1" src="https://github.com/user-attachments/assets/59211a87-0be3-449c-9270-3952519eb88d" /><img width="500" height="500" alt="iv plot 2" src="https://github.com/user-attachments/assets/4af3e959-4226-4359-a4a2-7df7f9c862c9" />

The bump (or lack thereof) between T = 0.1 to T = 0.2 might be caused by lack of data at that point, potentially filtered out due to illiquidity. The curve becomes less steep as T increases, and the valley tends towards negative log-moneyness. This makes sense as T increases, K is discounted more and as K = S e^(-rT), hence ln(S/K) = -rT. This shows the forward-looking traders pricing in expected returns (r).

### Delta
<img width="500" height="500" alt="delta plot 1" src="https://github.com/user-attachments/assets/69d64d6c-2ca4-486c-b618-9cc917a7fdaf" /><img width="500" height="500" alt="delta plot 2" src="https://github.com/user-attachments/assets/3d998654-ef16-4bc2-9b4b-5b4dbaaae87f" />

S shape curve of Delta steepens as T -> 0, where options become either in the money or out of the money, hence payoffs become digital. The steepest parts of the curve tends towards negative log-moneyness.

### Gamma
<img width="500" height="500" alt="gamma plot1" src="https://github.com/user-attachments/assets/9a8efca8-1319-46cb-9c61-8c523962b5af" /><img width="500" height="500" alt="gamma plot2" src="https://github.com/user-attachments/assets/d8d08bdc-faf9-4022-8673-d1f2bdeb68f4" />

Gamma tends towards a spike as T -> 0. This is because as options become digital, rate of change of Delta becomes infinite at Price = Strike and at 0 log-moneyness.

### Rho
<img width="500" height="500" alt="rho plot 1" src="https://github.com/user-attachments/assets/4bd2e26e-fe50-4463-be0e-74f65b9af26a" /><img width="500" height="500" alt="rho plot 2" src="https://github.com/user-attachments/assets/903a8225-6773-4c6d-99ab-a453db38a1d7" />

Interest Rate sensitivity increases as T increases, intuitively, as cost of paying strike is discounted more. Therefore, if the option is already in the money, interest rates matter more due to payoffs being affected materially from the change in strike cost today.

### Vega
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/d78fafa1-4f0e-4b62-af66-d61d70ba4995" /><img width="500" height="500" alt="vega plot 2" src="https://github.com/user-attachments/assets/1e06ddbc-5d9a-4ddd-95bf-20b51cbb445a" />

Volatility sensitivity of option prices are highest where the option is at the money and increases as T increases. Intuitively, this is because there is a greater chance for option to change moneyness as T increases.

### Theta
<img width="500" height="500" alt="theta plot 2" src="https://github.com/user-attachments/assets/01ac5d7f-8954-495a-aed5-b35e0884b670" /><img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/32b3c905-911b-4c09-9225-b21766fc5182" />

Theta plot might look as such due to outliers and illiquid options. Theta is the time decay of options prices, and Theta becomes less negative as T increases. This is because proportion of decrease of T when T is small is much larger than when T is large, hence the time decay effect is much greater when T -> 0.
