# IC-Pay-Protocol
A standardized Payment QR Code protocol built on the Internet Computer (IC)

**1. Background**
   
ICP offers a low-cost, high-speed environment without external infrastructure, making it ideal for building payment protocols.
Payment QR Codes are widely accepted globally, with mature user habits and strong compatibility.
Clear use cases include online e-commerce payments and offline QR-based transactions.

**2. Proposal Objectives**
   
To establish a universal Payment QR Code specification that includes:
A standardized format (e.g., transaction amount, target wallet address, memo field, etc.).
Support for multiple payment tokens (e.g., ICP, ckBTC, etc.).
Extensibility to accommodate future tokens or payment methods.
A standard URL protocol for requesting native ICP transfers, ICRC Token transfers, and ICP transactions allows for a better user experience across apps and wallets in the ICP ecosystem.

**3. Real Case**

With this feature, when users scan the merchant’s QR code using ICP Mobile Wallet, both the transaction amount and the Token type will be automatically populated. This not only significantly reduces the risk of errors caused by manual input or incorrect Token selection but also streamlines the payment process, enhancing user experience and transaction accuracy.

**4. Core Features**
   
QR Code Generation and Parsing Specification

Standardized fields ：
```
recipient: Recipient wallet address.

ledger: The ID of the ledger canister used for payment.

amount: Transaction amount.

memo: Optional memo information.
```

```vb.net
icp:<recipient>
      ?ledger=<ledger>
      &amount=<amount>
      &memo=<memo>
```

Examples
```vb.net
URL describing a transfer request for 1 ICP.
icp:xqvwn-5i4pu-uru5o-igwdh-kum5m-5cms5-5mfj6-duaui-o7lan-hcicc-5qe?ledger=ryjl3-tyaaa-aaaaa-aaaba-cai&amount=1&memo=OrderId12345
```

```vb.net
URL describing a transfer request for 1,000 FPL.(IRCR Token)
icp:xqvwn-5i4pu-uru5o-igwdh-kum5m-5cms5-5mfj6-duaui-o7lan-hcicc-5qe?ledger=ddsp7-7iaaa-aaaaq-aacqq-cai&amount=1000&memo=OrderId12345
```

![本地图片](https://github.com/LEEKOHCHING/ICP-Pay-Protocol/blob/main/icppay.png)

**5. Ecosystem Value**
   
Enhance ICP's competitiveness in the payment sector, attracting more merchants and users.
Strengthen the connection between ICP and real-world applications, promoting mainstream adoption.
Reduce technical costs for developers and merchants while improving user experience.


