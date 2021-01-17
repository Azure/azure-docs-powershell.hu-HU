---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371110"
---
# Get-AzKustoClusterSku

## SYNOPSIS
A Kusto-erőforrásszolgáltatóhoz használható, erre jogosult termékek listája.

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Lista1
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## LEÍRÁS
A Kusto-erőforrásszolgáltatóhoz használható, erre jogosult termékek listája.

## PÉLDÁK

### 1. példa: A jogosult termékek listája
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

A fenti parancs felsorolja a jogosult SKUs-okat.

### 2. példa: Az adott fürtre vonatkozó, jogosult termékkódok listája
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

A fenti parancs felsorolja az adott fürtre vonatkozó, jogosult termékkódokat.

## PARAMETERS

### -ClusterName
A Kusto-fürt neve.

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A Kusto-fürtöt tartalmazó erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.
Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription

## MEGJEGYZÉSEK

ALIASOK

## KAPCSOLÓDÓ HIVATKOZÁSOK

