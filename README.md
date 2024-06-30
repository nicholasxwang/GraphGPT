# GraphGPT

GraphGPT is a new machine-learning model tailored for educational purposes emphasizing intuition, logic, and visual presentation. Read the paper [here (link will be added shortly)]().  In this `README.md` file, I will be going over specific details that weren't mentioned in the paper if you would like to learn more about how GraphGPT works.

**Abstract**
> In this work, we introduce GraphGPT, a novel machine-learning approach designed for intuitive, logical, and visual education. GraphGPT is inspired by the observation that scientific graphs help learners visualize concepts, while causal graphs enhance the logic of responses. By combining the masked prediction capabilities of GPT with transform prediction using causal graphs, we can improve explanation accuracy. GraphGPT generates logical steps alongside diagrams, significantly enhancing intuition and visual presentation compared to ChatGPT. Experimental results show that GraphGPT outperforms ChatGPT by 25\% in accuracy for multiple-choice questions. Furthermore, a vast majority of participants in the subjective tests confirmed that GraphGPT surpasses ChatGPT in all four evaluation categories. Many highlighted the diagrams and graphical explanations as key factors, giving GraphGPT a notable intuitive advantage.


## Why GraphGPT over Text-Based GPTs?
Many students learn better in a classroom with a teacher explaining or even with a peer tutor than at home, reading a textbook. Why? This is because when someone is taught a topic in person, they are learning it intuitively and often visually, on a whiteboard. Modern AI technologies such as ChatGPT cannot accomplish this as they are a text model. However, ChaGPT understands the struggles of students learning intuitively and bridges this gap in AI Education.

Learning with graphs and diagrams offers countless advantages such as
- **Graphs never lie.** Sometimes, your intuition or logic might not be the answer.
- **Graphs are memorable.** During a timed test, its much easier to draw one graph and shift the lines than going through each step, and even risk making silly mistakes.
- **Graphs are intuitive.** Often, definitions or relationships might not make sense for a student new to the subject. However, with graphs, its much more straightforward.
- **Visual Learning.** Many students are visual learners and would prefer to "see" concepts in front of them

## 💰 Macroeconomics (Example of GraphGPT)
> Credits to [Alex Chen](https://github.com/dynoscord) for helping me with this

**Macroeconomics** is a social science that studies the performance, structure, behavior, and decision-making of an economy of a country as a whole. 

There are 6 key graphs in Macroeconomics:
- Supply & Demand
- PPC (Production Possibilities Curve)
- AD/AS (Aggregate-Demand/Aggregate-Supply)
- Philips Curve
- Money Market
- Loanable Funds

Key Formulas
- $AD = C+I+G+X$
- $r = nIR - eIR$


### Variables
| Symbol | Meaning                   |
|--------|---------------------------|
| S      | Supply                    |
| D      | Demand                    |
| C      | Consumer Spending         |
| I      | Investment Spending       |
| G      | Government Spending       |
| X      | Exports                   |
| M      | Imports                   |
| NX     | Net Exports               |
| AD     | Aggregate Demand          |
| AS     | Aggregate Supply          |
| PL     | Price Level               |
| Y      | Output                    |
| SRPC   | Short Run Philips Curve   |
| U      | Unemployment              |
| Inf    | Inflation                 |
| MS     | Money Supply              |
| DR     | Discount Rate             |
| IoR    | Interest on Reserve       |
| r      | Interest Rate             |
| nIR    | Nominal Interest Rate     |
| rIR    | Real Interest Rte         |
| SLF    | Supply of Loanable Funds  |
| DLF    | Demand of Loanable Funds  |
| QLF    | Quantity of Loanable Funds|
| Q$     | Quantity of Money         |

### Macroeconomics Causal Graph 
```mermaid
graph TD
    S --> P
    S --> Q
    D --> P
    D --> Q
    C --> AD
    I --> AD
    G --> AD
    NX --> AD
    M --> NX
    X-->NX
    AD-->Y
    AD-->PL
    AS-->Y
    AS-->PL
    AS-->SRPC
    SRPC-->AS
    AD-->U
    AD-->Inf
    Inf-->PL
    PL-->Inf
    Y-->U
    U-->Y
    SelfAdjustment --> AS
    Fiscal-->Tax
    Fiscal-->G
    Monetary-->Bonds
    Bonds-->MS
    Monetary-->DR
    Monetary-->RR
    DR-->r
    RR-->r
    Tax-->C
    PPC-->LRAS
    LRAS-->PPC
    LRPC-->LRAS
    LRAS-->LRPC
    PPC-->LRPC
    LRPC-->PPC
    I --> Growth
    Growth-->LRAS
    MS-->nIR
    MS-->Q$
    MD-->nIR
    MD-->Q$
    SLF-->rIR
    SLF-->QLF
    DLF-->rIR
    DLF-->QLF
    IOR-->r
    nIR-->r
    rIR-->r
    r-->I
    LRAS --> SelfAdjustment
    SelfAdjustment --> AS
    Wages--> PL
    r --> Appreciation
    r --> Depreciation
    PL --> Appreciation
    PL --> Depreciation
    Appreciation --> NX
    Depreciation --> NX
    ForeignInvestment --> r
```

### Macroeconomics Graphs
#### PPC
The PPC shows tradeoffs and the opportunity cost between two goods.
![image](https://github.com/nicholasxwang/GraphGPT/assets/80929436/2c1ada98-b5b4-46c4-80f6-89544aae4d76)


#### Supply & Demand
The Supply/Demand graph relates “Price” to “Quantity,” where the intersection is the current Price and Quantity
![image](https://github.com/nicholasxwang/GraphGPT/assets/80929436/51887015-f2d5-4fb4-ba13-edb1e8e3684d)


#### AD/AS
AD/AS is a graph relating “Price Level” to “Real GDP” where the current “position” of the country is the intersection of AD and AS
![image](https://github.com/nicholasxwang/GraphGPT/assets/80929436/0f7f18c5-8adb-4c78-afe1-1be81c53797c)


#### Philips Curve
The Philips Curve is a graph relating "Unemployment" to "Inflation".

![image](https://github.com/nicholasxwang/GraphGPT/assets/80929436/b6805266-bed8-4f73-a5ba-45f48659f392)


#### Money Market
The Philips Curve is a graph relating "Nominal Interest Rate" to "Quantity of Money".
![image](https://github.com/nicholasxwang/GraphGPT/assets/80929436/a43787d2-1a70-4e88-b806-10068408d8be)


#### Loanable Funds
The Philips Curve is a graph relating "Real Interest Rate" to "Quantity of Loanable Funds".
![image](https://github.com/nicholasxwang/GraphGPT/assets/80929436/91f44214-3782-4dba-a2c6-60be6fca3587)





### Questionaire
Questionaire is linked [here](https://docs.google.com/document/d/1aQat4cVoHsBqe1YZONiW4iaPVp-nlCsoxwKSrpdNQCY/edit).


### Text-Processing and Rendering
### List of Commands
| Command          |                                         Operands                                        |                                         |
|------------------|:---------------------------------------------------------------------------------------:|----------------------------------------:|
| `NEW`            |       `PPC`, `Supply/Demand`, `AD/AS`, `Philips`, `Money Market`, `Loanable Funds`      |                     Initiates new graph |
| `LEFT`           |     `Demand`, `Supply`, `AD`, `AS`, `LRAS`, `SRPC`, `LRPC`, `MS`, `MD`, `SLF`, `DLF`    |                 Shifts a line leftwards |
| `RIGHT`          |     `Demand`, `Supply`, `AD`, `AS`, `LRAS`, `SRPC`, `LRPC`, `MS`, `MD`, `SLF`, `DLF`    |                Shifts a line rightwards |
| `OUTWARDS`       | `PPC`                                                                                   | Equivalent to Right, used for `PPC`     |
| `INWARDS`        | `PPC`                                                                                   | Equivalent to Left, used for `PPC`      |
| `LEFTPOINT`      | `Demand`, `Supply`, `AD`, `AS`, `LRAS`, `SRPC`, `LRPC`, `MS`, `MD`, `SLF`, `DLF`        | Shifts the equilibrium point leftwards  |
| `RIGHTPOINT`     | `Demand`, `Supply`, `AD`, `AS`, `LRAS`, `SRPC`, `LRPC`, `MS`, `MD`, `SLF`, `DLF`        | Shifts the equilibrium point rightwards |
| `UPPOINT`        | `PPC`                                                                                   | Same as RightPoint, used for `PPC`      |
| `DOWNPOINT`      | `PPC`                                                                                   | Same as LeftPoint, used for `PPC`       |
| `INCREASE`       | `C`, `I`, `G`, `X`, `r`, `rIR`, `nIR`, `QLF`, `Q$`, etc.                                | Indicates an increase in a Variable     |
| `DECREASE`       | `C`, `I`, `G`, `X`, `r`, `rIR`, `nIR`, `QLF`, `Q$`, etc.                                | Indicates an increase in a Variable     |
| `FISCALPOLICY`   | `Increase Tax`, `Decrease Tax`, `Increase Spending`, `Decrease Spending`                | Shows any fiscal policy taken           |
| `MONETARYPOLICY` | `Increase IoR`, `Decrease IoR`, `Buy Bonds`, `Sell Bonds`, `Increase DR`, `Decrease DR` | Shows any monetary policy taken         |
| Anything Else    | Anything                                                                                | Treated text instructions               |

### Macroeconomics Dataset Example Questions
> At this time, I am unable to reveal the entire dataset but a significant amount will be listed below.

What happens to equilibrium quantity and price after an increase in demand?
> `[NEW "Supply/Demand"]` We use a supply and demand model to model this question.  `[RIGHT "D"]`  `[INCREASE "Price]` `[INCREASE "Quantity"]` As a result of the shift, Price and Quantity both increase.

## Further Applications to Various Subjects

### 🛒 Microeconomics
Graphs and Diagrams in Microeconomics include:
- Supply/Demand
- PPC (Possibilities Production Curve)
- International Trade with Tarrifs
- Perfect Competition
- Monopoly
- Natural Monopoly
- Monopolistic Competition
- Game Theory
- Labor Markets
- Monospony
- Externalities

### ⚡ Physics
Graphs in Physics include:
- Position-Time
- Velocity-Time
- Acceleration-Time
- Force-Time
- Force-Displacement

### 🧪 Chemistry
- Organic Chemistry
- Lewis Dot Structure

### $\pi$ Algebra
- Polynomials
- Sinusoids
- Trigonometry

### 🌱 Biology
- Cell Diagrams
- Plant Diagrams
- Animal/HUman Body Diagrams

### $\triangle$ Geometry
- Angle Chasing
- Similar Triangles
- Areas
- Volumes
- 3D Traversals

### $\int$ Calculus
Concepts in Calculus that can be explained visually can be:
- Integration
  - Riemann Sums
- Differentiation
  - Relationship between multiple degrees of differentiation for the same function
  - Instantaneous Slope

### 🌍 History
- Timelines
- Flowcharts
