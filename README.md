# Optimism Collective and OP Stack Documentation Improvements

Hello Optimism Collective! I'm Greg Cardo, a passionate developer focused on enhancing the usability, and accessibility of the OP Stack through high-standard documentation. This project primarily focuses around improving the OP Stack documentation, where I've introduced useful updates and clarifications to support developers and operators working with Optimism's core infrastructure. Below are highlights of my contributions:

## Resolved

* **[Derivative Pipeline Information](https://github.com/ethereum-optimism/docs/pull/805/files):** Added a high-level overview of the derivative pipeline and linked the specs page.

* **[Node Log Levels Explainer](https://github.com/ethereum-optimism/docs/pull/779/files):** This PR updates the consensus-config.mdx file to include detailed documentation on log levels for the op-node. The new section describes various log levels, ranging from silent to detailed, and provides guidance on setting the log level using the --log.level flag.

* **[Information on Expected Internal Reverts for Withdrawal Transactions](https://github.com/ethereum-optimism/docs/pull/853/files):** This modification adds a section to the existing withdrawal-flow.mdx documentation to explain the expected internal reverts that users often see on Etherscan during withdrawal transactions.

* **[Information about `proxyd`](https://github.com/ethereum-optimism/docs/pull/857/files):** I added a dedicated section and explanation for the proxyd service under Chain Operators > Operator Features. Documentation included what `proxyd` is, key features, how it works, consensus awareness, caching and metrics.

* **[Details on the sequencer fee vault](https://github.com/ethereum-optimism/docs/pull/858/files):** I added in-depth details on the sequence fee vaults to indicate where transaction fees collected by the sequencer go.

* **[Addition of rollup.sequencerhttp to node operation docs](https://github.com/ethereum-optimism/docs/pull/865/files):** Added a "callout" to the node operation documentation in step 7, instructing users to configure the --rollup.sequencerhttp flag.

* **[Addition of a Callout on the Cap for sequencer.l1-confs and verifier.l1-confs](https://github.com/ethereum-optimism/docs/pull/866/files):** Added a callout to the sequencer.l1-confs and verifier.l1-confs configuration options in the node operation documentation. The callout highlighted the maximum values for sequencer.l1-confs to be 1800 seconds (150 blocks) since the Fjord upgrade is live. It also suggests keeping verifier.l1-confs within a 12-13 minute range (10-20 blocks) for optimal performance.

* **[OP Conductor Docs Improvement](https://github.com/ethereum-optimism/docs/pull/796/files):** Improvements include:
  1. **Safe Head Database (SafeDB) Configuration:** Detailed instructions on enabling the SafeDB for op-node by setting the --safedb.path value. Explanation of the importance of SafeDB in ensuring the op-node is not stateless and can persist crucial update data.
  2. **Rollup RPC Configuration:** Clear guidelines on setting the --rollup-rpc flag to point to an op-node archive node, highlighting the need for the challenger to access historical output roots. Inclusion of an example configuration snippet for ease of understanding and implementation.
  3. **Historical Data Requirements:** Emphasis on the necessity for both op-node and op-geth to have data from the start of the games to maintain network consistency. Guidelines on ensuring sufficient historical data availability for both nodes, either through local storage or using archive nodes.

* **[Docker Images Discoverabilty](https://github.com/ethereum-optimism/docs/pull/809/files):** Improvements for docker images discoverability include:
  1. **Comprehensive Software Releases:** Expanding the scope to include all software components, not just node components. Adding op-challenger to the list of software components with links to releases.
  2. **Docker Image Searchability:** Clear instructions and links to find Docker images for op-node and op-geth. Consistent tagging conventions for Docker images to aid in searchability.
  3. **Example Docker Image Tags:** Examples of tagging the Docker images for better understanding and easier access.

* **[Chain Operator Feature: Span Batches](https://github.com/ethereum-optimism/docs/pull/823/files):** Enhancements include: 1. Documentation for Span Batches: Overview of what span batches are and their benefits. Detailed instructions on how to enable span batches in the chain configuration. 2. Configuration Instructions: Clear steps to add or update the configuration settings to enable span batches. Instructions on redeploying the chain node and verifying the changes. 3. Links to Related Pages: Direct links to detailed span batches specification and design documents for further reading.

## Work in Progress

* **[Cross Domain Section](https://github.com/ethereum-optimism/docs/pull/876/files):** Carving out a new "Cross Domain" section under OP STACK > Protocol that gives an overview of the lifecycle of an OP Stack cross-chain transaction.
