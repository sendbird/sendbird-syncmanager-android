## Change Log

### v1.1.28 (Nov 03, 2020) with Core SDK `v3.0.150`

* Added `MessageCollection#deleteMessageByRequestId` and `MessageCollection#deleteMessageByMessageId`.

### v1.1.27 (Oct 20, 2020) with Core SDK `v3.0.149`

* Fixed a bug in `FailedMessageDispatcher` caused by a timing issue. 
* Fixed a bug in `ChannelCollection` caused by a timing issue.

### v1.1.26 (Sep 29, 2020) with Core SDK `v3.0.147`

* Added `MessageCollection#fetchPendingMessages`.
* Sendbird Core SDK is now embedded in the SyncManager.

### v1.1.24 (Sep 11, 2020)
* Prevent duplicate message being inserted in `MessageCollection`.
* Improved stability.

### v1.1.23 (Sep 8, 2020)
* Fixed `MessageCollectionHandler.onNewMessage` not being fired in certain situations when receiving a new message.

### v1.1.22 (Jul 29, 2020)
* Fixed `MessageCollectionHandler.onSucceededMessageEvent()` not being called in some cases when failed message resend is successful.
* Improved stability.

### v1.1.21 (Jun 25, 2020)
* Changed resending failed messages job to be thread-safe.
* Improved stability.

### v1.1.20 (May 13, 2020)
* Added SyncManager version information to User-Agent
* Improved stability.

### v1.1.19 (Apr 1, 2020)
* Changes made to `SendBirdSyncManager.Options.AutomaticMessageResendRetryCount`.
  * Changed it's default value to 10.
  * The value should be in between 1 to 50, inclusive.
* Improved stability.

### v1.1.18 (Feb 5, 2020)
* Improved stability.

### v1.1.17 (Dec 17, 2019)
* Improved stability.

### v1.1.16 (Dec 13, 2019)
* Improved stability.

### v1.1.15 (Dec 6, 2019)
* Improved stability.

### v1.1.14 (Dec 4, 2019)
* Added features that supports fetching messages.
   * Added `fetchAllNextMessages()` in `MessageCollection` to fetch all new `SucceededMessage` in local database.
   * Added `FetchCompletionHandler(boolean hasMore, SendBirdException e)` to use in `fetchSucceededMessages()`, with flag whether there's more data to fetch.
* Improved stability.

### v1.1.13 (Nov 29, 2019)
* Improved stability.

### v1.1.12 (Nov 27, 2019)
* Improved stability.

### v1.1.11 (Nov 25, 2019)
* Improved stability.

### v1.1.10 (Nov 15, 2019)
* Improved stability.

### v1.1.8 (Nov 8, 2019)
* Improved stability.

### v1.1.7 (Oct 17, 2019)
* Improved stability.

### v1.1.6 (Oct 8, 2019)
* Improved stability.

### v1.1.5 (Oct 7, 2019)
* Improved stability.

### v1.1.4 (Sep 6, 2019)
* Improved stability.

### v1.1.3 (Aug 2, 2019)
* Added features that supports storing and resending messages which `RequestState` is `FAILED`.
   * Added `fetchFailedMessages()` in `MessageCollection` to fetch `FailedMessage` in local database.
   * Added `fetchSucceededMessages()` in `MessageCollection` to fetch `SucceededMessage` in local database.
   * Deprecated `fetch()` in `MessageCollection`. It is replaced by `fetchSucceededMessages()`.
   * Added `onFailedMessageEvent()` in `MessageCollectionHandler` to to notify events of messages which `RequestState` is `FAILED`.
   * Added `onSucceededMessageEvent()` in `MessageCollectionHandler` to notify events of messages which `RequestState` is `SUCCEEDED`.
   * Added `onPendingMessageEvent()` in `MessageCollectionHandler` to notify events of messages which `RequestState` is `PENDING`.
   * Added `onNewMessage()` in `MessageCollectionHandler` to notify new message's creation.
   * Deprecated `onMessageEvent()` in `MessageCollectionHandler`. It is replaced by `onSucceededMessageEvent()` and `onPendingMessageEvent()`.
* Added properties used for configuring `SendBirdSyncManager` in `SendBirdSyncManager.Options`.
   * Added `SendBirdSyncManager.Options.Builder` to build `SendBirdSyncManager.Options`.
   * Added `ThreadOption` and `setThreadOption()` in `SendBirdSyncManager.Options`.
   * Added `setMaxFailedMessageCountPerChannel()` in `SendBirdSyncManager.Options.Builder` to configure maximum count of failed messages one `GroupChannel` can store.
   * Added `setFailedMessageRetentionDays()` in `SendBirdSyncManager.Options.Builder` to configure retention days of failed messages.
   * Added `setAutomaticMessageResendRetryCount()` in `SendBirdSyncManager.Options.Builder` to configure resending retry count.
* Added `AUTOMATIC` to `MessageResendPolicy` to support resending failed messages automatically.
* Improved stability.
   
### v1.1.2 (Jun 7, 2019)
* Added `SendBirdSyncManager.Options` which is used for message count limit of `MessageCollection` and message resend policy.
* Added `handleSendMessageResponse()` in `MessageCollection` to support resend failed message.

### v1.1.1 (Apr 2, 2019)
* Improved stability.

### v1.1.0 (Mar 19, 2019)
* Added channel full synchronization support.
* Improved stability.

### v1.0.2 (Feb 27, 2019)
* Fixed minor bug.

### v1.0.1 (Feb 19, 2019)
* Fixed minor bug.

### v1.0.0 (Feb 8, 2019)
* First release.
