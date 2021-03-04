---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 842d0c26d4034a8c07415dfe8524b32623c07e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936417"
---
# Get-AzVMWareCluster

## SYNOPSIS
Fürt létrehozása név szerint egy privát felhőben

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Bej.le
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## LEÍRÁS
Fürt létrehozása név szerint egy privát felhőben

## PÉLDÁK

### 1. példa: Fürt lekérte
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

Fürt lekérte

### 2. példa: Listacsoportok
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

Lista fürtök

## PARAMETERS

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

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A privát felhőben lévő fürt neve

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateCloudName
A privát felhő neve

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.
A névben a kis- és

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A célként megcélzott előfizetés azonosítója.

```yaml
Type: System.String[]
Parameter Sets: Get, List
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

### Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <IVMWareIdentity> Identity Parameter
  - `[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben
  - `[ClusterName <String>]`: A privát felhőben lévő fürt neve
  - `[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[Location <String>]`: Azure-régió
  - `[PrivateCloudName <String>]`: A privát felhő neve
  - `[ResourceGroupName <String>]`: Az erőforráscsoport neve. A névben a kis- és
  - `[SubscriptionId <String>]`: A cél-előfizetés azonosítója.

## KAPCSOLÓDÓ HIVATKOZÁSOK

