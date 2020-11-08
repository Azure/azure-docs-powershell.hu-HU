---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016579"
---
# Get-AzureRemoteAppTemplateImage

## Áttekintés
Információt keres az Azure RemoteApp-sablon képeiről.

## SZINTAXISA

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRemoteAppTemplateImage** parancsmag információkat keres az Azure RemoteApp-sablon képeiről a Microsoft Azure-ban.
Ez a parancsmag egy olyan objektumot ad eredményül, amely a megadott sablon képével kapcsolatos információkat tartalmazza.
Ha nincs megadva sablon képe, az aktuális előfizetésben lévő összes sablon képéről információt olvas be.

## Példák

### Példa 1: az összes sablonból álló képek listájának beszerzése
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

Ez a parancs megjeleníti az összes sablon képeinek listáját.

### 2. példa: adatok beolvasása egy adott sablonról
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

Ez a parancs információkat olvas be a ContosoApps nevű sablon képéről.

## PARAMÉTEREK

### -ImageName
Egy Azure RemoteApp-sablon nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


