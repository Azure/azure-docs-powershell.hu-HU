---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016051"
---
# Set-AzureRemoteAppWorkspace

## Áttekintés
Egy Azure RemoteApp-munkaterület tulajdonságainak beállítása.

## SZINTAXISA

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureRemoteAppWorkspace** parancsmag az Azure RemoteApp-munkaterület tulajdonságait állítja be.

## Példák

### Példa 1: a munkaterület nevének beállítása
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

Ez a parancs beállítja az Azure RemoteApp-munkaterület nevét a contoso Work Applications alkalmazásban.

## PARAMÉTEREK

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

### -WorkspaceName
Az Azure RemoteApp-munkaterület nevét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI
* A megadott előfizetéshez tartozó összes Azure RemoteApp-gyűjtemény létezik egy megosztott munkaterületen belül.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRemoteAppWorkspace](./Get-AzureRemoteAppWorkspace.md)


