---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a68604e9701a6ae2c251edf3f2a0935df5ffa94f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835582"
---
# Get-AzKustoCluster

## Áttekintés
Megtekintheti egy erőforráscsoport összes Kusto-szektorcsoportját, vagy egy bizonyos Kusto-fürtöt.

## SZINTAXISA

### ByClusterOrResourceGroupOrSubscription (alapértelmezett)
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByResourceId
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Megtekintheti egy erőforráscsoport összes Kusto-szektorcsoportját, vagy egy bizonyos Kusto-fürtöt.

## Példák

### Példa 1 – egy erőforráscsoport összes Kusto listája

Írja be a következőt: Microsoft. Kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg név: mykustocluster1 hely: Közép-amerikai kapacitás: 3 SKU: D13_v2 ProvisioningState: sikeres állapot: futó címke: {} URI: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net

Írja be a következőt: Microsoft. Kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg név: mykustocluster2 hely: Közép-amerikai kapacitás: 5 SKU: D13_v2 ProvisioningState: sikeres állapot: futó címke: {} URI: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

A fenti parancs felsorolja az összes Kusto-szektorcsoportot az "testrg" erőforráscsoport csoportjában.

### 2 példa – adott Kusto-fürt beszerzése név alapján

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

A fenti parancs az "testrg" erőforráscsoport "mykustocluster" nevű Kusto-fürtöt számítja ki.

### 3 példa – adott Kusto-fürt beszerzése erőforrás-azonosítóval

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

A fenti parancs az "testrg" erőforráscsoport "mykustocluster" nevű Kusto-fürtöt számítja ki.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Egy adott fürt neve.

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnek a neve, amelyben a felhasználó a fürtöt szeretné beolvasni.

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Kusto a cluster ResourceID.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Kusto. models. PSKustoCluster

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
