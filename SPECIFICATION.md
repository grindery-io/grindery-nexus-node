# Grindery Nexus Node API Specification

This document specifies the Grindery Nexus Node API methods.


## Index

- [Connectors](#connectors)
  - [gn_createConnector](#gn_createConnector)
  - [gn_getConnectors](#gn_getConnectors)
  - [gn_getConnectors](#gn_getConnectors)
  - [gn_updateConnector](#gn_updateConnector)
- [Workflows](#workflows)
  - [gn_createWorkflow](#gn_createWorkflow)
  - [gn_getWorkflows](#gn_getWorkflows)
  - [gn_getWorkflow](#gn_getWorkflow)
  - [gn_updateWorkflow](#gn_updateWorkflow)
- [Wallets](#wallets)
  - [gn_getChainWallets](#gn_getChainWallets)
  - [gn_getChainWallet](#gn_getChainWallet)


## Connectors

### gn_createConnector

Creates a connector.

**Parameters:**

Index | Type | Description
------|------|------------
1 | [ConnectorSchema](https://github.com/grindery-io/grindery-nexus-schema/tree/master/connectors#connectorschema) | the connector definition.

**Returns:**

`string` | the id of the connector.


### gn_getConnectors

Returns connector definitions.

**Parameters:**

none.

**Returns:**

`Array<object>` | an array of objects each representing one connector.

Each item should have the following properties.

Key | Type | Description
----|------|------------
`id` | `string` | the id of the connector.
`data` | [ConnectorSchema](https://github.com/grindery-io/grindery-nexus-schema/tree/master/connectors#connectorschema) | the connector definition.


### gn_getConnector

Returns a connector definition.

**Parameters:**

Index | Type | Description
------|------|------------
1 | `string` | id of the connector.

**Returns:**

[ConnectorSchema](https://github.com/grindery-io/grindery-nexus-schema/tree/master/connectors#connectorschema) | the connector definition.


### gn_updateConnector

Updates a connector.

**Parameters:**

Index | Type | Description
------|------|------------
1 | `string` | id of the connector.
2 | [ConnectorSchema](https://github.com/grindery-io/grindery-nexus-schema/tree/master/connectors#connectorschema) | the connector definition.

**Returns:**

`string` | the id of the connector.


## Workflows

### gn_createWorkflow

Creates a workflow.

**Parameters:**

Index | Type | Description
------|------|------------
1 | [WorkflowSchema](https://github.com/grindery-io/grindery-nexus-schema/tree/master/workflows#workflowschema) | the workflow definition.

**Returns:**

`string` | the id of the workflow.


### gn_getWorkflows

Returns workflow definitions.

**Parameters:**

none.

**Returns:**

array<[WorkflowSchema](https://github.com/grindery-io/grindery-nexus-schema/tree/master/workflows#workflowschema)> | a list of workflow definitions.

`Array<object>` | an array of objects each representing one workflow.

Each item should have the following properties.

Key | Type | Description
----|------|------------
`id` | `string` | the id of the workflow.
`data` | [WorkflowSchema](https://github.com/grindery-io/grindery-nexus-schema/tree/master/workflows#workflowschema) | the workflow definition.


### gn_getWorkflow

Returns a workflow definition.

**Parameters:**

Index | Type | Description
------|------|------------
1 | `string` | id of the workflow.

**Returns:**

[WorkflowSchema](https://github.com/grindery-io/grindery-nexus-schema/tree/master/workflows#workflowschema) | the workflow definition.


### gn_updateWorkflow

Updates a workflow.

**Parameters:**

Index | Type | Description
------|------|------------
1 | `string` | id of the workflow.
2 | [WorkflowSchema](https://github.com/grindery-io/grindery-nexus-schema/tree/master/workflows#workflowschema) | the workflow definition.

**Returns:**

`string` | the id of the workflow.


## Wallets

### gn_getChainWallets

Returns Grindery Nexus Wallet account identifiers for all supported chains.

**Parameters:**

none.

**Returns:**

array<[ChainAccountSchema](https://github.com/grindery-io/grindery-nexus-schema/blob/master/connectors/README.md#chainaccountschema)> | The Grindery Nexus Wallet account identifier for the specified chain.


### gn_getChainWallet

Returns the Grindery Nexus Wallet account identifier for the specified chain.

**Parameters:**

Index | Type | Description
------|------|------------
1 | [ChainSchema](https://github.com/grindery-io/grindery-nexus-schema/blob/master/connectors/README.md#chainschema) | The identifier of the chain e.g `eip155:1` for Ethereum Mainnet.

**Returns:**

[ChainAccountSchema](https://github.com/grindery-io/grindery-nexus-schema/blob/master/connectors/README.md#chainaccountschema) | The Grindery Nexus Wallet account identifier for the specified chain.
 
