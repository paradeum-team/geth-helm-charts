# blockscout

A Helm chart for Kubernetes

![Version: 0.1.3](https://img.shields.io/badge/Version-0.1.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v4.1.8-beta.3](https://img.shields.io/badge/AppVersion-v4.1.8--beta.3-informational?style=flat-square)

## Installing the Chart

Add repository

```
helm repo add paradeum-team https://paradeum-team.github.io/helm-charts/
helm repo update
```

Install chart

```
helm install my-blockscout paradeum-team/blockscout --version --version 0.1.3
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
| env[11].value | string | `"v4.1.8-beta.3"` |  |
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
| image.repository | string | `"quay.io/netwarps/blockscout"` |  |
| image.tag | string | `"v4.1.8-beta.3"` |  |
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
| tolerations | list | `[]` |  |
