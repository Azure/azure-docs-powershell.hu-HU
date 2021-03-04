---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 53a164b2cd3421898974f7f5f1c2fd2b7ed51c21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921537"
---
# Get-AzApiManagementCache

## SYNOPSIS
A gyorsítótár részleteinek megtekintése.

## SZINTAXIS

### ContextParameterSet (alapértelmezett)
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az Api Management szolgáltatásban konfigurált gyorsítótár részleteinek megtekintése.

## PÉLDÁK

### 1. példa: Az összes gyorsítótár lekérte
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

Az Api Management szolgáltatásban konfigurált összes gyorsítótár listáját lekérte.

### 2. példa: A westus azonosító által megadott gyorsítótár lekérte
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

A westushoz konfigurált gyorsítótár részleteinek megtekintése

## PARAMETERS

### -CacheId
Gyorsítótár azonosítója.
Ha meg van adva, a rendszer megpróbálja megtalálni a gyorsítótárat az azonosító alapján.
Ez a paraméter nem kötelező.

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Környezet
A PsApiManagementContext példánya.
Ezt a paramétert kötelező megadni.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -ResourceId
Gyorsítótár erőforrás-azonosítójának felkarazása Ha meg van adva, a rendszer megpróbálja megtalálni a gyorsítótárat az azonosító alapján. Ezt a paramétert kötelező megadni.

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

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzApiManagementCache](./New-AzApiManagementCache.md)

[Remove-AzApiManagementCache](./Remove-AzApiManagementCache.md)

[Update-AzApiManagementCache](./Update-AzApiManagementCache.md)
