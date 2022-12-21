# How to add to this token list

1. fork repo
2. append token info to chain `.js` file (such as `sui/devnet.js`)
3. add icon to `icons` folder, `svg` format, or `webp` `png` size in range `48x48` to `64x64` (no too large)
4. Pull Request

Token Info example:

```javascript
{
  address: '0x2::sui::SUI',
  decimals: 9,
  symbol: 'SUI',
  name: 'Sui',
  logoURL: 'https://tokenlist.andex.finance/icons/SUI.png',
  projectURL: 'https://sui.io/',
}
```

```javascript
{
  address: '0x100cbbf8632ab38788a3996be4717c385c43d54f::coins::USDT',
  decimals: 8,
  symbol: 'USDT',
  name: 'Tether USD',
  logoURL: 'https://tokenlist.andex.finance/icons/USDT.webp',
  extensions: {
    stableUSD: true,
  },
}
```

Coin Schema:
```typescript
class Coin {
  address: string
  decimals: number
  symbol: string
  name: string
  logoURL?: string
  projectURL?: string
  extensions?: object
}
```

* `address`: the address of the token on blockchain
* `decimals`: the decimals of the token
* `symbol`: globally unique symbol within this token registry
* `logoURL`: optional, the URL of the logo of the token
* `projectURL`: optional, the project website of the token
* `extensions`: optional, used for special extra data
