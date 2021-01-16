---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379943"
---
# Get-AzNetworkVirtualAppliance

## SYNOPSIS
Virtuális hálózati készülékek be- vagy listába való be- vagy listába való be szereznie.

## SZINTAXIS

### ResourceNameParameterSet (alapértelmezett)
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A Get-AzNetworkVirtualAppliance parancsok a hálózati virtuális eszköz erőforrásait kapják vagy sorolják fel.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

Hálózati virtuális eszköz típusú erőforrás létrehozása.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Name
Az erőforrás neve.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az erőforrás azonosítója.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
