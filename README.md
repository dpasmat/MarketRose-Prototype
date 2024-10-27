# MarketRose

In this note we describe two methods to guide pricing decisions based on legal principles that are legislated to redesign features of the market for mobile app stores.

## App Stores - Distribution Fees

### **Context**

Governments around the world are proposing or enforcing new laws (rules) governing digital markets. The emerging dispute between Apple and EC relates closely to the fee structure the former can apply to 3P apps. This dispute previews a price regulation problem that will play out in several jurisdictions in the coming years. Failing to resolve this problem leads to high transaction costs and economically inefficient prices. Consequently there is high value to developing solutions to this problem. We expand in four steps _1._ Principles, _2._ Problems (Existing Solutions), _3._ Prototype (new solution), _4._ Remarks (limits and tradeoffs).  

### **1. Principles**

The EC lays out two principles to regulate this group of decisions (fairness, contestability).

_Contestability_  The EC may object to Apple’s proposed fee structure if it determines that this structure limits entry and expansion of alternative app stores. But it is unlikely that the EC will induce Apple to change decisions sufficiently to create meaningful entry by alternative app stores in the near future. For this reason it is unlikely that the regulator’s decisions based on the principle of contestability will render moot its decisions based on the principle of fairness.

_Fairness_ In some instances the gov-regulator must be prepared to effectively regulate prices and to do this it will rely on the principle of fairness (FRAND). Anticipating this challenge, recent commentators provide an economic definition of fairness and argue it is consistent with any discussion of the term as written in the DMA. 

_Surplus_ App stores generate value from at least two sources a. value of indirect network effects (app developers, users) and b. features (characteristics) of the app store or OS. These two sources interact with one another, i.e. the platform takes actions to grow network effects.  

### **2. Problems + Existing Solutions**

There are three methods to estimate FRAND (these have been used in SEPs and telecom regulation). These methods are i. Retail-pricing, ii. Benchmarking, and iii. Value-based. The first two are unlikely to form the basis of FRAND in app stores. To explore the third method, Padilla (2024) suggests reviewing business plans or perhaps using surveys to ask users how important certain characteristics of the platform are.

#### **2.1 Inadequacy of existing solutions**

Existing value-based methods are unsatisfactory as a basis to develop FRAND app store fees. The monopoly on app stores makes it meaningless to ask users about attributes of alternative stores. Qualitative suggestions of how much value one side brings to the other are unsound. We need a method to determine how to separate the value of the platform from the value created by the indirect network effects between app developers and users. 

### **3. Prototype**

We code a prototype under which advertiser and viewability metrics provide valid identification for indirect network effects on the app ecosystem. To derive these conditions we exploit two features 1. the Apple Store/iOS user experience (UX) and app experience (CX), and 2. data (metrics) that the platform makes available to app developers. Joining these two sources we derive variation in the number of users that are effectively available to an app developer. We present an algorithm to transform this data into dollar valuations that developers gain from users. We lay out how this estimate can be used to determine one of many FRAND prices.  

### **4. Remarks**

This prototype illustrates three features 1. It is sufficient to share commonly available, aggregated data to generate FRAND prices (and this does not require privacy protections), 2. this FRAND method formalizes the fairness principle, 3. there are several tradeoffs to consider in extending or applying this prototype to mobile app ecosystems (for example improving accuracy, reducing data burdens).   

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
