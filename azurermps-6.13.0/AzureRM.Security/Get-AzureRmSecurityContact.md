---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679508"
---
# Get-AzureRmSecurityContact

## Áttekintés
Az előfizetésben konfigurált biztonsági névjegyek lekérdezése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### SubscriptionScope (alapértelmezett)
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelResource
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Megkapja az előfizetésben konfigurált biztonsági névjegyeket.
A biztonsági partnerek értesítést kaphatnak az előfizetésben megjelenő biztonsági figyelmeztetésekről.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

Az összes konfigurált biztonsági partner beolvasása az előfizetésben

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Erőforrás neve

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Erőforrás-azonosító.

```yaml
Type: String
Parameter Sets: ResourceId
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

### Microsoft. Azure. commands. Security. models. SecurityContacts. PSSecurityContact

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
