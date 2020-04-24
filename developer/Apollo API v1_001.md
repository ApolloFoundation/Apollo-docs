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

### **deleteAccountProperty**

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

### **deleteScheduledTransaction**

\#Description

**Request parameters:**

-   transaction

-   adminPassword

**Response:** JSON response

### **getAccountCurrentAskOrders**

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

### **getAccountCurrentBidOrderIds**

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

### **getAccountCurrentBidOrders**

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

### **getAccountExchangeRequests**

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

### **getAccountId**

Get an account ID given a secret passphrase or public key.

**Request parameters:**

-   secretPhrase

-   publicKey

**Response:** JSON response

### **getAccountLedger**

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

### **getAccountLedgerEntry**

Get a specific account ledger entry.

**Request parameters:**

-   ledgerId

-   includeTransaction

-   includeHoldingInfo

**Response:** JSON response

### **getAccountLessors**

Get the lessors to an account.

**Request parameters:**

-   account

-   height

-   requireBlock

-   requireLastBlock

**Response:** JSON response

### **getAccountPhasedTransactionCount**

**Request parameters:**

-   a

**Response:** JSON response

### **getAccountPhasedTransactions**

**Request parameters:**

-   a

**Response:** JSON response

### **getAccountProperties**

**Request parameters:**

-   a

**Response:** JSON response

### **getAccountPublicKey**

### **getAssetsByIssuer**

### **getBalance**

### **getBlockchainTransactions**

### **getChatHistory**

### **getChats**

### **getCurrenciesByIssuer**

### **getExpectedExchangeRequests**

### **getFundingMonitor**

### **getGenesisBalances**

### **getGuaranteedBalance**

### **getPolls**

### **getPrivateAccountLedger**

### **getPrivateAccountLedgerEntry**

### **getPrivateBlockchainTransactions**

### **getPrivateUnconfirmedTransactions**

### **getScheduledTransactions**

### **getUnconfirmedTransactionIds**

### **getUnconfirmedTransactions**

### **getVotedAccountPolls**

### **getVoterPhasedTransactions**

### **searchAccounts**

### **sendMoney**

### **sendMoneyPrivate**

### **setAccountInfo**

### **setAccountProperty**

### **startFundingMonitor**

### **stopFundingMonitor**

**Request:**

**Response:** JSON response

getAllPhasingOnlyControls

getPhasingOnlyControl

importKey

leaseBalance

setPhasingOnlyControl

buyAlias

deleteAlias

getAlias

getAliasCount

getAliases

getAliasesLike

sellAlias

setAlias

cancelAskOrder

cancelBidOrder

deleteAssetShares

dividendPayment

getAccountCurrentAskOrders

getAccountCurrentBidOrderIds

getAccountCurrentBidOrders

getAllAssets

getAllOpenAskOrders

getAllOpenBidOrders

getAllTrades

getAskOrder

getAskOrderIds

getAskOrders

getAsset

getAssetAccountCount

getAssetAccounts

getAssetDeletes

getAssetDividends

getAssetIds

getAssetPhasedTransactions

getAssetTransfers

getAssets

getAssetsByIssuer

getBidOrder

getBidOrderIds

getBidOrders

getExpectedAskOrders

getExpectedAssetDeletes

getExpectedAssetTransfers

getExpectedBidOrders

getExpectedOrderCancellations

getLastTrades

getOrderTrades

getTrades

issueAsset

placeAskOrder

placeBidOrder

searchAssets

transferAsset

getBlock

getBlockId

getBlocks

getECBlock

approveTransaction

buyAlias

cancelAskOrder

cancelBidOrder

castVote

createPoll

currencyBuy

currencyMint

currencyReserveClaim

currencyReserveIncrease

currencySell

deleteAccountProperty

deleteAlias

deleteAssetShares

deleteCurrency

dgsDelisting

dgsDelivery

dgsFeedback

dgsListing

dgsPriceChange

dgsPurchase

dgsQuantityChange

dgsRefund

dividendPayment

extendTaggedData

issueAsset

issueCurrency

leaseBalance

placeAskOrder

placeBidOrder

publishExchangeOffer

scheduleCurrencyBuy

sellAlias

sendMessage

sendMoney

sendMoneyPrivate

sendUpdateTransaction

setAccountInfo

setAccountProperty

setAlias

setPhasingOnlyControl

shufflingCancel

shufflingCreate

shufflingProcess

shufflingRegister

shufflingVerify

transferAsset

transferCurrency

uploadTaggedData

dgsDelisting

dgsDelivery

dgsFeedback

dgsListing

dgsPriceChange

dgsPurchase

dgsQuantityChange

dgsRefund

getDGSExpiredPurchases

getDGSGood

getDGSGoods

getDGSGoodsCount

getDGSGoodsPurchaseCount

getDGSGoodsPurchases

getDGSPendingPurchases

getDGSPurchase

getDGSPurchaseCount

getDGSPurchases

getDGSTagCount

getDGSTags

getDGSTagsLike

searchDGSGoods

getForging

getGuaranteedBalance

getNextBlockGenerators

leaseBalance

startForging

stopForging

decryptFrom

downloadPrunableMessage

encryptTo

getAllPrunableMessages

getChatHistory

getChats

getPrunableMessage

getPrunableMessages

getSharedKey

readMessage

sendMessage

verifyPrunableMessage

canDeleteCurrency

currencyBuy

currencyMint

currencyReserveClaim

currencyReserveIncrease

currencySell

deleteCurrency

getAccountExchangeRequests

getAllCurrencies

getAllExchanges

getAvailableToBuy

getAvailableToSell

getBuyOffers

getCurrencies

getCurrenciesByIssuer

getCurrency

getCurrencyAccountCount

getCurrencyAccounts

getCurrencyFounders

getCurrencyIds

getCurrencyPhasedTransactions

getCurrencyTransfers

getExchanges

getExchangesByExchangeRequest

getExchangesByOffer

getExpectedBuyOffers

getExpectedCurrencyTransfers

getExpectedExchangeRequests

getExpectedSellOffers

getLastExchanges

getMintingTarget

getOffer

getSellOffers

issueCurrency

publishExchangeOffer

scheduleCurrencyBuy

searchCurrencies

transferCurrency

approveTransaction

getAccountPhasedTransactionCount

getAccountPhasedTransactions

getAssetPhasedTransactions

getCurrencyPhasedTransactions

getLinkedPhasedTransactions

getPhasingPoll

getPhasingPollVote

getPhasingPollVotes

getPhasingPolls

getVoterPhasedTransactions

getAliasesLike

getDGSTagsLike

getDataTagsLike

searchAccounts

searchAssets

searchCurrencies

searchDGSGoods

searchPolls

searchTaggedData

getAccountShufflings

getAllShufflings

getAssignedShufflings

getHoldingShufflings

getShufflers

getShuffling

getShufflingParticipants

shufflingCancel

shufflingCreate

shufflingProcess

shufflingRegister

shufflingVerify

startShuffler

stopShuffler

detectMimeType

downloadTaggedData

extendTaggedData

getAccountTaggedData

getAllTaggedData

getChannelTaggedData

getDataTagCount

getDataTags

getDataTagsLike

getTaggedData

getTaggedDataExtendTransactions

searchTaggedData

uploadTaggedData

verifyTaggedData

decodeFileToken

decodeHallmark

decodeToken

generateFileToken

generateToken

markHost

broadcastTransaction

calculateFullHash

deleteScheduledTransaction

getAllTransactions

getBlockchainTransactions

getElGamalPublicKey

getExpectedTransactions

getForgingPublicKey

getPrivateBlockchainTransactions

getPrivateTransaction

getPrivateUnconfirmedTransactions

getReferencingTransactions

getScheduledTransactions

getTransaction

getTransactionBytes

getUnconfirmedTransactionIds

getUnconfirmedTransactions

parseTransaction

retrievePrunedTransaction

sendTransaction

signTransaction

castVote

createPoll

getPoll

getPollResult

getPollVote

getPollVotes

getPolls

getVotedAccountPolls

searchPolls

clearUnconfirmedTransactions

dumpPeers

fullReset

getAllBroadcastedTransactions

getAllWaitingTransactions

getLog

getStackTraces

luceneReindex

popOff

rebroadcastUnconfirmedTransactions

requeueUnconfirmedTransactions

retrievePrunedData

scan

setLogging

shutdown

trimDerivedTables

getUpdateStatus

sendUpdateTransaction

startAvailableUpdate

getPlugins

getConstants

getTime

getTotalSupply

detectMimeType

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
