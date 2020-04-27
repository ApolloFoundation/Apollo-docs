APOLLO API V.1.0
================

23.04.2020

General Information
-------------------

The Apollo API allows interaction with Apollo nodes using HTTP requests to port
7876. Most HTTP requests can use either the GET or POST methods, but some API
calls accept only the POST method for security reasons. Responses are returned
as JSON objects.

All API calls can be viewed and tested at <http://localhost:7876/test> while the
local server node is running. For specific API calls,
use <http://localhost:7876/test?requestType=>*specificRequestType*.

This document corresponds to APL Software Version 1.0.4.

Accounts
--------

### deleteAccountProperty

Deletes an account property.

**Request:**

Names of the property for deletion are as follows:

-   recipient

-   property

-   setter

-   secretPhrase

-   publicKey

-   feeATM

-   deadline

-   referencedTransactionFullHash

-   broadcast

-   message

-   messageIsText

-   messageIsPrunable

-   messageToEncrypt

-   messageToEncryptIsText

-   encryptedMessageData

-   encryptedMessageNonce

-   encryptedMessageIsPrunable

-   compressMessageToEncrypt

-   messageToEncryptToSelf

-   messageToEncryptToSelfIsText

-   encryptToSelfMessageData

-   encryptToSelfMessageNonce

-   compressMessageToEncryptToSelf

-   phased

-   phasingFinishHeight

-   phasingVotingModel

-   phasingQuorum

-   phasingMinBalance

-   phasingHolding

-   phasingMinBalanceModel

-   phasingWhitelisted

-   phasingWhitelisted

-   phasingWhitelisted

-   phasingLinkedFullHash

-   phasingLinkedFullHash

-   phasingLinkedFullHash

-   phasingHashedSecret

-   phasingHashedSecretAlgorithm

-   recipientPublicKey

-   ecBlockId

-   ecBlockHeight

-   sender

-   passphrase

-   code2FA

**Response:** JSON response

### deleteScheduledTransaction

\#Description

**Request parameters:**

-   transaction

-   adminPassword

**Response:** JSON response

### getAccountCurrentAskOrders

Get current asset orders

**Request parameters:**

-   account

-   asset

-   firstIndex

-   lastIndex

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getAccountCurrentBidOrderIds

Get current asset orders

**Request parameters:**

-   account

-   asset

-   firstIndex

-   lastIndex

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getAccountCurrentBidOrders

Get current asset orders

**Request parameters:**

-   account

-   asset

-   firstIndex

-   lastIndex

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getAccountExchangeRequests

Get the exchange requests associated with a given account and/or currency in
reverse chronological order (or in expected order of execution for expected
requests).

**Request parameters:**

-   account

-   currency

-   includeCurrencyInfo

-   firstIndex

-   lastIndex

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getAccountId

Get an account ID given a secret passphrase or public key.

**Request parameters:**

-   secretPhrase

-   publicKey

**Response:** JSON response

### getAccountLedger

Get multiple account ledger entries.

**Request parameters:**

-   account

-   firstIndex

-   lastIndex

-   eventType

-   event

-   holdingType

-   holding

-   includeTransactions

-   includeHoldingInfo

-   adminPassword

-   requireBlock

-   requireLastBlock:

**Response:** JSON response

### getAccountLedgerEntry

Get a specific account ledger entry.

**Request parameters:**

-   ledgerId

-   includeTransaction

-   includeHoldingInfo

**Response:** JSON response

### getAccountLessors

Get the lessors to an account.

**Request parameters:**

-   account

-   height

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getAccountPhasedTransactionCount

Get the number of pending phased transactions associated with an account given
the account ID.

**Request parameters:**

-   account

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getAccountPhasedTransactions

Get pending phased transactions associated with an account given the account ID
in reverse chronological creation order.

**Request parameters:**

-   account

-   firstIndex

-   lastIndex

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getAccountProperties

Get the Account properties for a specific account or setter.

**Request parameters:**

-   recipient

-   property

-   setter

-   firstIndex

-   lastIndex

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getAccountPublicKey

Get the public key associated with an account ID.

**Request parameters:**

-   account

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getAssetsByIssuer

Get asset information given multiple creation account IDs in reverse block
height of creation order.

**Request parameters:**

-   account

-   account

-   account

-   firstIndex

-   lastIndex

-   includeCounts

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getBalance

Get the balance of an account.

**Request parameters:**

-   account

-   includeEffectiveBalance

-   height

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getBlockchainTransactions

Get the transactions associated with an account in reverse block timestamp
order.

Returns only public transactions (private transactions dont be returned!) to get
all transactions use Get Private Blockchain Transactions.

**Request parameters:**

-   account

-   timestamp

-   type

-   subtype

-   firstIndex

-   lastIndex

-   numberOfConfirmations

-   withMessage

-   phasedOnly

-   nonPhasedOnly

-   includeExpiredPrunable

-   includePhasingResult

-   executedOnly

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getChatHistory

\#TODO

**Request parameters:**

-   account1

-   account2

-   firstIndex

-   lastIndex

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getChats

\#TODO

**Request parameters:**

-   account

-   firstIndex

-   lastIndex

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getCurrenciesByIssuer

Get currencies issued by multiple accounts in reverse creation order.

**Request parameters:**

-   account

-   account

-   account

-   firstIndex

-   lastIndex

-   includeCounts

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getExpectedExchangeRequests

Get the exchange requests associated with a given account and/or currency in
reverse chronological order (or in expected order of execution for expected
requests).

**Request parameters:**

-   account

-   currency

-   includeCurrencyInfo

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getFundingMonitor

Get a funding monitor.

**Request parameters:**

-   holdingType

-   holding

-   property

-   secretPhrase

-   includeMonitoredAccounts

-   account

-   adminPassword

-   account

-   passphrase

**Response:** JSON response

### getGenesisBalances

**Request parameters:**

-   firstIndex

-   lastIndex

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getGuaranteedBalance

Get the balance of an account that is confirmed at least a specified number of
times.

**Request parameters:**

-   account

-   numberOfConfirmations

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getPolls

Get poll details in reverse creation order.

**Request parameters:**

-   account

-   firstIndex

-   lastIndex

-   timestamp

-   includeFinished

-   finishedOnly

-   adminPassword

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### getPrivateAccountLedger

Get a list of ALL ledger entries for given *secretPhrase* (not recommended, no
private ledger entries encryption, for localhost only) or *publicKey*
(recommended, encrypted private ledger entries, security provided for remote
servers) including private ledger entries.

**Request parameters:**

-   firstIndex

-   lastIndex

-   eventType

-   event

-   holdingType

-   holding

-   includeTransactions

-   includeHoldingInfo

-   secretPhrase

-   publicKey

-   adminPassword

-   requireBlock

-   requireLastBlock

-   account

-   passphrase

**Response:** JSON response

### getPrivateAccountLedgerEntry

Get only ONE private ledger entry by *ledgerId* for given *secretPhrase* (not
recommended, no private ledger entry encryption, for localhost only) or
*publicKey* (recommended, encrypted private ledger entry, security provided for
remote servers).

**Request parameters:**

-   ledgerId

-   includeTransaction

-   includeHoldingInfo

-   secretPhrase

-   publicKey

-   account

-   passphrase

**Response:** JSON response

### getPrivateBlockchainTransactions

Get a List of all transactions for user with given *secretPhrase* (private
transactions will be encrypted if publicKey provided and not encrypted when
*secretPhrase* provided (for localhost usage only!)

**Request parameters:**

-   a

**Response:** JSON response

### getPrivateUnconfirmedTransactions

Get a List of all unconfirmed transactions for user with given *secretPhrase*
(not recommended, no transaction encryption, for localhost only) or *publicKey*
(recommended, encrypted transaction, security provided for remote servers)
including private unconfirmed transactions.

**Request parameters:**

-   a

**Response:** JSON response

### getScheduledTransactions

**Request parameters:**

-   a

**Response:** JSON response

### getUnconfirmedTransactionIds

Get a list of unconfirmed transaction IDs associated with an account.

**Request parameters:**

-   a

**Response:** JSON response

### getUnconfirmedTransactions

Get a list of unconfirmed transactions associated with an account.

Returns only public unconfirmed transactions\_ (private unconfirmed transactions
dont be returned!) to get all unconfirmed transactions use
GetPrivateUnconfirmedTransactions.

**Request parameters:**

-   a

**Response:** JSON response

### getVotedAccountPolls

**Request parameters:**

-   a

**Response:** JSON response

### getVoterPhasedTransactions

Get pending phased transactions which include a whitelist in reverse
chronological creation order. These transactions can be considered transaction
approval requests.

**Request parameters:**

-   a

**Response:** JSON response

### searchAccounts

Get accounts having a name or description that match a given query in reverse
relevance order.

**Request parameters:**

-   a

**Response:** JSON response

### sendMoney

Send APL to an account. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### sendMoneyPrivate

Sends Private Payment transaction and returns created transaction.

POST only.

**Request parameters:**

-   a

**Response:** JSON response

### setAccountInfo

Set account information. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### setAccountProperty

Set account property. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### startFundingMonitor

Starts a funding monitor that will transfer APL, ASSET or CURRENCY from the
funding account to a recipient account when the amount held by the recipient
account drops below the threshold. The transfer will not be done until the
current block height is greater than equal to the block height of the last
transfer plus the interval. The funding account is identified by the secret
phrase.

The recipient accounts are identified by the specified account property (see Set
Account Property). Each account that has this property set by the funding
account will be monitored for changes. The property value can be omitted or it
can consist of a JSON string containing one or more values in the format:
{"amount":long,"threshold":long,"interval":integer} . POST only.

**Request parameters:**

-   a

**Response:** JSON response

### stopFundingMonitor

Stop a funding monitor. When the secret phrase is specified, a single monitor
will be stopped. The monitor is identified by the secret phrase, holding and
account property. The administrator password is not required and will be
ignored.

When the administrator password is specified, a single monitor can be stopped by
specifying the funding account, holding and account property. If no account is
specified, all monitors will be stopped.

The holding type and account property name must be specified when the secret
phrase or account is specified. Holding type codes are listed in getConstants.
In addition, the holding identifier must be specified when the holding type is
ASSET or CURRENCY. POST only.

**Request:**

**Response:** JSON response

### getAllPhasingOnlyControls

Retrieve all accounts subject to phasing control with their respective
restrictions.

**Request parameters:**

-   a

**Response:** JSON response

### getPhasingOnlyControl

Retrieve phasing control with their respective restrictions for a specific
account.

**Request parameters:**

-   a

**Response:** JSON response

### importKey

**Request parameters:**

-   a

**Response:** JSON response

### leaseBalance

Lease the entire guaranteed balance of APL to another account, after 1440
confirmations. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### setPhasingOnlyControl

Sets (or removes) phasing control for a specific account. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### buyAlias

Buy an alias. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### deleteAlias

Delete an alias given an alias ID or name. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### getAlias

Get information about a given alias

**Request parameters:**

-   a

**Response:** JSON response

### getAliasCount

Get the number of aliases owned by an account given the account ID.

**Request parameters:**

-   a

**Response:** JSON response

### getAliases

Get information on aliases owned by a given account in alias name order.

**Request parameters:**

-   a

**Response:** JSON response

### getAliasesLike 

**Request parameters:**

-   a

**Response:** JSON response

### sellAlias

Sell an alias. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### setAlias

Create and/or assign an alias. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### cancelAskOrder

Cancel an existing asset order. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### cancelBidOrder

Cancel an existing asset order. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### deleteAssetShares

Permanently deletes a specified quantity of owned asset shares.

**Request parameters:**

-   a

**Response:** JSON response

### dividendPayment

Pay dividend to all shareholders of an asset. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### getAllAssets

Get all assets in the exchange in reverse block height of creation order.

**Request parameters:**

-   a

**Response:** JSON response

### getAllOpenAskOrders

Get all open bid/ask orders in reverse block height order.

**Request parameters:**

-   a

**Response:** JSON response

### getAllOpenBidOrders

Get all open bid/ask orders in reverse block height order.

**Request parameters:**

-   a

**Response:** JSON response

### getAllTrades

Get all trades since a given timestamp in reverse block height order.

**Request parameters:**

-   a

**Response:** JSON response

### getAskOrder

Get an ask order given an order ID.

**Request parameters:**

-   a

**Response:** JSON response

### getAskOrderIds

Get ask order IDs given an asset ID, in order of decreasing bid price or
increasing ask price.

**Request parameters:**

-   a

**Response:** JSON response

### getAskOrders

Get ask orders given an asset ID, in order of decreasing bid price or increasing
ask price (if *sortByPrice* is *true* for expected orders, otherwise in the
expected order of execution).

**Request parameters:**

-   a

**Response:** JSON response

### getAsset

Get asset information given an asset ID.

**Request parameters:**

-   a

**Response:** JSON response

### getAssetAccountCount

Get the number of accounts that own an asset given the asset ID.

**Request parameters:**

-   a

**Response:** JSON response

### getAssetAccounts

Get the accounts that own an asset given the asset ID in reverse quantity order.

**Request parameters:**

-   a

**Response:** JSON response

### getAssetDeletes

Get asset deletions for a specific asset or account.

**Request parameters:**

-   a

**Response:** JSON response

### getAssetDividends

Get the dividend payment history for a specific asset.

**Request parameters:**

-   a

**Response:** JSON response

### getAssetIds

Get the IDs of all assets in the exchange in reverse block height of creation
order.

**Request parameters:**

-   a

**Response:** JSON response

### getAssetPhasedTransactions

Get pending phased transactions based on an asset in reverse chronological
creation order. These transactions can be considered transaction approval
requests.

**Request parameters:**

-   a

**Response:** JSON response

### getAssetTransfers

Get transfers associated with a given asset and/or account in reverse block
height order (or in the expected order of execution for expected transfers).

**Request parameters:**

-   a

**Response:** JSON response

### getAssets

Get asset information given multiple asset IDs

**Request parameters:**

-   a

**Response:** JSON response

### getBidOrder

Get a bid order given an order ID.

**Request parameters:**

-   a

**Response:** JSON response

### getBidOrderIds

Get bid order IDs given an asset ID, in order of decreasing bid price or
increasing ask price.

**Request parameters:**

-   a

**Response:** JSON response

### getBidOrders

Get bid orders given an asset ID, in order of decreasing bid price or increasing
ask price (if *sortByPrice* is *true* for expected orders, otherwise in the
expected order of execution).

**Request parameters:**

-   a

**Response:** JSON response

### getExpectedAskOrders

Get bid orders given an asset ID, in order of decreasing bid price or increasing
ask price (if *sortByPrice* is *true* for expected orders, otherwise in the
expected order of execution).

**Request parameters:**

-   a

**Response:** JSON response

### getExpectedAssetDeletes

Gets asset deletes which are expected to be executed in the next block.

**Request parameters:**

-   a

**Response:** JSON response

### getExpectedAssetTransfers

Get transfers associated with a given asset and/or account in reverse block
height order (or in the expected order of execution for expected transfers).

**Request parameters:**

-   a

**Response:** JSON response

### getExpectedBidOrders

Get bid orders given an asset ID, in order of decreasing bid price or increasing
ask price (if *sortByPrice* is *true* for expected orders, otherwise in the
expected order of execution).

**Request parameters:**

-   a

**Response:** JSON response

### getExpectedOrderCancellations

Get all expected order cancellations in the order in which they are expected to
be executed.

**Request parameters:**

-   a

**Response:** JSON response

### getLastTrades

Get the last trade of each of multiple assets.

**Request parameters:**

-   a

**Response:** JSON response

### getOrderTrades

Get all trades that were executed as a result of a
given *askOrder* and/or *bidOrder* in reverse block height order.

**Request parameters:**

-   a

**Response:** JSON response

### getTrades

Get trades associated with a given asset and/or account in reverse block height
order.

**Request parameters:**

-   a

**Response:** JSON response

### issueAsset

Create an asset on the exchange. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### placeAskOrder

Place an asset order. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### placeBidOrder

Place an asset order. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### searchAssets

Get assets having a name or description that match a given query in reverse
relevance order.

**Request parameters:**

-   a

**Response:** JSON response

### transferAsset

Transfer a quantity of an asset from one account to another. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### getBlock

Get a block object given a block ID or block height.

If includeTransactions is true - includes private transactions with masked
amount, recipient and sender.

**Request parameters:**

-   a

**Response:** JSON response

### getBlockId

Get a block ID given a block height.

**Request parameters:**

-   a

**Response:** JSON response

### getBlocks

Get blocks from the blockchain in reverse block height order.

If includeTransactions is true - includes private transactions with masked
amount, recipient and sender.

**Request parameters:**

-   a

**Response:** JSON response

### getECBlock

Get Economic Cluster block data.

**Request parameters:**

-   a

**Response:** JSON response

### approveTransaction

Approve (vote for) a phased transaction. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### castVote

**Request parameters:**

-   a

**Response:** JSON response

### createPoll

Cast a vote on a poll. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### currencyBuy

Make an exchange request to buy an exchangeable currency. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### currencyMint

Submit a valid computed nonce to the blockchain in return for newly minted
currency. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### currencyReserveClaim

Claim currency reserve. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### currencyReserveIncrease

Increase the currency reserve of an unissued reservable currency. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### currencySell

Make an exchange request to sell an exchangeable currency. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### deleteCurrency

Delete a deletable currency (see Can Delete Currency). POST only.

**Request parameters:**

-   a

**Response:** JSON response

### dgsDelisting

Delist a listed product. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### dgsDelivery

Deliver a product. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### dgsFeedback

Give feedback about a purchased product after delivery. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### dgsListing

List a product in the DGS by creating a listing transaction. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### dgsPriceChange

Change the price of a listed product. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### dgsPurchase

Purchase a product for sale. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### dgsQuantityChange

Change the quantity of a listed product. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### dgsRefund

Refund a purchase. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### extendTaggedData

Extend the expiration time of already uploaded tagged data. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### issueCurrency

Issue a new currency or re-issue an existing currency with different properties.
POST only.

**Request parameters:**

-   a

**Response:** JSON response

### publishExchangeOffer

Publish an exchange offer for an exchangeable currency. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### scheduleCurrencyBuy

**Request parameters:**

-   a

**Response:** JSON response

### sendMessage

Create an Arbitrary Message transaction. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### sendUpdateTransaction

**Request parameters:**

-   a

**Response:** JSON response

### shufflingCancel

Cancels a shuffling

**Request parameters:**

-   a

**Response:** JSON response

### shufflingCreate

Creates a new shuffling.

**Request parameters:**

-   a

**Response:** JSON response

### shufflingProcess

Manually process the shuffling for a specific participant. Note that the
shuffling must be in processing stage and the *secretPhrase* must match the
current shuffling assignee.

**Request parameters:**

-   a

**Response:** JSON response

### shufflingRegister

Registers a new participant to an existing shuffling. The shuffling must be in
stage registration.

**Request parameters:**

-   a

**Response:** JSON response

### shufflingVerify

Sends a verification that an account's recipient public key is found within a
shuffling.

**Request parameters:**

-   a

**Response:** JSON response

### transferCurrency

Transfer currency to a given recipient. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### uploadTaggedData

Upload and broadcast new tagged data. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSExpiredPurchases

Get purchase orders which have expired without being delivered, given a seller
ID, in reverse chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSGood

Get a DGS product given a goods ID.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSGoods

Get DGS products for sale in reverse chronological listing creation order unless
a seller is given, then in product name order.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSGoodsCount

Get the number of products for sale by a given seller or all sellers.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSGoodsPurchaseCount

Get the number of completed purchase orders given a goods ID.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSGoodsPurchases

Get completed purchase orders given a goods ID and optionally a buyer ID in
reverse chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSPendingPurchases

Get pending purchase orders given a seller ID in reverse chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSPurchase

Get a purchase order given a purchase order ID.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSPurchaseCount

Get the number of purchase orders given a seller and/or buyer ID, or all orders
combined.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSPurchases

Get purchase orders given a seller and/or buyer ID in reverse chronological
order.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSTagCount

Get the number of tags used by all sellers.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSTags

Get tags used by all sellers in reverse *inStockCount*,
reverse *totalCount*, *tag* order.

**Request parameters:**

-   a

**Response:** JSON response

### getDGSTagsLike

Get all tags starting with a given prefix (at least 2 characters long) in
reverse *inStockCount*, reverse *totalCount*, *tag* order.

**Request parameters:**

-   a

**Response:** JSON response

### searchDGSGoods

Get product listings that have a name or description that match a given query in
reverse relevance order, then name order (given a seller), then reverse
chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getForging

Check to see if an account is forging. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### getNextBlockGenerators

Returns the next block generators ordered by hit time. The list of currently
active forgers is first initialized using the block generators with at least 2
blocks generated within the previous 10,000 blocks, excluding accounts without a
public key. The list is updated as new blocks are processed. The results are not
100% correct since previously active generators may no longer be running and new
generators won't be known until they generate a block.

**Request parameters:**

-   a

**Response:** JSON response

### startForging

Start forging with an account. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### stopForging

Stop forging with an account. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### decryptFrom

Decrypt an AES-encrypted message.

**Request parameters:**

-   a

**Response:** JSON response

### downloadPrunableMessage

Downloadins a prunable message attachments directly as binary data. An optional
secretPhrase parameter is supported, to allow decryption and downloading of the
encrypted part of the message instead of the plain text part.

**Request parameters:**

-   a

**Response:** JSON response

### encryptTo

Encrypt a message using AES without sending it.

**Request parameters:**

-   a

**Response:** JSON response

### getAllPrunableMessages

Get all available prunable messages in reverse block timestamp order.

**Request parameters:**

-   a

**Response:** JSON response

### getPrunableMessage

Get the prunable message given a transaction ID, optionally decrypting it if
encrypted and if a secretPhrase is provided, if it is still available.

**Request parameters:**

-   a

**Response:** JSON response

### getPrunableMessages

Get all still-available prunable messages given an account id, optionally
limiting to only those with another account as recipient or sender, in reverse
chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getSharedKey

Get the one-time shared key used for encryption of messages.

**Request parameters:**

-   a

**Response:** JSON response

### readMessage

Get a message given a transaction ID.

**Request parameters:**

-   a

**Response:** JSON response

### verifyPrunableMessage

Verify that a prunable message obtained from any source, when hashed, matches
the hash of the original prunable message.

**Request parameters:**

-   a

**Response:** JSON response

### canDeleteCurrency

Determine if a currency can be deleted.

**Request parameters:**

-   a

**Response:** JSON response

### getAllCurrencies

Get all currencies in reverse creation order.

**Request parameters:**

-   a

**Response:** JSON response

### getAllExchanges

Get all currency exchanges in reverse chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getAvailableToBuy

Calculates the rate required in order to completely fill an exchange request.

**Request parameters:**

-   a

**Response:** JSON response

### getAvailableToSell

Calculates the rate required in order to completely fill an exchange request.

**Request parameters:**

-   a

**Response:** JSON response

### getBuyOffers

Get currency buy offers given a currency ID and/or an account ID in order of
rate (if *sortByRate* is *true* for expected offers, otherwise in the expected
order of execution).

**Request parameters:**

-   a

**Response:** JSON response

### getCurrencies

Get currencies given multiple currency IDs.

**Request parameters:**

-   a

**Response:** JSON response

### getCurrency

Get the details of a currency.

**Request parameters:**

-   a

**Response:** JSON response

### getCurrencyAccountCount

Get the number of accounts that hold a given currency

**Request parameters:**

-   a

**Response:** JSON response

### getCurrencyAccounts

Get the accounts that hold a given currency in reverse units order.

**Request parameters:**

-   a

**Response:** JSON response

### getCurrencyFounders

Get a reservable currency's founders.

**Request parameters:**

-   a

**Response:** JSON response

### getCurrencyIds

Get all currency IDs in reverse chronological creation order.

**Request parameters:**

-   a

**Response:** JSON response

### getCurrencyPhasedTransactions

Get pending phased transactions based on a currency in reverse chronological
creation order. These transactions can be considered transaction approval
requests.

**Request parameters:**

-   a

**Response:** JSON response

### getCurrencyTransfers

Get currency transfers given a currency ID and/or an account ID in reverse block
height order (or in expected order of execution for expected transfers).

**Request parameters:**

-   a

**Response:** JSON response

### getExchanges

Get currency exchanges given a currency and/or an account in reverse
chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getExchangesByExchangeRequest

Get currency exchanges given an exchange request transaction ID in reverse
chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getExchangesByOffer

**Request parameters:**

-   a

**Response:** JSON response

### getExpectedBuyOffers

Get currency exchanges given a currency offer ID in reverse chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getExpectedCurrencyTransfers

Get currency transfers given a currency ID and/or an account ID in reverse block
height order (or in expected order of execution for expected transfers).

**Request parameters:**

-   a

**Response:** JSON response

### getExpectedSellOffers

Get currency sell offers given a currency ID and/or an account ID in order of
rate (if *sortByRate* is *true* for expected offers, otherwise in the expected
order of execution).

**Request parameters:**

-   a

**Response:** JSON response

### getLastExchanges

Get the last exchange of each of multiple currencies.

**Request parameters:**

-   a

**Response:** JSON response

### getMintingTarget

Get the current minting target of a mintable currency.

**Request parameters:**

-   a

**Response:** JSON response

### getOffer

Get offer details given an offer ID.

**Request parameters:**

-   a

**Response:** JSON response

### getSellOffers

Get currency sell offers given a currency ID and/or an account ID in order of
rate (if *sortByRate* is *true* for expected offers, otherwise in the expected
order of execution).

**Request parameters:**

-   a

**Response:** JSON response

### searchCurrencies

Get currencies having a code that matches a given query in reverse relevance
order.

**Request parameters:**

-   a

**Response:** JSON response

### getLinkedPhasedTransactions

Gets the phased transactions with by-transaction voting model for a given
linkedFullHash, regardless of their phasing status (pending, approved or
rejected). Since the corresponding table is trimmed after finish height however,
the result will not include those transactions that finished before the last
trimming height.

**Request parameters:**

-   a

**Response:** JSON response

### getPhasingPoll

Get the details of a phasing poll.

**Request parameters:**

-   a

**Response:** JSON response

### getPhasingPollVote

Get a cast phasing poll vote given a phased transaction ID and an account ID of
a voter, if it is still available.

**Request parameters:**

-   a

**Response:** JSON response

### getPhasingPollVotes

Get all cast phasing poll votes in a phasing poll given a phased transaction ID,
if they are still available.

**Request parameters:**

-   a

**Response:** JSON response

### getPhasingPolls

Get phasing poll details given multiple phased transaction IDs.

**Request parameters:**

-   a

**Response:** JSON response

### getDataTagsLike

Prefix search of available data tags, return in alphabetical order.

**Request parameters:**

-   a

**Response:** JSON response

### searchPolls

Search for poll details given a name/description query string.

**Request parameters:**

-   a

**Response:** JSON response

### searchTaggedData

Full text search on available tagged data name, description and tags; optionally
filtered by tag, channel or uploading account; return in reverse relevance
order.

**Request parameters:**

-   a

**Response:** JSON response

### getAccountShufflings

Retrieves info about shufflings for a specific account.

**Request parameters:**

-   a

**Response:** JSON response

### getAllShufflings

Retrieves info about all shufflings.

**Request parameters:**

-   a

**Response:** JSON response

### getAssignedShufflings

Retrieves info about a shufflings that are currently assigned to a specific
account.

**Request parameters:**

-   a

**Response:** JSON response

### getHoldingShufflings

Retrieves info about shufflings for a specific holding and/or stage.

**Request parameters:**

-   a

**Response:** JSON response

### getShufflers

Retrieves info about active shufflers on the current node.

**Request parameters:**

-   a

**Response:** JSON response

### getShuffling

Retrieves info about a shuffling.

**Request parameters:**

-   a

**Response:** JSON response

### getShufflingParticipants

Retrieves info about participants in a shuffling.

**Request parameters:**

-   a

**Response:** JSON response

### startShuffler

Starts a automated Shuffler. Once started, the Shuffler monitors the blockchain
state for transactions relevant to the specified shuffle, and automatically
submits the required transactions on behalf of the user, performing shuffle
processing, verification, or cancellation as needed.

**Request parameters:**

-   a

**Response:** JSON response

### stopShuffler

Stops a previously started automated Shuffler.

**Request parameters:**

-   a

**Response:** JSON response

### detectMimeType

Gets the mime type of uploaded file or data.

**Request parameters:**

-   a

**Response:** JSON response

### downloadTaggedData

Download tagged data as a file if it is still available.

**Request parameters:**

-   a

**Response:** JSON response

### getAccountTaggedData

Get all available tagged data uploaded by a given account in reverse
chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getAllTaggedData

Get all available tagged data in reverse chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getChannelTaggedData

Get available tagged data by channel, optionally filtered by account, in reverse
chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### getDataTagCount

Get the total number of distinct available data tags.

**Request parameters:**

-   a

**Response:** JSON response

### getDataTags

Get the distinct tags of all available tagged data, with the number of uses of
each tag, in order of number of uses, then alphabetical order.

**Request parameters:**

-   a

**Response:** JSON response

### getTaggedData

Get available tagged data given a transaction ID.

**Request parameters:**

-   a

**Response:** JSON response

### getTaggedDataExtendTransactions

Retrieves all tagged data extend transactions for a given tagged data upload
transaction.

**Request parameters:**

-   a

**Response:** JSON response

### verifyTaggedData

Verify expired tagged data downloaded from another node, against the hash in the
blockchain.

**Request parameters:**

-   a

**Response:** JSON response

### decodeFileToken

Validate a file token without requiring the transmission of a secret passphrase.
POST only.

**Request parameters:**

-   a

**Response:** JSON response

### decodeHallmark

Decode a node hallmark.

**Request parameters:**

-   a

**Response:** JSON response

### decodeToken

Validate a token without requiring the transmission of a secret passphrase.

**Request parameters:**

-   a

**Response:** JSON response

### generateFileToken

Generate a file token. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### generateToken

Generate a token. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### markHost

Generates a node hallmark. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### broadcastTransaction

Broadcast a transaction to the network. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### calculateFullHash

Calculate the full hash of a transaction.

**Request parameters:**

-   a

**Response:** JSON response

### getAllTransactions

**Request parameters:**

-   a

**Response:** JSON response

### getElGamalPublicKey

**Request parameters:**

-   a

**Response:** JSON response

### getExpectedTransactions

Returns the non-phased unconfirmed transactions expected to be included in the
next block (only), plus the phased transactions scheduled to finish in that
block (whether approved or not).

**Request parameters:**

-   a

**Response:** JSON response

### getForgingPublicKey

**Request parameters:**

-   a

**Response:** JSON response

### getPrivateTransaction

Get only ONE private transaction by *transactionId* or *fullHash* for given
*secretPhrase* (not recommended, no transaction encryption, for localhost only)
or *publicKey* (recommended, encrypted transaction, security provided for remote
servers).

**Request parameters:**

-   a

**Response:** JSON response

### getReferencingTransactions

Gets the transactions referencing a given transaction id.

**Request parameters:**

-   a

**Response:** JSON response

### getTransaction

Get a transaction object given a transaction ID.

Returns unknown transaction if transaction with given hash or id is private.

**Request parameters:**

-   a

**Response:** JSON response

### getTransactionBytes

Get the bytecode of a transaction.

**Request parameters:**

-   a

**Response:** JSON response

### parseTransaction

Get a transaction object given a (signed or unsigned) transaction bytecode, or
re-parse a transaction object. Verify the signature

**Request parameters:**

-   a

**Response:** JSON response

### retrievePrunedTransaction

Force retrieval of the prunable data for a given transaction, even if past the
configured apl.maxPrunableLifetime.

**Request parameters:**

-   a

**Response:** JSON response

### sendTransaction

It broadcasts a transaction to the network without validating it, without
re-broadcasting it and without adding it locally as unconfirmed transaction.
Specially intended for roaming or light clients to send transactions to remote
peers. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### signTransaction

Calculates the full hash, signature hash, and transaction ID of an unsigned
transaction.

**Request parameters:**

-   a

**Response:** JSON response

### getPoll

Get the details of a poll.

**Request parameters:**

-   a

**Response:** JSON response

### getPollResult

Get the result of a poll.

**Request parameters:**

-   a

**Response:** JSON response

### getPollVote

Get a poll vote given a poll ID and an account ID.

**Request parameters:**

-   a

**Response:** JSON response

### getPollVotes

Get all votes on a poll in reverse chronological order.

**Request parameters:**

-   a

**Response:** JSON response

### clearUnconfirmedTransactions

Empties the unconfirmed transaction pool. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### dumpPeers

Get all active peers, optionally of a certain version or a minimum weight.

**Request parameters:**

-   a

**Response:** JSON response

### fullReset

Deletes the entire blockchain. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### getAllBroadcastedTransactions

Get unconfirmed transactions broadcasted from this node but not yet received
back from a peer, if transaction rebroadcasting is enabled.

**Request parameters:**

-   a

**Response:** JSON response

### getAllWaitingTransactions

Get unconfirmed transactions temporarily kept in memory during transaction
processing.

**Request parameters:**

-   a

**Response:** JSON response

### getLog

Get up to 100 of the most recent log messages from a memory buffer.

**Request parameters:**

-   a

**Response:** JSON response

### getStackTraces

Get the stack traces of the currently running threads in reverse *id* order.

**Request parameters:**

-   a

**Response:** JSON response

### luceneReindex

Forces a rebuild of the Lucene search index. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### popOff

Removes specified number of blocks (and associated transactions) from the top of
the blockchain. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### rebroadcastUnconfirmedTransactions

Rebroadcast transactions in the unconfirmed pool to peers, until received back
or found in the blockchain. Rebroadcasting can be disabled by setting
the *apl.enableTransactionRebroadcasting* property to *false*. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### requeueUnconfirmedTransactions

Requeue unconfirmed transactions. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### retrievePrunedData

Initiates a task of requesting and restoring missing prunable data. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### Scan

Scans the top of the blockchain. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### setLogging

Sets the log level and optionally specifies communication events to be logged,
without restarting the server. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### Shutdown

Shutdown the server. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### trimDerivedTables

Trigger a derived tables trim, and a prunable tables pruning. POST only.

**Request parameters:**

-   a

**Response:** JSON response

### getUpdateStatus

**Request parameters:**

-   a

**Response:** JSON response

### startAvailableUpdate

**Request parameters:**

-   a

**Response:** JSON response

### getPlugins

Get a list of all installed plugins on the server.

**Request parameters:**

-   a

**Response:** JSON response

### getConstants

Get all defined constants.

**Request parameters:**

-   a

**Response:** JSON response

### getTime

Get the current time.

**Request parameters:**

-   a

**Response:** JSON response

### getTotalSupply

**Request parameters:**

-   a

**Response:** JSON response

\#TODO
======

getServerInfo ??

importKeyStore ??

exportKeyStore ??

getAccountInfo ??

getEthWalletAmount ??

getEthWalletTransfer ??

getDexHistory

getDexOffers

getDexOrders

getDexWidthraw

getMyInfo

getPeer

addPeer

getPeers

getInboundPeers

blacklistPeer

blacklistAPIProxyPeer

setAPIProxyPeer
