# Crypto ERC20 Scout

## Description for Model

This plugin provides very accurate information about well known ERC20 tokens that live on EVM-compatible blockchains such as ethereum, arbitrum, polygon, optimism, xdai and much more.
Popular token lists authored by different entities are getting indexed and aggregated to come out with the best results and make the search as exhaustive as possible. Indexed token lists all conform to the Uniswap token list standard.
This plugin allows anyone to query this aggregation of lists to retrieve information about tokens or less frequently the indexed lists themselves.
Search endpoints are provided for that matter, allowing search by token symbol, contract address or even specific tags as specified by the token list specification.
Each search endpoint supports additional filters on chain identifiers, list names, and more.
When possible, explorer links to the token's contract are generated so that the user can directly jump to the explorer for more advanced analysis.
When possible, a logo URI is provided along with the token data so that a nice preview can be displayed.
When a token is returned, other entries from other lists were most likely merged to form only one final token and make the response more clear. In the returned token data, the name of the lists that reference the given token are given. Preference is given to a token from a given list depending on a set of factors, for instance whether it has a logo URI or not.
When searching tokens the result always gets paginated. A cursor field is systematically added to the response so that it can be used to query the next page (if any),
The endpoint to search lists however returns all the lists at once.
Token pricing info is also provided using the CoinGecko API at the moment. If the plugin gets used a lot it is expected for the pricing info to take time to get retrieved or even fail since the API's rate limit is very restrictive.
Since the database against which searches are being made is based on exhaustive token lists some new or very niche tokens might not be retrievable. However that should do it for most tokens.

Here are some prompts that illustrate the plugin capability:

- Get me the most popular stablecoins on ethereum mainnet
- Fetch the token info associated with the contract address 0x000000000000000000000000000
- List all the chains where the MATIC token can be found.
- Get me all the token lists.
- Is the BUSD token available on Polygon ?
- What's the address of the USDC token on ethereum mainnet ?
- What's the current price of MANA on Polygon ?


