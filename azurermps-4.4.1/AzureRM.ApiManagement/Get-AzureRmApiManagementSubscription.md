---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503324"
---
# Get-AzureRmApiManagementSubscription

## Áttekintés
Előfizetéseket kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Az összes előfizetés lekérése (alapértelmezett)
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Beolvasás subsctiption-AZONOSÍTÓval
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Beolvasás felhasználói AZONOSÍTÓval
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Get by Product ID
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmApiManagementSubscription** parancsmag megadott előfizetést kap, vagy minden előfizetést, ha nincs megadva előfizetés.

## Példák

### Példa 1: az összes előfizetés lekérése
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

Ez a parancs minden előfizetéshez bekerül.

### 2. példa: előfizetés kérése megadott AZONOSÍTÓval
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

Ez a parancs AZONOSÍTÓval kapja meg az előfizetést.

### 3. példa: a felhasználók összes előfizetésének beszerzése
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

Ez a parancs a felhasználó előfizetéseit kapja meg.

### Példa 4: a termékek összes előfizetésének beszerzése
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

Ez a parancs beolvassa a szorzat összes előfizetését.

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

### -Termékkód
Egy termékazonosítót ad meg.
Ha meg van adva, ez a parancsmag minden előfizetést megtalál a termékazonosítóban.

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionId
Az előfizetés azonosítóját adja meg.
Ha meg van adva, ez a parancsmag megkeresi az előfizetést az azonosító alapján.

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserId
A felhasználó azonosítóját adja meg.
Ha meg van adva, ez a parancsmag megkeresi az összes előfizetést a felhasználói azonosítóval.

```yaml
Type: System.String
Parameter Sets: Get by user ID
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

### IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmApiManagementSubscription](./New-AzureRmApiManagementSubscription.md)

[Remove-AzureRmApiManagementSubscription](./Remove-AzureRmApiManagementSubscription.md)

[Set-AzureRmApiManagementSubscription](./Set-AzureRmApiManagementSubscription.md)


