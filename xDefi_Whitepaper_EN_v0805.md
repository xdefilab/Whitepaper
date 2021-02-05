# xDeFi : Stack of Decentralized Finance Protocols

2020.8.20 team@xdefi.com

## 0. AMM(Automated Market Making) Manifesto

- AMM has everything you want. AMM is the only thing you need.
- AMM is the source for oracles, sink for lending services, opportunity for arbitragers.
- AMM is the tool for liquidity providers, portfolio managers, and option underwriters.
- AMM belongs to all users, who believe in permissionless, trustless and self-organizing mechanisms. 

## 1. xDeFi Introduction


### 1.1 A brief history of AMM DEXes and other DeFi projects

From the end of 2019, Ethereum community nurtured a large batch of outstanding automatic market-making decentralized exchanges ( i.e. AMM DEX ) which emerged in a +300% CAGR ( according to data from [DeFiPulse](defipulse.com) ). As of the date of writing, multiple successful AMM DEX products have found their own position of Ethereum's history:


- [Uniswap V1/V2](uniswap.org): Initiated from Nov 2nd, 2018. Although developed later than earlier pioneers like Bancor Network or 0x on-chain orderbook trading system, Uniswap has easier exchange curves to understand, lower gas to trade, winning great number of users and new projects' IEO (initial exchange offering) in Jul-Aug 2020. Uniswap V1 only supported exchange pairs between Ethereum and any other token, but in Uniswap V2, trading derivative token like DAI against any other token became possible, which greatly enhanced the liquidity power of Uniswap systems.
- [Kyber Network](kyber.network): Initiated from 2017. Compared to binary pools (Ethereum + any other token) Compared to Uniswap's fixed binary pools of 50%-50% proportion, Kyber introdudced multiple assets at non-fixed proportion in 2019. It can provide about 4 times of liquidity effiency* over Uniswap V1 and 1.5 times over Uniswap V2. 
- [Balancer](balancer.finance): Beta version online at the end of 2019, and incentivized liquidity token distribution initiated from June 1st, 2020. Balancer's pool management is dexterous enough for a wide variety of DeFi user groups, including fund managers, risk managers , liquidity providers and arbitragers. Low liquidity pools became YFI's most important infrastructure, while at the same time, high liquidity pools are themselves crypto-index. Balancer became one of the most used infrastructure in DeFi world, won 2nd highest DAU among many DEXes.
- [Curve.fi](curve.finance): Beta version online at the end of 2019, and incentivized liquidity token distribution initiated from Aug. 2020. Curve.Fi introduced a mixed constant-value market making function, compromising almost all main-stream stable-coins and cross-chain Bitcoins, established a new standard for trading homogeneous tokens**.
- [SushiSwap](sushiswapclassic.org): A famous project which played an almost perfect cold-start, enabling Uniswap's LP token (Liquidity providing proof token) so that it can mining SushiToken, migrate huge amount of TVL (Total Value Locked). Sushi's TVL is over 1B at early September 2020, later migrated back due to tokenization of Uniswap ). DAU and #tnxs of SushiSwap is about 10% of Uniswap V2, and TVL at 1/4 of Uniswap. 
- [MCDex](mcdex.io): Providing ETH perpetual short AMM, a sophisticated but useful tool for Ethereum miners who have graphic cards.



*: Liquidity Efficiency: Defined as $$\text{Liquidity Efficiency := Trading Volume/Total Value Locked}$$
**: Homogeneous tokens share the same underlying assets。

These AMM DEXes are extremely precious data examples, since they achieved more than 6 billion USD TVL in their on-chain trading systems. At the same time, in Ethereum community and even in similar ecosystems like Tron and Polkadot, many DeFi projects,  with different product forms, with greater DAO mechanisms, with better tokeneconomics, and with better fairness are rapidly emerging. Projects like [MakerDAO](), [AAVE(lend)](), [Compound](compound.finance), [Synthetix](synthetix.io) and [YFI](yearn.finance) attend this Cambrion of DeFi in many forms, greatly helped the development of all AMM DEXes. The first time since the ICO mania in summer 2017, people feel the enthusiasm of creativity and species' diversity of Ethereum community.

The two founders of xDeFi are blockchain developers, Ethereum DeFi fans, Ethereum miners (with non-professional rigs). In their opinion, a fully developed DeFi ecosystem should start from well-established infrastructures. Many best practices are introduced in xDeFi ecosystem, including but restricted to : xDEX as one of optimized AMM DEXes, xHalfLife as a money stream protocol, xSTA as a stable coin minted from crypto assets, xNSure as capped-style European option trading platform and liquidity solution, xBadge as a incentive-driven NFT project to encourage behavior beneeficial for the ecosystem based on social consensus, and any other DeFi building blocks which are essential for
a well-ordered market.

xDeFi doesn't focus on different AMM curves or special optimization for any certain trading scenarios, but it proposed a full set of parameters which reward fairness and loyalty from liquidity providers proportional to their contribution. Initial design by a small team fewer than 10 developers and a small group of community volunteers, xDEX is fully ready to embrace DAO after community users had a fully understanding about what problem xDeFi is solving, which could enable xDEX Token with a much more decentralized governance process. 

xDEX liquidity pools introduced several templates for liquidity providers tooo provide liquidity and earn reward ( as well as xDEX token incentives), and for most of these pools, the proportions of tokens are fixed to minimize the slippage, boost the liquidity efficiency to its theoretical limit, and also saving Ethereum mainnet gas fee. Participants in the Liquidity Pools (LP) of xDEX, the so-called XPTs, will be entitled to receive xDEX token incentives according to each users' relative contribution after various adjustment and correction parameters if users stake their XDEX Pool Tokens, which unleash the maximized liquidity providing profitability directly to users in a much more fair way. Transaction fees collected will also be fairly distributed if xDEX work smooth in a long enough period, performing Repurchase & Make strategy introduced by [PlaceHolder](www.placeholder.vc).

xDEX also allow users to establish ordinary pools (multi token tuples, instead of binary token pairs) to satisfy their own demand. New token issuers, risk managers, and liquidity providers are free to establish any pools using any standard ERC-20 tokens (template provided) without any permission. 

In the future, xDEX provided templates for socialization of crypto-funds. Community economists will be invited to create crypto fund, and XPTs are easy to invest in just like ordinary ETFs. Community users can upvote or downvote pools eligible for incentives as ineligible, to maximize rewards on xDEX tokens. xDeFi's founders, as experienced rustlang and Polkadot/Substrate developer and tokeneconomist, can also initiate proposals to migrate the series of xDeFi to other cross-chain protocols or mainnets like Polkadot, Cosmos or Near, on which user experience may benefit from newer features as long as EVM is supported. xDEX's DAO will show astonishing adaptability , versatility and inclusivity.


## 2. xDEX: Features and Advantages

### 2.1 xDEX: Rethink Multi-Asset AMM

We shall first give thanks to outstanding products: UniSwap and Balancer.

Uniswap(V1/V2) implemented constant-product function AMM curve back in 2018: 

$$ V = X \cdot Y $$

to ensure the constant product of the amount of 2 tokens ( assets ) in a particular pool before or after any trading.

To add or remove liquidity, $V$ will change together with pool's LP Token ( proof of liquidity providing ), and the amount of 2 tokens also scales proportionally: $ \delta X$ and $\delta Y$ must conform to

$$ \delta X/X = \delta Y/Y $$

This design provide infinite depth liquidity between these 2 tokens for each other, together with price feeding: 

$$Asset_1/Asset_2 = Y/X $$ 

which equals to 

$$ X \cdot Asset1 = Y \cdot Asset2$$

This formula inherently support a fact that the 2 tokens' ( assets' ) proportion in this portfolio ( pool ) are always kept at  $ 50\%:50\% $, and the goals of "Pool as Oracle", "Automatically Balancing Pool" are naturally achieved. 

In UniSwap V1, one of the 2 assets must be Ethereum. Uniswap V2 removed this constraint.

In [Balancer's Whitepaper](https://balancer.finance/whitepaper/) , an expanded constant weighted multiproduct AMM curve is used: 

$$ V = \prod B_t^{W_t} $$

This expansion provided infinite depth of liquidity between any 2 tokens ( assets ) out of N tokens in the single pool, feeding arbitrary pairs with price : 

$$ Asset_i / Asset_j = \frac{\frac{W_i}{B_i}}{\frac{W_j}{B_j}}$$

which means

$$ (B_1 \cdot Asset_1) : (B_2 \cdot Asset_2) : ... : (B_n \cdot Asset_n) = W_1 : W_2 : ... : W_n  $$


This formula inherently support a fact that the N tokens' ( assets' ) proportion in this portfolio ( pool ) are always kept at  $ W_1 : W_2 : .... W_n $, and the goals of "Pool as Oracle", "Automatic balancing multi-asset pool" are naturally achieved.

xDEX conforms to the basic design of Balancer. In practices, Balancer's typical usages varies between one each other, attracted many geeks to explore many possibilities. Right after its $\$BAL$ tokenization, a bunch of $98\%-2\%$ pools, which composed from extremely unbalanced components, were rapidly emerging. These pools, like many other pools, were established at their owners' wish to play some roles in different scenarios, but in fact most of them were not qualified to provide enough liquidity. On the opposite side, the components' proportion of pools in UniSwap V1/V2 ( and many other AMM DEXes forked from UniSwap) are fixed at $50\%:50\%$ , are extremely easy to use, but no any other choices on providing liquidity. UniSwap has 10 times more DAU than Balancer, but the assets backing any LP-token is usually much more volatile compared to Balancers' BPT, especially when Ethereum's price was under heavy price changes.

Taken the observations above, XDEX's founders design special templates for fixed-ratio multi-asset liquidity pools.

One of the most important template ( quarternary pool)is defined as following:

If $\mathfrak{X}$ is the token name of any asset of high liquidity, we define the liquidity composition as 
$$\mathfrak{X}\text{:wETH:DAI:XDEX's TVL} = 32\%:32\%:32\%:4\% $$

Any liquidity pool is responsible for price feeding of 6 different trading pairs.


We still provide basic ternary liquidity pool:

$$ \text{wETH:DAI:XDEX's TVL} = 48\%:48\%:4\%$$

and voting ternary liquidity pool: 

$$ \text{wETH:DAI:XDEX's TVL} = 32\%:32\%:36\%$$

For DAO voters, adding liquidity to voting pool will increase his/her voting power in higher speed, but he/she cannot buy voting power directly by simple bribery/pump before critical voting.

For users holding UniSwap's LP tokens, SushiSwap's SLPs, or Balancer's BPTs, we encouraged users to instead earn XDEX token by contributing to similar liquidity, but in a discounted speed in certain stages. The discount ratio is discussed in Chapter 3.

We encourage users  holding UniSwap's LP tokens, SushiSwap's SLPs, or Balancer's BPTs manually convert their portfolio into XDEX's pools eligible for incentives. After adding liquidity and staking their XPTs, they can earn XDEX token in undiscounted speed. We don't force them to migrate their LP tokens to XPTs, since the portfolio might be slightly changed.

Only XLP of voting ternary pool $\text{XDEX:ETH:DAI}$ can generate voting rights to vote, conforming to xVote protocol, which will be detailly discussed in Chapter 4.

We are ready to implement any best practices in AMM DEXes, including (but not restricted to) the potential UniSwap V3.

### 2.2 xDEX: Rethink the Choice of Assets

To select suitable $\mathfrak{X}$ for quarternary liquidity pools, XDEX has several basic standards:


- Products ready
- Projects made their income statement/dashboard publicly available
- Standard ERC-20 token
- Tokens in multiple markets of good liquidity

In the last year, XDEX's two founders researched by their own as well as bought reports to investigate more than 50 projects which already issued their ERC-20 tokens. 

Newly issued tokens, after upvote proposal, will be eligible as part of multi-asset liquity pool earning XDEX according to liquidity template.

Non-standard ERC-20 tokens, tokens of unaudited projects and  will be blacklisted in liquidity pools and in ordinary pools.


### 2.3 XDEX: Rethink the Choice of Components' Proportion in Pools

Ordinary pools conforms to the same standard as Balancer, with minor parameters changed:

- Single asset proportion not lower than 5%
- Asset types no more than 8
- Some extra tutorials or templates are given.


For different scenarios, XDEX has multiple different liquidity pool templates:

- $95\%:5\%$: Low impermanent loss pool
- $32\%:32\%:32\%:4\%$: Any liquidity pool ineligible for earning XDEX is welcomed to use this template to test liquidity efficiency. Low price volatility for the entire portfolio, and enough liquidity provided for trading between Components 1-3. 
- $40\%:20\%:20\%:20\%$: For newly issued tokens, liquidity pool ineligible for earning XDEX is welcomed to use this template to suffice its financing demand.


### 2.4 xHalfLife Protocol: Exponentially Decaying Money Stream Protocol

xHalfLife Protocol has 4 parameters for execution: $NumStart$、$K$、$ratio$ and $eps$. Under this protocol, users' reward are split to 2 parts: 

$\text{Deferred Incentives}$ and $\text{Earned Incentives}$.

Any new income enters $\text{Deferred Incentives}$ account.

After $NumStart$ ethereum mainnet block, each time the block number can be divided by $K$, and asset in $\text{Deferred Incentives}$ balance is over $eps$, $ratio \cdot \text{Deferred Incentives}$ in $\text{Deferred Incentives}$ balance will be forwarded into $\text{Earned Incentives}$ account. 

When needed, any asset in $\text{Earned Incentives}$ is free to withdraw.

$50\%$ of any single cashflow under xHalfLife is free to withdraw after 

$$-K / log_2(1-ratio) * 13.1s$$

since time at Ethereum Mainnet Block Height $numStart$

For more detail, refer to yellowpaper/slides of xHalfLife.

For xDEX token distributed via voting liquidity pool, ordinary liquidity pools, and founder teams' fund, any incentives are awarded through xHalfLife protocol.  Our vision is enable this template as a backbone protocol in a wide range of financing activities in crypto asset world.

xHalfLife is inspired by Sablier Protocol.

## 3. xDEX Token Incentive Distribution Among Liquidity Pools: A Fair and Incentivising Design

### 3.1 Distribution Fairness

#### 3.1.1  Fee Designs: Self-Assessed Trading Fee

User select fee rate to establish pools among: 

$$[0.1\%, 0.25\%, 1\%, 2.5\%, 10\%]$$

- Trading fee of liquidity pools eligible for earning XDEX : $0.25\%$
- User-defined Pools: Selected by their owners
- $0.25\%$ part goes into SAFU fund.
  - $0.2\%$ to be repurchase and market making for XDEX
  - $0.05\%$ for referrer (if referrer not null)
- Warning: Exit fee for Voting pools: $1\%$

Self-Assessed Fee Rate is inspire by [Radical Markets: Uprooting Capitalism and Democracy for a Just Society](https://www.amazon.com/Radical-Markets-Uprooting-Capitalism-Democracy/dp/0691177503)



#### 3.1.2 Fair Distribution Among Liquidity Pools: directFactor

$$\text{directFactor} = \text{tokenFactor} \cdot \text{liqFactor} \cdot \text{capFactor}$$

##### 3.1.2.1 tokenFactor

- Voting Pool: 9
- Liquidity Pool eligible for earning XDEX: 1
- Liquidity Pool ineligible for earning XDEX: 0

##### 3.1.2.3 capFactor and liqFactor

$capFactor= round(1 + log(clip (1000000/B_{ETH},1,1000000),10)),\text{ if }B_{ETH}<=1000000$

$capFactor= 1 \text{ if }B_{ETH}>1000000 $

$liqFactor \approx clip(\sqrt{B_{ETH}/100},1,100)$

- $B_{ETH} in [316227.7,): capFactor=1, liqFactor = 100 $
- $B_{ETH} in [31622.77,316227.7): capFactor=2, liqFactor = 32$
- $B_{ETH} in [3162.277,31622.77): capFactor=3, liqFactor = 10$
- $B_{ETH} in [316.2277,3162.277): capFactor=4, liqFactor = 3.2$
- $B_{ETH} in [0,316.2277): capFactor=5, liqFactor = 1$

#### 3.1.3 Potential Fair Distribution Among Native/Outer Homogeneous Liquidity Pools

For liquidity Pool

- Native XPT Staking: 1
- Uniswap/Sushi $ETH/DAI$ LP/SLP Staking : 0.96
- Uniswap/Sushi $\mathfrak{X}$/ETH, $\mathfrak{X}$/DAI LP/SLP Staking: 0.48
- XDEX/Balancer binary unbalanced pool containing $\mathfrak{X}$:
$$min(p_\mathfrak{X}/0.32,p_{ETH or DAI}/0.32,1) \cdot 0.48 $$
- XDEX/Balancer ternary unbalanced pool containing $\mathfrak{X}$:
$$min(p_\mathfrak{X},p_{ETH},p_{DAI}) \cdot 2.88 $$

No migrating mechanism. Users must manually remove their LP/SLP/BPT liquidity, add liquidity to XDEX to get XPT, and stake XPT to earn XDEX token.

In different stages of distribution, XDEX support different outer pool LP tokens to earn xDEX tokens.

In all stages, xDEX support all inner pool XPT tokens to earn XDEX tokens.

### 3.2 xDEX Token Empowered For Users/Voters/Founders

The native digital cryptographically-secured utility token of the xDeFi ecosystem (xDEX tokens) is a transferable representation of attributed functions specified in the protocol/code of the xDeFi ecosystem, which is designed to play a major role in the functioning of the xDeFi ecosystem and intended to be used solely as the primary utility token on the platform.
In order for the xDeFi ecosystem to function properly, users would need to be incentivised to play the role of liquidity providers and stake their digital assets into the market making pools. As compensation for opportunity costs as well as impermanent losses, these liquidity providers which help to promote adoption of the xDeFi ecosystem by staking or including assets to liquidity pools would be rewarded with xDEX tokens tokens (i.e. "mining" on the xDeFi ecosystem), according to each user's relative contribution after various adjustment and correction parameters.

It is anticipated that the community of xDEX tokens holders would comprise a diverse field of developers, professionals and supporters of the project to develop the xDeFi ecosystem (including without limitation experts in software development, blockchain technology, cryptography, artificial intelligence, law or finance), which will be able to share and exchange balanced views on the overall direction of the project, and it is these community members which would drive development of the xDeFi ecosystem. Accordingly, xDEX tokens would allow holders to propose and vote on governance proposals to determine features and/or parameters of the xDeFi ecosystem, with voting weight calculated in proportion to their token holdings. For the avoidance of doubt, the right to vote is restricted solely to voting on features of the xDeFi ecosystem; the right to vote does not entitle xDEX tokens holders to vote on the operation and management of the Company, its affiliates, or their assets, and does not constitute any equity interest in any of these entities.

$xDEX-ETH-DAI$ pools' deferred incentives would allow for corresponding DAO voting power, which is described in Section 4.0 in detail.

Voting liquidity pool's XDEXreward has an unlocking speed 2x faster than the founders.

Ordinary liquidity pools' XDEX reward has an unlocking speed 45x faster than the founders.

According to section 3.1.1, part of xDEX fee enters SAFU fund.

If xDEX system runs smoothly after certain stages of token distribution, according to best practices from [PlaceHolder](www.placeholder.vc), xDEX will perform "Repurchase and Make" strategy routinely to find the possibly  unbiased value of xDEX tokens as well as keep sufficient ETH and DAI capital reserves.

xDEX tends to repurchase xDEX token among multiple markets ( including Uniswap V2 and Balancer) to continuously add exposure to daily DEX users, investors.

If system is under problems or experiencing updates, multi-sig founders and teams and DAO have the rights ( and have the rights to submit proposals which will then be voted on by deferred token reward holders ) to utilize SAFU fund ecosystem development, such as human resource or technological improvements. These free of use \(ETH\) and stable coins will be used to support further ecosystem development.


### 3.3 xDEX Distribution Timetable

Basic Rules: Risk-aware，Loyalty-aware，Fairness-aware.

### 3.3.0 Initial Distribution:

100 million tokens before 4 times of halving.

- 5% For DAO, community and marketing.
  - Initial liquidity in Uniswap, Balancer, and xDEX
  - Community reward programs, 3rd party financial advisors and marketing.
  - Remaining part locked.
- 75% Early stage incentivatin for liquidity providers:
  - 38.4% Four stages of incentivization, 0% Seigniorage.
  - 36.6% TVL milestones for users.
- 10% Initial Team
  - Locked until 4 stages of halving finished. Unlocking patterns comform to xHalfLife.
- 5% To introduce new parters: Professionals in Layer-2 Technology, Substrate development, data analysis, stable coins, and local compliance. If any, their shares will be locked until 4 stages of incentivization finished and unlocking patterns comform to xHalfLife. The remaining will be locked.
- 5% Multi-Sig locked, for private investment: If any, 20% of their shares will be unlocked instantly. 80% of their shares will be unlock until 4 stages of halving finished and unlocking patterns comform to xHalfLife. The remaining will be locked.

xDEX tokens are designed to be consumed/utilised(maily in liquidity pool and minting), and that is the goal of the xDEX tokens token distribution. In fact, the project to develop the xDeFi ecosystem would be halted if all xDEX tokens holders simply held onto their xDEX tokens and did nothing with it.


### 3.3.1 Four stages of Early Bird Reward

Since the genesis block of xDEX token block # 0:

38400000 XDEX tokens will be distributed as incentives according to the following schedule, during 4 stages of liquidity providing:

- 9600000 tokens for block # 1-80000, 120 each.
- 9600000 tokens for block # 80001-240000, 60 each.
- 9600000 tokens for block # 240001-560000, 30 each.
- 9600000 tokens for block # 560001-1200000, 15 each.
- For block # after 1200001, 8 tokens for each block.
- 0% seigniorage lifetime.

### 3.3.2 xHalfLife Protocol To Incentivise Loyalty In User-First Manner

- For founders: Block # after 600000, 0.1% tokens unlocked per 3600 block.
- For voting pool participants: Block # after 0, 0.1% tokens unlocked per 1800 block.
- For ordinary liquidity pool participants: Block # after 0, 0.1% tokens unlocked per 40 block.


### 3.3.3 High Liquidity First

In the early token distribution stages, ERC-20 tokens with high liquidity are automatically added to liquidity pools.

DAO will be responsible for deciding the new ERC-20 tokens which may be eligible for earning XDEX in the next stage.

### 3.3.4 Awards For TVL Milestones

XDEX development team deeply hope founders can gather community users, DeFi fans, DAO fans and institutional participants to achieve multiple TVL milestones  through the distribution of xDEX token incentives.

At the end of each token distribution stage, if TVL reached 1M/10M/100M/1B/10B/100B for the first time, weighted awards will be airdropped to all liquidity providing users in xDEX. If some milestones are not met in the 4 early stages of liquidity providing, xDEX will airdrop xDEX token till milestones are met ASAP.


TVL Milestones incentives (in xDEX tokens 36600000): 

- 1M USD: 300,000
- 10M USD: 300,000
- 100M USD: 900,000
- 1B USD: 2,700,000
- 10B USD: 8,100,000
- 100B USD: 24,300,000


## 4. xDAO Operation


### 4.0 xDAO Voting Power

$\text{Original Power P} = (\text{Founder's Power} + \text{Power in Voting Pool})$

$\text{Weighted Power P} = P/(1+log(1.0+P))$

Voting power is:

- Linearly distributed to reward loyalty
- Slowly dampened to keep prestige
- Mildly squeezed to resist voting bribery 

### 4.1 A Draft: Upvoting and Downvoting For ERC-20 tokens: 

xDEX welcomes any pools with any qualified ERC-20 tokens (standard ERC-20 of non-fraudulent projects) to be traded. In each 40,000 blocks, xDAO collected ERC-20 candidates to be upvoted as liquidity pool tokens, $\{\mathfrak{X}\}$. Effective voting power must exceed 1/3 in this voting, and original voting power must exceed 1/10 in all original voting power. At most 1 erc-20 will be upvoted.

In each 80,000 blocks, any existing ordinary liquidity pool may be proposed to be downvoted to be liquidity pool ineligible for earning XDEX. xDAO collected ERC-20 candidates to be downvoted as liquidity pool tokens which pool is ineliglble for earning XDEX. Effective voting power must exceed 1/3 in this voting, and original voting power must exceed 1/10 in all original voting power. At most 2 erc-20 will be downvoted.

### 4.2 xDEX Recommendation Incentives

xBadge system is under development.

### 4.3 Community Contributors' Reward

DAO has the right to propose and pass rewards to reward active community contributors.

## 5. Risk Management

### 5.1 Market Risk

For tokens in liquidity pools, xDEX hope liquidity providers fully understand various type of market risk: market price risk exposure, impermanent loss, volatility of XPT under different compositions, and loss under extreme scenarios like market flashcrash. 

xDEX hope liquidity providers fully understand the risks of market making processes.

xDEX team and community volunteers will routinely give advices for tokens which may be eligible for earning XDEX.

### 5.2 Options In Extreme Scenarios

xDeFi option product xNSure , capped-style European option is under testing,

Beta version.

### 5.3 Stable Coin Crisis

xDeFi defines xSTA as its native stable coin, to get rid the risk of:

- Any other stable coins unpegged from USD
- USD unpegged from 8 main-stream fiat

xSTA is in design.

### 5.4 Extreme Market Volatility

Some ERC-20 tokens with very low marketcap will suffer a heavy slippage, especially when market crashes. xDEX will warn users to notice those ERC-20 tokens.

### 5.5 FlashLoan Attacks

In history, price attackers manipulates markets with low depth (specially for those with orderbooks), and make profit in AMM. In our experience, LP of AMM DEXes with also make profit under this situation.

### 5.6 Failure of Oracles

ERC-20 with very low LP TVL may cause failure of oracles insider xDEX. Under extreme situation, we will refer to AMM DEXes (Uniswap, BAL, Kyber Network) to get price feeding weighted by their liquidity quality in a time-weighted manner , and then LINK, BAND, NEST APIs to make sure the continuous and unbiased price feeding still being available.


### 5.7 Hacking events

5% Initial Liquidity, and SAFU fund (right after xDEX start to make profit) is the defenses of xDEX from hacking events. xDEX will be audited at least once before online.


Each xDEX upgrade will cause additional audit.

Audit from several more authoritative audit service providers will be listed as soon as the report is ready.

## 6. Project Roadmap

2021Q1

- Basic Features: Ordinary liquidity pools
- At least 3 round of code auditing
- Initiated several stages of LP incentives
- Community established
- DAO's voting for new $\mathfrak{X}:wETH:DAI:XDEX$ incentive pools.

2021Q2-Q3

- Stable Coin open for minting
- More templates for $\mathfrak{X}$ incentives
- DAO mechanism

## 7. References

- [Automated Market Making](https://digitexfutures.com/blog/what-are-automated-market-makers-and-why-do-they-matter/)
- [Radical Markets: Uprooting Capitalism and Democracy for a Just Society](https://www.amazon.com/Radical-Markets-Uprooting-Capitalism-Democracy/dp/0691177503)
- [Uniswap V1 Doc](https://uniswap.org/docs/v1/)
- [Uniswap V2 Doc](https://uniswap.org/docs/v2/)
- [Balancer Whitepaper](balancer.finance/whitepaper)
- [KyberSwap Doc](https://developer.kyber.network/docs/Reserves-Intro/)
- [Synthetix Doc](https://docs.synthetix.io/)
- [MCDex Whitepaper](https://mcdex.io/references/#/en-US/white-paper)
- [Sablier Protocol](https://github.com/sablierhq/sablier)
