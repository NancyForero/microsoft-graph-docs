---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let runs = await client.api('/security/attackSimulation/simulationAutomations/fbad62b0-b32d-b6ac-9f48-d84bbea08f96/runs')
	.version('beta')
	.get();

```