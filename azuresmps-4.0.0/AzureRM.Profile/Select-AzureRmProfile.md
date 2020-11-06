---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491324"
---
# Select-AzureRmProfile

## Áttekintés
Azure-hitelesítési adatok betöltése egy fájlból.

## SZINTAXISA

### InMemoryProfile
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### ProfileFromDisk
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## Leírás
A Select-AzureRmProfile parancsmag az Azure-környezet és-környezet beállításához betölti a fájlok hitelesítési adatait.
Az aktuális munkamenetben futtatott parancsmagok ezekkel az információkkal hitelesíthetők az Azure Resource Manager kérései között.

## Példák

### 1. példa: profil kijelölése PSAzureProfile
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Ez a példa kijelöl egy profilt egy olyan PSAzureProfile, amely át lett adva a parancsmagnak.

### 2. példa: profil kiválasztása JSON-fájlból
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Ebben a példában egy JSON-fájlból kiválaszt egy profilt, amelyet a parancsmagnak továbbítanak. Ezt a JSON-fájlt a Save-AzureRmProfile hozhatja létre.

## PARAMÉTEREK

### -Path (elérési út)
A Save-AzureRMProfile használatával mentett profil-információk elérési útját adja meg.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### PSAzureProfile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRMContext]()

