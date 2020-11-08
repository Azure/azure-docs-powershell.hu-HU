---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016549"
---
# Get-AzureStorSimpleResourceContext

## Áttekintés
Az aktuális erőforrás környezetének beolvasása

## SZINTAXISA

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleResourceContext** parancsmag a jelenlegi erőforrás-környezetet kapja.

## Példák

### Példa 1: az aktuális környezet beszerzése
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

Az első parancs a **Select-AzureStorSimpleResource** parancsmaggal állítja be az aktuális környezetet a Contoso63-Tsqa nevű erőforráshoz.

A második parancs a jelenlegi erőforrás-környezetet kapja.

### 2. példa: az aktuális környezet beszerzésének kísérlete
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

Ez a parancs a jelenlegi környezetet kapja.
Ebben a példában nincs beállítva környezet.
A parancs olyan üzenetet ad eredményül, amely ismerteti a problémát.

## PARAMÉTEREK

### -Profil
Egy Azure-profilt ad meg.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### StorSimpleResourceContext
Ez a parancsmag egy **ResourceContext** objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Select-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


