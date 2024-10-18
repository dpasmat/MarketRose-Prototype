# MarketRose

In this note we describe two methods to guide pricing decisions based on legal principles that are legislated to redesign features of the market for mobile app stores.

## App Stores - Access Fee

### **Context**

The current-emerging dispute between Apple and EC relates closely to the fee structure the former can apply to 3P apps. The EC lays out two principles to regulate this group of decisions (fairness, contestability). Considering contestability, the EC may object to Apple’s new fee structure if it determines that this structure limits entry and expansion of alternative app stores.

### **Problem**

_Contestability_ As noted by Padilla (2024), it is unlikely as a practical matter that the EC will induce Apple to change decisions sufficiently to create meaningful entry by alternative app stores in the near future. For this reason it is unlikely that the regulator’s decisions based on the principle of contestability will render moot its decisions based on the principle of fairness.

_Fairness_ For this reason, in some instances gov-regulator must be prepared to effectively regulate prices and to do this it relies on the principle of fairness. Anticipating this problem, recent commentators provide a definition of fairness and argue it consistent with any discussion of the term as written in the DMA.

Padilla (2024) agrees that the EC may need to regulate Access Fees. To begin exploring how to do this he follows traditional competition economics by appealing to counterfactuals. To flesh this out he suggests reviewing business plans or perhaps using surveys to ask users how important certain characteristics of the platform are. 

### **Remarks**

These methods are unsatisfactory as a basis to explore FRAND app store fees. The monopoly on app stores makes it meaningless to ask users about attributes. In any case, the value that the platform provides is not limited to a few attributes or characteristics. We need a method to determine how to separate the value of the platform from the value created by the network effects. 

There are three methods to estimate FRAND (these have been used in SEPs and telecom regulation). These methods are i. Retail-pricing, ii. Benchmarking, and iii. Value-based. The first two are unlikely to form basis of FRAND in app stores. The methods alluded to above are effectively Value-based. To become workable definitions, it is clear that we must improve the basis of value based methodologies significantly.

### **Solution**

To make progress on practical guidance toward regulating the Access Fee we lay out basic conditions necessary to estimate indirect network effects. We supplement this model with data. We expand on this in accompanying code. 

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
