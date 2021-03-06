---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/get-azurermmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
ms.openlocfilehash: b1fe94533074860a3c95c05d6609bb8ebb446a9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497591"
---
# Get-AzureRmManagementPartner

## Áttekintés
Az aktuálisan hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) azonosítójának beszerzése. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az aktuálisan hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) azonosítójának beszerzése. 

## Példák

### Példa 1
```powershell
PS C:\> Get-AzureRmManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

A jelenlegi felügyeleti partner azonosítójának beszerzése

### 2. példa
```powershell
PS C:\> Get-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

A jelenlegi kezelési partnerek azonosítójának beszerzése partner-azonosítóval (ha nem egyeznek meg), sikertelen lesz

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

### -PartnerId
A kezelési partner azonosítója a 6 jegyű szám

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. Resources. PSManagementPartner

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureRmManagementPartner](./Remove-AzureRmManagementPartner.md)

[Új – AzureRmManagementPartner](./New-AzureRmManagementPartner.md)

[Update-AzureRmManagementPartner](./Update-AzureRmManagementPartner.md)
