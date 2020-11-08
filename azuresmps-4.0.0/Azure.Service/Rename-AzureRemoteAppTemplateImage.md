---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015474"
---
# Rename-AzureRemoteAppTemplateImage

## Áttekintés
Az Azure RemoteApp-sablon képének átnevezése

## SZINTAXISA

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Az **Rename-AzureRemoteAppTemplateImage** parancsmag az Azure RemoteApp-sablon képét átnevezi.

## Példák

### Példa 1: sablon átnevezése kép
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

Ez a parancs átnevezi az Azure RemoteApp template nevű ContosoApps a ContosoFinanceApps nevű képet.

## PARAMÉTEREK

### -ImageName
Annak az Azure RemoteApp-sablonnak a neve, amelyet átnevezni szeretne.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NewName
Új nevet ad az Azure RemoteApp-sablon képhez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
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

[Get-AzureRemoteAppTemplateImage](./Get-AzureRemoteAppTemplateImage.md)

[Új – AzureRemoteAppTemplateImage](./New-AzureRemoteAppTemplateImage.md)

[Remove-AzureRemoteAppTemplateImage](./Remove-AzureRemoteAppTemplateImage.md)


