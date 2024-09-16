# MarketRose

Library building suite of methods-tools to guide pricing decisions based on legal principles that are legislated to redesign digital markets.

## App Stores - One time fee

### **Context**

App suppliers make the following claim

`In order to fairly implement a one time acquisition fee, we suggest that Apple and Google be allowed to charge this fee when the user downloads an app via their app store and makes a purchase within a 7-day window of the install; subject to two exceptions: (i) when the user has typed the trademark of the app developer in the app store search box and (ii) when the app developer has bought search ads. In the former case, the app developer brought the user to the app store and in the latter case the app developer has already paid fees for acquisition.'

### **Remarks**

Suppliers make reference to fairness based on causality. They propose to identify the causal effect of the platform (respectively, the suppliers) based on three types of behaviors: attribution window, user behavior, app behavior. 

### **Objectives**

We build a prototype tool to assist regulator to set app store price that is charged to 3P developers. By assist we mean two functions a. positively we encode fairness into a dataset of Apple purchases. b. normatively we use this encoding to provide optimal price \(with respect to fairness, efficiency)\. 

### **Code**

1. Builds a synthetic dataset of App Store purchases. 
2. Constructs a model encoding one notion of fairness \(Geradin, 2024\). By encode we mean 'build an attribution model determining payouts to DP and Developers.' 
3. Constructs a model encoding alternative, specific versions of fairness. We consider concrete alternatives \(parties, DMA\).  
4. Constructs Pareto Frontier between fairness (2., 3.) and efficiency.  

### **Additional Remarks**

- This model relies on a simulated dataset of individual level app store purchases, dates, and search advertisements. The data could comprise a snapshot of any two week period. 
- This model excludes relevant data protections, for example privacy scores. 
- This model enables visualization of the Pareto frontier via R/Shiny. 
