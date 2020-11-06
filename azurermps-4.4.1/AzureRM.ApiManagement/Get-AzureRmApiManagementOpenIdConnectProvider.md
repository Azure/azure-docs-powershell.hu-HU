---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492619"
---
# Get-AzureRmApiManagementOpenIdConnectProvider

## Áttekintés
Megkapja az OpenID Connect szolgáltatókat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Az összes OpenID Connect-szolgáltató beszerzése (alapértelmezett)
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Get by OpenID Connect Provider azonosító
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Keresés az OpenID-kapcsolat szolgáltatójának felhasználóbarát nevében
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmApiManagementOpenIdConnectProvider** parancsmag OpenID Connect-szolgáltatókat kap az Azure API-menedzsmentben.

## Példák

### Példa 1: az összes szolgáltató beszerzése
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

Ez a parancs az összes OpenID Connect szolgáltatót megkapja a megadott környezetben.

### 2. példa: szolgáltató beszerzése azonosító használatával
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

Ez a parancs a OICProvicer01 AZONOSÍTÓját tartalmazó szolgáltatót kapja.

### 3. példa: szolgáltató beszerzése név használatával
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

Ez a parancs a contoso OpenID Connect Provider nevű szolgáltatót kapja meg.

## PARAMÉTEREK

### -Környezet
Egy **PsApiManagementContext** -objektumot ad meg.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A szolgáltató rövid nevét adja meg.
Ha megad egy nevet, ez a parancsmag a szolgáltatót kapja.

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OpenIdConnectProviderId
Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amely a parancsmagot eltávolítja.
Ha azonosítót ad meg, ez a parancsmag a szolgáltatót kapja meg.

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmApiManagementOpenIdConnectProvider](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[Remove-AzureRmApiManagementOpenIdConnectProvider](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[Set-AzureRmApiManagementOpenIdConnectProvider](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


