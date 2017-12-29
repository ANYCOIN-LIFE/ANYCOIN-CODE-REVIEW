# ANYCOIN-CODE-REVIEW

##### by [Ryu, Mun Hyung](pfofile-ryumunhyung.md)

## SYSTEM AND METHOD FOR ELECTRONIC MONEY TRANSACTION

### Index
- [Technical Field](#technical-field)
- [Background Art](#background-art)
- [Technical Approach](#technical-approach)
- [Technical Problem](#technical-problem)
- [Advantageous Effects](#advantageous-effects)
- [Description of Code Definitions](#description-of-drawings)
- [Best Modes](#best-modes)

##### Technical Field
The present technical elements in the ANYCOIN PCT relates to a transaction method using electronic money and, more particularly, to a system and method for electronic money transaction, capable of preventing an error which may occur during a process of generating a block chain and strengthening security regarding transactional information of electronic money, while allowing electronic money users to directly exchange real money.

##### Background Art
In the conventional system for transaction using the electronic money forming the block chain, transactions may beperformed only when a seller who wants to sell electronic money and a purchaser who wants to purchase electronic money open an electronic wallet.  To this end, a user who wants to trade electronic money accesses an exchange server to open an electronic wallet and transfers real money to the exchange to purchase electronic money.  The exchange checks the transfer of the real money and subsequently transfers electronic money to an electronic wallet of the user who has purchased electronic money.  When a user wants to sell electronic money, he or she accesses the exchange server and subsequently transfers electronic money, and thereafter, a buyer purchases the transferred electronic money, whereby the real money is moved between the user and the purchaser. That is, the conventional electronic money exchange does not provide a direct exchange between electronic money and real money to the user, but serve to mediate transaction of electronic money between the seller and the purchaser.  Meanwhile, in the case of bit coin, which is a representative example of electronic money, one block is generated every about ten minutes.  Therefore, since it takes about 10 minutes for a next transaction to be verified after a previous transaction, the use of bit coin as electronic money in a short-time electronic commerce may cause a problem of hindering promptness of transaction.

Examples of transaction using bit coin may include Korean Patent Laid-Open No. 10-2016-0009301 (Payment agency service of private key-based electronic money and method thereof), Korean Patent Registration No. 10-1628007 (Transaction system of digital virtual money having block chain between parties concerned, Korean Patent Registration No. 10-1628009 (Transaction system of digital virtual money having block chain between parties concerned).

However, the conventional technology does not provide direct exchange of electronic money and real money between exchanges and users, and there is a problem that it is difficult to perform an immediate transaction due to time (about 10 minutes) required for verifying a block.  In addition, electronic money such as bit coin supports transparency that all transaction details included in each block may be referred to or checked.  Therefore, a third party may check all transaction details included in each block.  In addition, since all the source codes of software including the principle of running a transaction system are open, all transactions may be observed transparently.  However, it may be difficult to provide security for transaction details to a company or a store who wants not to open transaction details through electronic money to the outside, among users participating in transactions using electronic money.

#### Technical Approach

##### Technical Problem
Therefore, an aspect of the present AnyCoin is to increase convenience of electronic money transaction by allowing a user to exchange between electronic money and real money directly in a store. In addition, another aspect of the present elements is to enhance security of transaction details between a user and a store by processing an address of the store to be non-public.

#### Advantageous Effects
According to the system and method for an electronic money transaction according to the embodiment of the present disclosure, since electronic money users may directly exchange electronic money with real money through an exchange server, an electronic money transaction procedure may be simplified.  In addition, since an address of a point-of-sale (POS) terminal is used as a virtual address, security of transaction details may be enhanced. In addition, by introducing a game-type electronic money mining process, interest of a user in the use of electronic money may be increased.  Also, since electronic money information is changed on the basis of transaction data confirmed in validity, an error that may occur in a process of generating a block chain may be prevented and security of transaction details of electronic money may be strengthened.

##### Description of Code Definitions
Here is a view illustrating an example of electronic money information in an electronic money transaction system electronic according to an embodiment of the present AnyCoin, in which [class EthereumCustomer](class-EthereumCustomer-5a.md) illustrates customer information of a user, [class Ethereum Account](class-EthereumAccount-5b.md) illustrates account information of a user, [class Ethereum Wallet](class-EthereumWallet-5c.md) illustrates wallet information of a user, and [class Ethereum Exchange(1)](class-EthereumExchange-5d.md) [class Ethereum Exchange(2)](class-EthereumExchangeLog-5d.md) illustrates an exchange rate of electronic money, and [class Ethereum Adjust Detail](class-EthereumAdjustDetail-5e.md) illustrates settlement information;

[Input data area](Input-data-area-6a.png) is a view illustrating a data structure for allocating a plurality of coins to one wallet in an electronic money transaction system according to an embodiment of the present AnyCoin;


##### Best Modes
[class Ethereum Customer](class-EthereumCustomer-5a.md) illustrates an example of customer information of the user, and class Ethereum Account and class Ethereum Wallet show examples of account information and wallet information, respectively.  class Ethereum Exchange and class Ethereum Adjust Detail respectively show examples of exchange rate information and payment information of electronic money, respectively.

Customer information may include a name of a customer, a customer type, a user ID, a password, a language, a country code, a phone number, an e-mail, a cell phone type, a date and time for subscription, a transaction store, bank and an account number, location information (latitude and longitude), and an affiliated group, and the like.  The account information may include the user’s account address and the account code.  The wallet information may include information such as customer ID, usage token and coin type, a wallet address, balance, and the like, based on the account code.  In the electronic money transaction system of the present disclosure, since a plurality of coins may be included and used in one wallet address, a plurality of pieces of coin information may be included in the wallet information.  The exchange rate information of the electronic money may include a classification code according to the kind of exchange and exchange rate information according to a specific date and time.


[Input Data Area](Input-data-area-6a.png) illustrates an example of a data structure for assigning a plurality of coins to one wallet in an electronic money transaction system according to an embodiment of the present disclosure, and FIG. 6B illustrates an example of a case where a plurality of coins are allocated to one wallet.

Referring to [Input Data Area](Input-data-area-6a.png), a data block of electronic money such as Ethereum, includes an input data area in which a plurality of coin addresses may be allocated to one wallet address.  To a field of
[0] in the input data area of [Input Data Area](Input-data-area-6a.png), a plurality of coin addresses allocated to the user's wallet address may be allocated.  As for the plurality of coins allocated in this manner, data such as a wall address, a coin value, and the like, corresponding to the plurality of allocated coins may be recorded in fields of [3] to [6].  In case where a plurality of coils are allocated to one wallet as illustrated in [Input Data Area](Input-data-area-6a.png), the user may check the plurality of pieces of allocated coin information.  Accordingly, in the electronic money transaction system of the present AnyCoin, since various kinds of coins are allocated to one wallet address, the wall may be conveniently managed in using a plurality of coins and electronic money may be effectively traded.
