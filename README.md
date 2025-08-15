### Problem Statement
- The portfolio team needs to decide whether the current ETF strategy should continue to be deployed into the next 12 months. The decision owner is the Portfolio Manager. The output will be operated by the quant analyst and monitored by risk. The business need is to avoid allocating capital to a strategy whose edge has decayed, while don't sell security that can provide risk-adjusted excess returns too early.
- The useful answer is predictive which is a forward-looking view of expected net alpha versus a suitable benchmark, with uncertainty bands and simple decision triggers. We will produce a forecast distribution for 12-month net excess return, scenario notes, and a go/hold/stop recommendation tied to acceptance criteria the PM sets. We will also report descriptive diagnostics to support the decision.

### Stakeholder & User
- Decision owner: Portfolio Manager (PM)
- Tool/operator: Quant analyst, Risk team, Portfolio Manager
- Timing & workflow context: Analysis produced on a monthly to support the Investment Committee.

### Useful Answer
- Descriptive / Predictive / Causal: The useful answer is framed as predictive, supported by descriptive diagnostics.
- Metric or artifact: The primary metric will be the forecast distribution of the next 12-month net excess return versus the benchmark, measured after trading costs and fees. The main artifact delivered will be a one-pager summarizing the forecast and risk bands, along with a rerunnable notebook that can be refreshed with updated data.

### Assumptions & Constraints
- The analysis relies on several assumptions and constraints that define the scope of the strategy evaluation. We assume approximate stationarity of alpha drivers, with no major structural breaks in the ETF universe during the forecast horizon. Data inputs must be point-in-time, free from look-ahead bias, and processed through a reproducible process.

### Known Unknowns / Risks
- There are several uncertainties and risks that may affect the reliability of the evaluation. A key concern is regime change or signal decay, where the underlying drivers of alpha may weaken or disappear over time. Transaction costs could be misestimated, particularly if liquidity conditions shift. Data issues such as selection bias, or overfitting in model development may also distort performance estimates. In addition, errors in the risk model could lead to misleading conclusions. Finally, unexpected market shocks present ongoing risks that must be monitored throughout the lifecycle of the strategy.

### Lifecycle Mapping
- The lifecycle of this project begins with validating whether the ETF strategy retains an edge, which is the central goal of Stage 1 and is addressed through the scoping paragraph and README. Once framed, the next step is to align on decision criteria and metrics, producing a specification and acceptance criteria that guide the analysis. Stage 2 will then focus on preparing a reproducible dataset to establish a clean foundation for modeling. Stage 3 will center on estimating predictive performance through backtests and forecast notebooks, while Stage 4 culminates in delivering a report and checklist to support a clear continue, hold, or stop decision.