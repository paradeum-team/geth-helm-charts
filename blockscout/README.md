# blockscout

A Helm chart for Kubernetes

![Version: 0.1.4](https://img.shields.io/badge/Version-0.1.4-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 13573befcc6b94c68b4a05554377e101f36bd7fe](https://img.shields.io/badge/AppVersion-13573befcc6b94c68b4a05554377e101f36bd7fe-informational?style=flat-square)

## Installing the Chart

Add repository

```
helm repo add paradeum-team https://paradeum-team.github.io/helm-charts/
helm repo update
```

Install chart

```
helm install my-blockscout paradeum-team/blockscout --version --version 0.1.4
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| args[0] | string | `"-c"` |  |
| args[1] | string | `"bin/blockscout start"` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| command[0] | string | `"/bin/sh"` |  |
| envFrom[0].secretRef.name | string | `"blockscout-secret"` |  |
| env[0].name | string | `"ETHEREUM_JSONRPC_VARIANT"` |  |
| env[0].value | string | `"geth"` |  |
| env[10].name | string | `"LOGO_FOOTER"` |  |
| env[10].value | string | `"/images/chain-wallet.png"` |  |
| env[11].name | string | `"BLOCKSCOUT_VERSION"` |  |
| env[11].value | string | `"13573befcc6b94c68b4a05554377e101f36bd7fe"` |  |
| env[12].name | string | `"RELEASE_LINK"` |  |
| env[12].value | string | `"https://github.com/paradeum-team/blockscout/releases/tag/${BLOCKSCOUT_VERSION}"` |  |
| env[13].name | string | `"DISABLE_EXCHANGE_RATES"` |  |
| env[13].value | string | `"true"` |  |
| env[14].name | string | `"DISABLE_KNOWN_TOKENS"` |  |
| env[14].value | string | `"true"` |  |
| env[15].name | string | `"SHOW_ADDRESS_MARKETCAP_PERCENTAGE"` |  |
| env[15].value | string | `"false"` |  |
| env[16].name | string | `"SHOW_PRICE_CHART"` |  |
| env[16].value | string | `"false"` |  |
| env[17].name | string | `"DISABLE_BRIDGE_MARKET_CAP_UPDATER"` |  |
| env[17].value | string | `"true"` |  |
| env[18].name | string | `"SHOW_TXS_CHART"` |  |
| env[18].value | string | `"true"` |  |
| env[19].name | string | `"ENABLE_TXS_STATS"` |  |
| env[19].value | string | `"true"` |  |
| env[1].name | string | `"COIN"` |  |
| env[1].value | string | `"SC"` |  |
| env[20].name | string | `"HIDE_BLOCK_MINER"` |  |
| env[20].value | string | `"true"` |  |
| env[21].name | string | `"DISABLE_READ_API"` |  |
| env[21].value | string | `"true"` |  |
| env[22].name | string | `"DISABLE_WRITE_API"` |  |
| env[22].value | string | `"true"` |  |
| env[23].name | string | `"ECTO_USE_SSL"` |  |
| env[23].value | string | `"false"` |  |
| env[24].name | string | `"SUPPORTED_CHAINS"` |  |
| env[24].value | string | `"[{\"title\":\"POA\",\"url\":\"https://blockscout.com/poa/core\"},{\"title\":\"Sokol\",\"url\":\"https://blockscout.com/poa/sokol\",\"test_net?\":true},{\"title\":\"Gnosis Chain\",\"url\":\"https://blockscout.com/xdai/mainnet\"},{\"title\":\"Ethereum Classic\",\"url\":\"https://blockscout.com/etc/mainnet\",\"other?\":true},{\"title\":\"RSK\",\"url\":\"https://blockscout.com/rsk/mainnet\",\"other?\":true},{\"title\":\"Solar Chain Testnet\",\"url\":\"https://sctscan.starnet.ltd/\",\"test_net?\":true}]"` |  |
| env[25].name | string | `"APPS_MENU"` |  |
| env[25].value | string | `"false"` |  |
| env[26].name | string | `"EXTERNAL_APPS"` |  |
| env[26].value | string | `""` |  |
| env[27].name | string | `"PORT"` |  |
| env[27].value | string | `"4000"` |  |
| env[28].name | string | `"POOL_SIZE"` |  |
| env[28].value | string | `"40"` |  |
| env[29].name | string | `"POOL_SIZE_API"` |  |
| env[29].value | string | `"10"` |  |
| env[2].name | string | `"COIN_NAME"` |  |
| env[2].value | string | `"SC"` |  |
| env[30].name | string | `"ENABLE_RUST_VERIFICATION_SERVICE"` |  |
| env[30].value | string | `"false"` |  |
| env[31].name | string | `"RUST_VERIFICATION_SERVICE_URL"` |  |
| env[31].value | string | `"http://127.0.0.1:8043/"` |  |
| env[32].name | string | `"ACCOUNT_ENABLED"` |  |
| env[32].value | string | `"false"` |  |
| env[3].name | string | `"ETHEREUM_JSONRPC_HTTP_URL"` |  |
| env[3].value | string | `"http://127.0.0.1:8545"` |  |
| env[4].name | string | `"ETHEREUM_JSONRPC_WS_URL"` |  |
| env[4].value | string | `"ws://127.0.0.1:8546"` |  |
| env[5].name | string | `"INDEXER_MEMORY_LIMIT"` |  |
| env[5].value | string | `"1gb"` |  |
| env[6].name | string | `"BLOCK_TRANSFORMER"` |  |
| env[6].value | string | `"clique"` |  |
| env[7].name | string | `"NETWORK"` |  |
| env[7].value | string | `"Solar Chain"` |  |
| env[8].name | string | `"SUBNETWORK"` |  |
| env[8].value | string | `"Solar Chain Testnet"` |  |
| env[9].name | string | `"LOGO"` |  |
| env[9].value | string | `"/images/chain-wallet.png"` |  |
| extraVolumeMounts[0].mountPath | string | `"/etc/localtime"` |  |
| extraVolumeMounts[0].name | string | `"localtime"` |  |
| extraVolumeMounts[0].readOnly | bool | `true` |  |
| extraVolumes[0].hostPath.path | string | `"/etc/localtime"` |  |
| extraVolumes[0].name | string | `"localtime"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"quay.io/netwarps/blockscout@sha256"` |  |
| image.tag | string | `"bb30328997c1b147dc123ce6ab9d3f6c2e86583cd26ebd2d3b035211b511339f"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| initContainer.args[0] | string | `"-c"` |  |
| initContainer.args[1] | string | `"bin/blockscout eval \"Elixir.Explorer.ReleaseTasks.create_and_migrate()\""` |  |
| initContainer.command[0] | string | `"/bin/sh"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `4000` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| smartContractVerifier.enabled | bool | `false` |  |
| smartContractVerifier.env[0].name | string | `"SMART_CONTRACT_VERIFIER__SERVER__ADDR"` |  |
| smartContractVerifier.env[0].value | string | `"0.0.0.0:8043"` |  |
| smartContractVerifier.env[10].name | string | `"SMART_CONTRACT_VERIFIER__SOURCIFY__API_URL"` |  |
| smartContractVerifier.env[10].value | string | `"https://sourcify.dev/server/"` |  |
| smartContractVerifier.env[11].name | string | `"SMART_CONTRACT_VERIFIER__SOURCIFY__VERIFICATION_ATTEMPTS"` |  |
| smartContractVerifier.env[11].value | string | `"3"` |  |
| smartContractVerifier.env[12].name | string | `"SMART_CONTRACT_VERIFIER__SOURCIFY__REQUEST_TIMEOUT"` |  |
| smartContractVerifier.env[12].value | string | `"10"` |  |
| smartContractVerifier.env[13].name | string | `"SMART_CONTRACT_VERIFIER__METRICS__ENABLED"` |  |
| smartContractVerifier.env[13].value | string | `"false"` |  |
| smartContractVerifier.env[14].name | string | `"SMART_CONTRACT_VERIFIER__JAEGER__ENABLED"` |  |
| smartContractVerifier.env[14].value | string | `"false"` |  |
| smartContractVerifier.env[1].name | string | `"SMART_CONTRACT_VERIFIER__SOLIDITY__ENABLED"` |  |
| smartContractVerifier.env[1].value | string | `"true"` |  |
| smartContractVerifier.env[2].name | string | `"SMART_CONTRACT_VERIFIER__SOLIDITY__COMPILERS_DIR"` |  |
| smartContractVerifier.env[2].value | string | `"/tmp/solidity-compilers"` |  |
| smartContractVerifier.env[3].name | string | `"SMART_CONTRACT_VERIFIER__SOLIDITY__REFRESH_VERSIONS_SCHEDULE"` |  |
| smartContractVerifier.env[3].value | string | `"0 0 * * * * *"` |  |
| smartContractVerifier.env[4].name | string | `"SMART_CONTRACT_VERIFIER__SOLIDITY__FETCHER__LIST__LIST_URL"` |  |
| smartContractVerifier.env[4].value | string | `"https://solc-bin.ethereum.org/linux-amd64/list.json"` |  |
| smartContractVerifier.env[5].name | string | `"SMART_CONTRACT_VERIFIER__VYPER__ENABLED"` |  |
| smartContractVerifier.env[5].value | string | `"true"` |  |
| smartContractVerifier.env[6].name | string | `"SMART_CONTRACT_VERIFIER__VYPER__COMPILERS_DIR"` |  |
| smartContractVerifier.env[6].value | string | `"/tmp/vyper-compilers"` |  |
| smartContractVerifier.env[7].name | string | `"SMART_CONTRACT_VERIFIER__VYPER__FETCHER__LIST__LIST_URL"` |  |
| smartContractVerifier.env[7].value | string | `"https://raw.githubusercontent.com/blockscout/solc-bin/main/vyper.list.json"` |  |
| smartContractVerifier.env[8].name | string | `"SMART_CONTRACT_VERIFIER__VYPER__REFRESH_VERSIONS_SCHEDULE"` |  |
| smartContractVerifier.env[8].value | string | `"0 0 * * * * *"` |  |
| smartContractVerifier.env[9].name | string | `"SMART_CONTRACT_VERIFIER__SOURCIFY__ENABLED"` |  |
| smartContractVerifier.env[9].value | string | `"true"` |  |
| smartContractVerifier.image.pullPolicy | string | `"IfNotPresent"` |  |
| smartContractVerifier.image.repository | string | `"ghcr.io/blockscout/smart-contract-verifier"` |  |
| smartContractVerifier.image.tag | string | `"v0.5.0"` |  |
| smartContractVerifier.resources | object | `{}` |  |
| tolerations | list | `[]` |  |
