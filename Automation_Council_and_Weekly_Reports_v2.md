# Objective 

To develop a script that enhances the functionality of the existing reporting tool available at [joy-council-report.vercel.app](https://joy-council-report.vercel.app). The script should be capable of generating two types of reports: 
- Weekly Roundup
- Council Report


# Weekly Roundup

The following adjustments should be made to the current version of the reporting script (https://joy-council-report.vercel.app):

- Users can navigate to the Weekly Report Data section (already implemented).
- Users can select the interval for Weekly Report Data (already implemented).
- Users can click a button to generate a text file. This file will contain the Weekly Report Data, compiled with GitHub markup and formatted as follows (new feature):

## ------------- FORMAT EXAMPLE START -------------

## Period

**28 October 2023 - 04 November 2023**

- Start Block:  `4,640,412`
- End Block:  `4,741,212`

# Tokenomics

- Total supply: **1,035,085,728** JOY**
- JOY inflation (since mainnet launch): **3.50%**
- Circulating supply:  **682,898,250 JOY**
- Weekly Tokens Minted: **986,304 JOY**
- Weekly Tokens Burned: **(213,955) JOY**

MEXC exchange wallet:

- Balance:  **91,143,907 JOY**
- Weekly Balance change: **2,791,438 JOY**

DAO Spending:

- Start Issuance: **1,034,099,424 JOY**
- End Issuance: **1,035,085,728 JOY**
- Total minted (net): **986,304 JOY**

*including:*

- Council rewards: **116,667 JOY**
- WG spent: **808,333 JOY**
- Funding proposals: **10,050 JOY**
- Creator payout: **7,500 JOY**
- Validator rewards: **257,721 JOY**
- Fees and token burn: **(228,285) JOY**

# **Content**

### Videos

- Total Videos, qty: **358,664**
- Weekly Videos Growth, qty: **40,693**
- Weekly Videos Growth, %: **12.8%**

![https://i.imgur.com/HsXeaYG.png](https://i.imgur.com/HsXeaYG.png)

### Channels

Provided stats below are for non-empty channels only:

- Total Channels, qty:  **8,209**
- Weekly Channels Growth, qty: **1,601**
- Weekly Channels Growth, **24.2%**

### Media Storage

- Total Storage Used: **29,359 GB**
- Weekly Storage Used Growth: **2,420 GB**
- Weekly Storage Used Growth, %: **9.0%**

![https://i.imgur.com/RtZW8wi.png](https://i.imgur.com/RtZW8wi.png)

### Video NFTs

- Total NFT: **3,122**
- Weekly NFT Growth: **231**
- Weekly NFT Growth, %: **7.9%**
- Weekly NFT sold: 4

![https://i.imgur.com/m9GxS1j.png](https://i.imgur.com/m9GxS1j.png)

# **Membership**

- Total Membership Accounts: **23,602**
- Weekly Membership Accounts Growth: **3,331**
- Weekly Membership Accounts Growth, %: **16.4%**

![https://i.imgur.com/XsgtUAB.png](https://i.imgur.com/XsgtUAB.png)

## ------------- FORMAT EXAMPLE END -------------


# Council Report

The following adjustments should be made to the current version of the reporting script (https://joy-council-report.vercel.app):

- Users can navigate to the Council Report section (already implemented).
- Users can select the interval for Council Report (already implemented).
- Users can fill in USD rate for the term which is called "EMA30 currnet term", "EMA30 prev term" (new feature)
- Users can click a button to generate a text file. This file will contain the Council Report, compiled with GitHub markup and formatted as follows (new feature):

## ------------- FORMAT EXAMPLE START                   -------------
## ------------- Notice: planned values can be ommitted -------------


- Dates: October 16,2023 → October 30, 2023
- Council Term: 21
- Start block: `4,449,620`  `0x4ef054c25517a6316fc38a0cecd04f1769127518070129a1a6cf92e266ce03e4`
- End block: `4,665,621` `0xe59a1eaa9dc51c75e1e99890b287c4acf6df152145f4d091965ee507462decd0`

## 1. Composition

- **chaos77**, 30%
- **leet_joy**, 19%
- **0x2bc**, 3%

Election results: https://pioneerapp.xyz/#/election/past-elections/0000000l

## 2. General stats

- Channels:  **4215** (total **6914**)
- Videos: **162,670** (total **325,586**)
- Storage Used: **9,219** GB (total **27,278** GB)
- Forum threads: **26** (total **668**)
- Forum posts: **138** (total **5,220**)
- Proposals: **31** (total **614**)
- Memberships: **8,554** (total **21,310**)
- EMA30: **0.031 USDT**

## 6. Budget

**Overview**

- Starting Council budget: **28,718,634 JOY**
- Spending from Council budget: **1,637,480 JOY**
- Refill of Council budget: **750,000 JOY**
- Ending Council budget: **27,806,737 JOY**

**Inflation**

Term inflation

- Start issuance: **1,032,572,327 JOY**
- End issuance: **1,034,316,113 JOY**
- Term issuance: **1,743,786 JOY**
- Term issuance: **0.174 %**

Year inflation

- Projected inflation:  **39.43 MJOY**
- Projected inflation:  **3.92 %**

Projected issuance per year is based on total spending so far interpolated to 24 Council terms annually.

**Table 6.1. Inflation**

| Term | Minted, MJOY | Inflation |
| --- | --- | --- |
| 1-15 | 23.6 | 2.36% |
| 16 | 2.15 | 0.22% |
| 17 | 1.67 | 0.167% |
| 18 | 1.76 | 0.176% |
| 19 | 1.64 | 0.16% |
| 20 | 1.65 | 0.16% |
| 21 | 1.74 | 0.17% |
| Total | 34.32 | 3.43 % |

**Table 6.2. Overall Budget** 

| Item | Total spending (planned), JOY | Total spending (actual), JOY | Total spending (planned), USDT | Total spending (actual), USDT |
| --- | --- | --- | --- | --- |
| Council rewards | 250,000 | 249,975 | 7,750 | 7,749 |
| WG spending | 888,566 | 1,538,389 | 30,857 | 47,690 |
| Funding proposals | 0 | 0 | 0 | 0 |
| Creator payout rewards | 20,000 | 10,200 | 620 | 316 |
| Validator rewards | 536,700 | 545,638 | 16,647 | 16,915 |
| Fees and commissions |  | (600,416) | 0 | (18,613) |
| Grand Total | 1,695,266 | 1,743,786 | 55,874 | 54,057 |

**Table 6.3. WGs’ Workers**

| Working group | Workers number (incl Lead) | Workers hired | Workers fired | Workers left |
| --- | --- | --- | --- | --- |
| Builders | 13 |  |  |  |
| Storage | 12 | 1 |  |  |
| Distribution | 8 |  |  |  |
| Forum | 1 |  |  |  |
| Apps | 1 |  |  |  |
| Content | 7 |  |  |  |
| HR | 5 |  |  |  |
| Membership | 1 |  |  |  |
| Marketing | 14 | 4 | 1 |  |
| Total | 62 | 5 | 1 | 0 |

**Table 6.4. WGs’ Budgets, JOY**

| Working group | Start budget, JOY | Refilled, JOY | Spending (planned), JOY | Spending (actual), JOY | Workers rewards, JOY | Lead rewards, JOY | End budget, JOY |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Builders | 10,219 | 341,000 | 179,709 | 362,965 | 362,965 | 124,365 | 29,123 |
| Storage | 221 | 123,426 | 123,425 | 186,017 | 186,017 | 41,040 | 0 |
| Distribution | 64,638 | 80,000 | 91,849 | 108,756 | 108,756 | 156,362 | 47,220 |
| Forum | 1,194 | 15,120 | 15,120 | 15,141 | 15,141 | 15,120 | 1,180 |
| Apps | 5,444 | 7,500 | 10,000 | 10,000 | 10,000 | 0 | 0 |
| Content | 35,177 | 100,000 | 132,540 | 156,427 | 156,427 | 41,040 | 0 |
| HR | 21,313 | 84,649 | 84,649 | 84,240 | 84,240 | 41,040 | 21,417 |
| Membership | 2,052 | 500,000 | 0 | 456,822 | 456,822 | 31,822 | 65,490 |
| Marketing | 51,260 | 150,000 | 200,000 | 158,021 | 158,021 | 124,365 | 51,478 |
| Total | 191,518 | 1,401,695 | 888,566 | 1,538,389 | 1,538,389 | 575,154 | 215,908 |

**Table 6.5. WGs’ Budgets, USDT**

| Working group | Start budget, USDT | Refilled, USDT | Spending (planned), USDT | Spending (actual), USDT | Workers rewards, USDT | Lead rewards, USDT | End budget, USDT |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Builders | 317 | 10,571 | 5,571 | 11,252 | 11,252 | 3,855 | 903 |
| Storage | 7 | 3,826 | 3,826 | 5,767 | 5,767 | 1,272 | 0 |
| Distribution | 2,004 | 2,480 | 2,847 | 3,371 | 3,371 | 4,847 | 1,464 |
| Forum | 37 | 469 | 469 | 469 | 469 | 469 | 37 |
| Apps | 169 | 233 | 310 | 310 | 310 | 0 | 0 |
| Content | 1,090 | 3,100 | 4,109 | 4,849 | 4,849 | 1,272 | 0 |
| HR | 661 | 2,624 | 2,624 | 2,611 | 2,611 | 1,272 | 664 |
| Membership | 64 | 15,500 | 0 | 14,161 | 14,161 | 986 | 2,030 |
| Marketing | 1,589 | 4,650 | 6,200 | 4,899 | 4,899 | 3,855 | 1,596 |
| Total | 5,937 | 43,453 | 27,546 | 47,690 | 47,690 | 17,830 | 6,693 |

### **Proposals**

[https://pioneerapp.xyz/#/council/past-councils/0000000l](https://pioneerapp.xyz/#/council/past-councils/0000000l)

## **7. Financial Dashboard**

### O**verall Spending**

ema30 (current term)= 0.031

ema30 (prev term)= 0.025

| Item | Spending (previous term), JOY | Spending (current term), JOY | Spending (previous term), USDT | Spending (current term), USDT |
| --- | --- | --- | --- | --- |
| Council rewards | 250,560 | 249,975 | 6,264 | 7,749 |
| WG filled | 922,312 | 1,538,389 | 23,058 | 47,690 |
| Funding proposals | 20,000 | 0 | 500 | 0 |
| Creator payout rewards | 17,800 | 10,200 | 445 | 316 |
| Validator rewards | 535,000 | 545,638 | 13,375 | 16,915 |
| Fees and commissions |  | (600,416) | 0 | -18,613 |
| Grand Total | 1,648,477 | 1,743,786 | 41,212 | 54,057 |

**Chart 7.1. Overall spending for current term, JOY**

**Chart 7.2. Overall spending for current term, USDT**

![https://i.imgur.com/wCUCzX9.png](https://i.imgur.com/wCUCzX9.png)

**Chart 7.3. Overall spending (current term VS prev term), JOY**

![https://i.imgur.com/Q1un79o.png](https://i.imgur.com/Q1un79o.png)

**Chart 7.4. Overall spending (current term VS prev term), USDT**

![https://i.imgur.com/WlMBnOg.png](https://i.imgur.com/WlMBnOg.png)

### **WGs’ Spending**

EMA30 (current term)= 0.031

EMA30 (prev term)= 0.025

| Working group | Spending (previous term), JOY | Spending (current term), JOY | Spending (previous term), USDT | Spending (current term), USDT |
| --- | --- | --- | --- | --- |
| Builders | 130,700 | 362,965 | 3,268 | 11,252 |
| Storage | 191,954 | 186,017 | 4,799 | 5,767 |
| Distribution | 239,200 | 108,756 | 5,980 | 3,371 |
| Forum | 15,120 | 15,141 | 378 | 469 |
| Apps | 2,839 | 10,000 | 71 | 310 |
| Content | 125,930 | 156,427 | 3,148 | 4,849 |
| HR | 84,650 | 84,240 | 2,116 | 2,611 |
| Membership | 0 | 456,822 | 0 | 14,161 |
| Marketing | 205,000 | 158,021 | 5,125 | 4,899 |
| Total | 995,393 | 1,538,389 | 24,885 | 47,690 |

**Chart 7.5. WGs’ spending for current term, JOY**

**Chart 7.6. WGs’ spending for current term, USDT**

![https://i.imgur.com/F5LvVSE.png](https://i.imgur.com/F5LvVSE.png)

**Chart 7.7. WGs’ spending (current term VS prev term), JOY**

![https://i.imgur.com/FTpajA8.png](https://i.imgur.com/FTpajA8.png)

**Chart 7.8. WGs’ spending (current term VS prev term), USDT**

![https://i.imgur.com/3E3ukWG.png](https://i.imgur.com/3E3ukWG.png)


## ------------- FORMAT EXAMPLE END -------------
