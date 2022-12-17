# Datasets for TDH-DQN trading bots, By Gregory Roy AI/ML Engineer
Multi-Timeframe Algorithmic Trading Bots using Thick Data Heuristics with Deep Reinforcement Learning<br>
This article presents an augmented Artificial Intelligence (AI) algorithmic trading approach that combines Thick Data Heuristic (TDH), with Deep Reinforcement Learning (DRL), to successfully learn trading execution timing policies. Combining the augmented AI human trader's intuition and heuristics with DRL techniques to provide more focused drivers for trading order execution timing is explored in this study. In this research, the goal is to solve the sequential decision-making problem of AI for profitable day and swing trading order timing executions. Enabling trading bots with cognitive intelligence and common-sense heuristics will offer traders including automatic traders an insight to understand the day-to-day swing trading timeframes indicators and arrive at mature trading decision-making. This article examines the performance of bots with Nasdaq and NYSE stocks that have a strong catalyst (info. which increases directional momentum) to find that they outperform benchmark algorithmic trading approaches. The research illustrates to the reader how to combine TDH and Deep Q-networks (DQN) into a TDH-DQN augmented AI trading bot. The bot learns through test data to predict the optimal timing of order executions autonomously on idealized trading time series data.<br>
<br>
SUMMARY: In the author's manuscript titled, 'Multi-Timeframe Algorithmic Trading Bots using Thick
Data Heuristics with Deep Reinforcement Learning' he studied all the modern Artificial Intelligence (AI)
algorithms. When the movies and media refer to "AI", they are referring to the field of Reinforcement
Learning (RL) studied rigorously by computer scientists.<br>
<br>
BACKGROUND: DRL agents can do amazing things, including playing Atari, chess, and Go. And yet they
are all versions of a Turing Machine, which is an abstract model that sets the limits of what can be done by a
computer through its mathematical logic. The author would argue no conscious, intelligent entity is going to
emerge from a Turing Machine. This is the reason the author has taken an augmented AI approach. Currently,
augmented AI is the best form of AI we have available as stock traders. The bots can deal with more tasks
better than human traders do, including predicting stock buying and selling order timing executions [9].
<br><br>
METHODS: In the thesis, combining the augmented AI human trader's intuition and heuristics with DRL
techniques to provide more focused drivers for trading order execution timing was explored. The thesis
illustrates to the reader how to combine Thick Data Heuristics (TDH) and Deep Q-networks (DQN) into a
TDH-DQN augmented AI trading bot. The bot learns through test data to predict the optimal timing of order
executions autonomously on idealized trading time series data.
PROBLEM DEFINITION: Solve the sequential decision-making problem formalized of trading as an MDP
optimization of order timing executions for a single catalyst stock. The environment for the experiments was
comprised of the observation space including the state, discrete action space (discrete for the bot, but
continuous for human (buy, sell, wait)), and finally rewards.
<br><br>
RESULTS: DRL and ML algorithms cannot entirely replace human intuition and heuristics. Complex models,
if not correctly guided can over-fit or uncover false relationships and patterns. Crafting financial models is an
art form more than a science. It's important to test many different model parameters and train the model for the
appropriate market conditions. The author would argue that to be successful at algorithmic trading it is not
about finding the holy grail cocktail of trading rules, sentiment, or fundamental or technical analysis that will
always be correct. It is about crafting specific models using experience and intuition to catalyst stocks at
specific times.
<br>
CONCLUSIONS: The application of DRL still requires significant human intervention and domain expertise.
Humans must still be relied upon to define objectives, select, and curate data, design and optimize a model,
and make appropriate use of the results. The use of powerful models with a high capacity to learn patterns
requires particular care to avoid over-fitting when the signal-to-noise ratio is as low as is often the case with
financial data. Furthermore, the competitive nature of trading implies that patterns evolve quickly as signals
decay, requiring additional attention to performance monitoring and model maintenance.
<br>


The TDH-DQN Augmented AI process for building and implementing a trading bot that uses a combination of deep reinforcement learning (DRL) and hard-coded rules to trade assets in the financial markets is explored. The trading bot is designed to analyze the market in real-time and identify opportunities to maximize returns while minimizing risk.
<br>
The first step in the process is to analyze the market during the pre-market session using real-time data on high volume percentage gainers and losers. A human trader is responsible for building a pre-defined list of stocks based on high relative volume, news, and technical analysis, which serves as a watchlist for the trading bot to monitor. The human trader also uses Multicharts.Net to perform parameter optimization, backtesting, fib-analysis, and price level identification based on previous pivot points.
<br>
Next, the trading bot creates policies to maximize the annual percentage rate (APR) for the pre-approved catalyst stocks. This is done by training and testing the model on real-time data at various time series intervals (5 seconds, 1 minute, 5 minutes, 1 hour, daily, weekly, monthly). Python libraries and datasets are loaded, and the data is explored and analyzed using technical analysis of multi-timeframe moving averages. A train-test split is then performed, with 70% of the dataset used for modeling and 30% for testing.
<br>
The DRL loop then begins, which involves retrieving the current state of the market, applying the best action recommended by the model, getting the reward, and obtaining the next state. This process is repeated until the batch is complete, at which point the data is added to memory and the replay buffer function is run. The replay buffer function updates the Q-function using the updated Bellman equation, and compares the Q-predicted and Q-target values to calculate the buy, sell, and hold actions. The Q-function is then updated by minimizing the mean squared error (MSE) between the Q-predicted and Q-target values, and the artificial neural network (ANN) is fit. This process is repeated until the specified number of epochs is complete.
<br>
The model is then tested, and the model's parameters (such as Gamma, Epsilon, episode size, batch size, window size, and number of layers and nodes in the ANN) are fine-tuned as needed to achieve an APR of greater than 5% for both the training and test data. If the time is greater than 9:30 am EST, the trading bot switches from testing mode to live trading mode. It executes live orders when the stock matches the high volume rate market scanner and the pre-defined stock watchlist, and has a high volume rate of more than one million shares per three-minute bar. The trading bot also analyzes real-time market scanners and compares them to the pre-defined watchlist to identify potential trades. Risk is managed using profit targets and stop loss orders, and the trading bot exits its positions at the end of the day or after a predetermined number of bars.
<br>
The TDH-DQN Augmented AI Pseudo Code also includes a set of hard-coded trading rules that are used to filter the trade execution orders generated by the DRL agent. These rules are based on factors such as time of day, risk, volume, technical analysis of multi-timeframe exponential moving averages (EMAs), and price levels. The process is repeated by downloading new data, backtesting for parameter optimization, training the model, and executing new orders that are filtered by the hard-coded rules and the human trader, if required. This process continues at each primary time series interval until 4 pm EST, when the market closes.
<br>
<br>
To implement a TDH-DQN trading bot using the Interactive Brokers API in Python, you can follow these steps:
<br>
Set up an account with Interactive Brokers and obtain your API credentials.
Install the Interactive Brokers Python API by following the instructions provided in the API documentation.
Familiarize yourself with the Interactive Brokers API documentation and the various functions and methods that are available for accessing market data, placing orders, and managing your account.
Determine the specific assets that you want to trade and the market conditions under which you want to trade them. This will help you to design the reward function for your TDH-DQN trading bot.
Design and implement the TDH-DQN algorithm for your trading bot. This will involve designing the neural network architecture, choosing an appropriate training algorithm, and implementing the Q-learning update rule.
Test your trading bot on historical data to ensure that it is functioning correctly and generating satisfactory returns.
Integrate your trading bot with the Interactive Brokers API to enable it to access live market data and place trades on your behalf.
Test your trading bot on live market data and fine-tune it as needed to optimize its performance.

<br>



<br>
[Presentation Video describing the Trading Bots](https://youtu.be/sUZHrpG-JMs)
<br><br>
[Article: Multi-Timeframe Algorithmic Trading Bots using Thick Data Heuristics with Deep Reinforcement Learning](https://ojs.wiserpub.com/index.php/AIE/article/view/1722)
<br><br>
[Ateriox AI](http://ateriox.com)



