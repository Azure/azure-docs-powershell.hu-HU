---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: a714730a416d7554cba53e96428c9813fe4e720d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922194"
---
# New-AzApiManagementVirtualNetwork

## SYNOPSIS
Létrehozza a PsApiManagementVirtualNetwork példányát.

## SZINTAXIS

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzApiManagementVirtualNetwork** parancsmag egy segítő parancs a **PsApiManagementVirtualNetwork** példányának létrehozásához.
Ez a parancs a **Set-AzApiManagement** és a **New-AzApiManagement** parancsmaggal használható.

## PÉLDÁK

### 1. példa: Virtuális hálózat létrehozása és meglévő APIM-szolgáltatás frissítése a VNET-be
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

Ez a példa létrehoz egy virtuális hálózatot, majd felhívja a **Set-AzApiManagement** parancsmagot.

### 2. példa: API-kezelési szolgáltatás létrehozása külső virtuális hálózathoz
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

Ebben a példában egy új APIM-szolgáltatást hoz létre virtuális hálózat `External` módban

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

### -SubnetResourceId
A virtuális hálózat alhálózati erőforrás-azonosítóját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)

