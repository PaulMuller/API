# Scanner 3rd-party GrapgQL api documentation
**API endpoints**
+ [generalContractInfo](#generalContractInfo)
+ [stats](#stats)
+ [search](#search)
+ [project](#project)
+ [projectPdf](#projectPdf)
+ [ratingProjects](#ratingProjects)
+ [projectNetworks](#projectNetworks)

## generalContractInfo 
```GraphQL
 generalContractInfo(address: String, network: String)
```

General contract info provide all currently available contract data that was scanned and could retreived with defiyield scanner.
### Prameters
```GraphQL
address: String
network: String
```

### Return statements:
```GraphQL
{
  symbol: String
  name: String
  network: String
  block_time_in_minutes: Float
  hashing_algorithm: String
  categories: [String]
  description: String
  homepage: String
  blockchain_site: String
  official_forum_url: String
  chat_url: String
  announcement_url: String
  subreddit_url: String
  image: String
  country_origin: String
  address: String
  sentiment_votes_up_percentage: Float
  sentiment_votes_down_percentage: Float
  market_cap_rank: Float
  coingecko_rank: Float
  developer_score: Float
  community_score: Float
  liquidity_score: Float
  public_interest_score: Float
  current_price: {
    usd: Float
    eth: Float
    btc: Float
  }
  total_value_locked_btc: Float
  total_value_locked_usd: Float
  ath: {
    usd: Float
    eth: Float
    btc: Float
  }
  ath_change: {
    usd: Float
    eth: Float
    btc: Float
  }
  atl: {
    usd: Float
    eth: Float
    btc: Float
  }
  atl_change: {
    usd: Float
    eth: Float
    btc: Float
  }
  total_volume: {
    usd: Float
    eth: Float
    btc: Float
  }
  high_24h: {
    usd: Float
    eth: Float
    btc: Float
  }
  low_24h: {
    usd: Float
    eth: Float
    btc: Float
  }
  price_change_24h: Float
  price_change_percentage_24h: Float
  market_cap: {
    usd: Float
    eth: Float
    btc: Float
  }
  market_cap_change_24h: Float
  market_cap_change_percentage_24h: Float
  total_supply: Float
  max_supply: Float
  circulating_supply: Float
  forks: Float
  stars: Float
  subscribers: Float
  total_issues: Float
  closed_issues: Float
  pull_requests_merged: Float
  pull_request_contributors: Float
  commit_count_4_weeks: Float
  last_updated: String
}
```


## stats
```GraphQL
stats
```

Total statistic amount of scanned addresses and founded issues and scams. Addition provides total fund lost across scam database

### Return statements:
```GraphQL
{
  totalScanned: Int
  totalIssues: Int
  totalScams: Int
  totalFundsLost: Int
}
```

## search
```GraphQL
search(name: String, address: String)
```
Brief info about address

### Parameters:
```GraphQL
  name: String
  address: String
```
### Return statements:
```GraphQL
{
  id: Int
  address: String
  network: Int
  name: String
  logo: String
}
```


## project
```GraphQL
project(id: Int)
```

Total findings about project

### Parameters:
```GraphQL
  id: Int
```

### Return statements:
```GraphQL
{
  id: Int
  address: String
  network: Int
  name: String
  contractName: String
  onChainScanned: Int
  staticAnalizeScanned: Int
  diffCheckScanned: Int
  logo: String
  compilerVersion: String
  proxy: Int
  txCount: Int
  initialFunder: String
  initialFunding: Float
  mint: Float
  pause: Float
  migration: Float
  issues: [{
    id: Int
    confidence: String
    impact: String
    description: String
    snippet: String
    scwName: String
    scwTitle: String
    scwDescription: String
    scwSolution: String
  }]
  diffs: [{
    id: Int
    address: String
    network: Int
    name: String
    projectName: String
    score: Float
    createdAt: String
  }]
  stats: {
    low: Int
    medium: Int
    high: Int
    total: Int
  }
}
```


## projectPdf
```GraphQL
projectPdf(address: String!, network: Int!, remake: Boolean)
```
Get link for pdf with scan results
### Parameters:
```GraphQL
  address: String!
  network: Int!
  remake: Boolean
```
### Return statements:
```GraphQL
{
  status: String
  filename: String
}
```

## ratingProjects
```GraphQL
ratingProjects
```

Get information for Rating page

### Return statements:
```GraphQL
{
  id: Int
  address: String
  network: Int
  name: String
  category: String
  logo: String
}
```

## projectNetworks
```GraphQL
projectNetworks(address: String!)
```
Awailable networks

### Parameters:
```GraphQL
{
  address: String!
}
```
### Return statements:
```GraphQL
{
  id: Int
  name: String
  logo: String
}
```






  
  
