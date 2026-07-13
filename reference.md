# Reference
## Payments
<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">listPayments</a>({ ...params }) -> SuwardSDK.CryptopayListPaymentsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return a paginated list of the project's payments, newest first. Page and sort the results with the order, limit, and lastId query parameters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.listPayments();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.GetV1PaymentsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">createPayment</a>({ ...params }) -> SuwardSDK.CryptopayPaymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a payment request. Returns a unique, single-use deposit address and the amount to collect; the customer pays and you track progress via webhooks or polling. Pass externalId to make the call idempotent and dedupe retries.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.createPayment();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.CryptopayCreatePaymentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">getPayment</a>({ ...params }) -> SuwardSDK.GetV1PaymentsPaymentIdResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns full payment details when called with an API key (merchant view).
Returns limited payment details when called without an API key (customer view).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.getPayment({
    paymentId: "paymentId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.GetV1PaymentsPaymentIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">activatePayment</a>({ ...params }) -> SuwardSDK.CryptopayPublicPaymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Activate a payment (public, customer-facing)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.activatePayment({
    paymentId: "paymentId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.PostV1PaymentsPaymentIdActivateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">cancelPayment</a>({ ...params }) -> SuwardSDK.CryptopayPaymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel a payment that has not yet completed. It stops accepting funds and moves to a terminal Failed state. Only valid from early statuses (before finality).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.cancelPayment({
    paymentId: "paymentId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.PostV1PaymentsPaymentIdCancelRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">simulatePayment</a>({ ...params }) -> SuwardSDK.CryptopayPaymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Simulate a payment status transition. Available for test-coin assets only.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.simulatePayment({
    paymentId: "paymentId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.CryptopaySimulatePaymentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">quotePaymentFees</a>({ ...params }) -> SuwardSDK.CryptopayQuotePaymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the platform fee, estimated network fee, and net amount for a payment of `amount` in `asset`, without creating anything. All monetary fields are integer strings in the asset's smallest unit.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.quotePaymentFees({
    asset: "USDT_ETHEREUM",
    amount: "amount"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.CryptopayQuotePaymentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">listPaymentTransactions</a>({ ...params }) -> SuwardSDK.CryptopaywireTransactionList</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Paginated list of the on-chain transactions detected for a payment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.listPaymentTransactions({
    paymentId: "paymentId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.GetV1PaymentsPaymentIdTransactionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## StaticWallets
<details><summary><code>client.staticWallets.<a href="/src/api/resources/staticWallets/client/Client.ts">listStaticWallets</a>({ ...params }) -> SuwardSDK.CryptopayListStaticWalletsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the project's static wallets, newest first. Paginated via limit and lastId.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.staticWallets.listStaticWallets();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.GetV1StaticWalletsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StaticWalletsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.staticWallets.<a href="/src/api/resources/staticWallets/client/Client.ts">createStaticWallet</a>({ ...params }) -> SuwardSDK.CryptopayStaticWalletResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a reusable deposit address with an accepted-asset allow-list
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.staticWallets.createStaticWallet();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.CryptopayCreateStaticWalletRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StaticWalletsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.staticWallets.<a href="/src/api/resources/staticWallets/client/Client.ts">getStaticWallet</a>({ ...params }) -> SuwardSDK.CryptopayStaticWalletResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Fetch a single static wallet by its id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.staticWallets.getStaticWallet({
    staticWalletId: "staticWalletId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.GetV1StaticWalletsStaticWalletIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StaticWalletsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.staticWallets.<a href="/src/api/resources/staticWallets/client/Client.ts">deleteStaticWallet</a>({ ...params }) -> Record&lt;string, boolean&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a static wallet. Its address stops being monitored and can no longer receive new deposits; previously recorded deposits are unaffected.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.staticWallets.deleteStaticWallet({
    staticWalletId: "staticWalletId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.DeleteV1StaticWalletsStaticWalletIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StaticWalletsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.staticWallets.<a href="/src/api/resources/staticWallets/client/Client.ts">updateStaticWallet</a>({ ...params }) -> SuwardSDK.CryptopayStaticWalletResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a static wallet's accepted-asset allow-list, metadata, or webhook URL. Only the fields present in the body are changed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.staticWallets.updateStaticWallet({
    staticWalletId: "staticWalletId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.CryptopayUpdateStaticWalletRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StaticWalletsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.staticWallets.<a href="/src/api/resources/staticWallets/client/Client.ts">listStaticWalletDeposits</a>({ ...params }) -> SuwardSDK.CryptopayListStaticDepositsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Paginated list of the deposits received by a static wallet, newest first.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.staticWallets.listStaticWalletDeposits({
    staticWalletId: "staticWalletId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.GetV1StaticWalletsStaticWalletIdDepositsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StaticWalletsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.staticWallets.<a href="/src/api/resources/staticWallets/client/Client.ts">getStaticWalletDeposit</a>({ ...params }) -> SuwardSDK.CryptopayStaticDepositResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Fetch a single static-wallet deposit by its id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.staticWallets.getStaticWalletDeposit({
    staticWalletId: "staticWalletId",
    depositId: "depositId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.GetV1StaticWalletsStaticWalletIdDepositsDepositIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StaticWalletsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.staticWallets.<a href="/src/api/resources/staticWallets/client/Client.ts">simulateStaticWalletDeposit</a>({ ...params }) -> SuwardSDK.CryptopayStaticDepositResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Drive a synthetic deposit through its lifecycle (no on-chain activity, no balance credit). Available for test-coin assets only.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.staticWallets.simulateStaticWalletDeposit({
    staticWalletId: "staticWalletId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `SuwardSDK.CryptopaySimulateStaticDepositRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StaticWalletsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Assets
<details><summary><code>client.assets.<a href="/src/api/resources/assets/client/Client.ts">listAcceptedAssets</a>() -> SuwardSDK.GetV1AssetsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all assets accepted by the Suward gateway. No authentication required.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.assets.listAcceptedAssets();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AssetsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.assets.<a href="/src/api/resources/assets/client/Client.ts">listSupportedBlockchains</a>() -> SuwardSDK.CryptopayBlockchainResponse[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all supported blockchains (informational). No authentication required.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.assets.listSupportedBlockchains();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AssetsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

