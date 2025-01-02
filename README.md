# ICP-Pay-Protocol
A standardized Payment QR Code protocol built on the Internet Computer (ICP)
Proposal Framework
1. Background
ICP offers a low-cost, high-speed environment without external infrastructure, making it ideal for building payment protocols.
Payment QR Codes are widely accepted globally, with mature user habits and strong compatibility.
Clear use cases include online e-commerce payments and offline QR-based transactions.

2. Proposal Objectives
To establish a universal Payment QR Code specification that includes:
A standardized format (e.g., transaction amount, target wallet address, memo field, etc.).
Support for multiple payment tokens (e.g., ICP, ckBTC, etc.).
Extensibility to accommodate future tokens or payment methods.
A standard URL protocol for requesting native ICP transfers, ICRC Token transfers, and ICP transactions allows for a better user experience across apps and wallets in the ICP ecosystem.

4. Core Features
QR Code Generation and Parsing Specification
Standardized fields ：
recipient: Recipient wallet address.
token: Type of token used for payment.
amount: Transaction amount.
memo: Optional memo information.

icp:<recipient>
      ?token=<token>
      &amount=<amount>
      &memo=<memo>

Examples
URL describing a transfer request for 1 ICP.
icp:xqvwn-5i4pu-uru5o-igwdh-kum5m-5cms5-5mfj6-duaui-o7lan-hcicc-5qe?token=icp&amount=1&memo=OrderId12345

URL describing a transfer request for 1,000 FPL.(IRCR Token)
icp:xqvwn-5i4pu-uru5o-igwdh-kum5m-5cms5-5mfj6-duaui-o7lan-hcicc-5qe?token=fpl&amount=1000&memo=OrderId12345



6. Ecosystem Value
Enhance ICP's competitiveness in the payment sector, attracting more merchants and users.
Strengthen the connection between ICP and real-world applications, promoting mainstream adoption.
Reduce technical costs for developers and merchants while improving user experience.
