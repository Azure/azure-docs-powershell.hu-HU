---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 21e821a4575fb918599ad2315c569a7f270e0a84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671183"
---
# Get-AzContainerRegistryReplication

## Áttekintés
A tároló beállításjegyzékének replikálását kapja.

## SZINTAXISA

### ListReplicationByNameResourceGroupParameterSet (alapértelmezett)
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ShowReplicationByNameResourceGroupParameterSet
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ShowReplicationByRegistryObjectParameterSet
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListReplicationByRegistryObjectParameterSet
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A Get-AzContainerRegistryReplication parancsmag a tároló beállításjegyzékének meghatározott replikálását vagy a tároló beállításjegyzékének összes replikálását kapja.

## Példák

### Példa 1: egy tároló rendszerleíró adatbázisának meghatározott replikálását kapja meg.
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

A tároló beállításjegyzékének meghatározott replikálását kapja

### 2. példa: a tárolók rendszerleíró adatbázisának minden replikálását kapja meg.
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

A tároló beállításjegyzékének minden replikálását kapja

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A tároló beállításjegyzék-replikációs neve.

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Registry
Tároló rendszerleíróadatbázis-objektum.

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RegistryName
A tároló beállításjegyzékének neve.

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A tároló beállításjegyzék-replikációs erőforrás-azonosítója

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry

### System. String

## KIMENETEK

### Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryReplication

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzContainerRegistryReplication](New-AzContainerRegistryReplication.md)

[Remove-AzContainerRegistryReplication](Remove-AzContainerRegistryReplication.md)