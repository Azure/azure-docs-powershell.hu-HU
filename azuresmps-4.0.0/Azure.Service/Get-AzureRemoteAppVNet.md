---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016570"
---
# Get-AzureRemoteAppVNet

## Áttekintés
Információt keres az Azure RemoteApp virtuális hálózatáról az Azure-ban.

## SZINTAXISA

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRemoteAppVNet** parancsmag információkat keres az Azure RemoteApp virtuális hálózatokról a Microsoft Azure-ban.
Ez a parancsmag egy olyan objektumot ad eredményül, amely a megadott virtuális hálózatról tartalmaz információkat.
Ha nincs megadva virtuális hálózat, ez a parancsmag információt ad az aktuális előfizetésben lévő összes virtuális hálózatról.

## Példák

### Példa 1: virtuális hálózat adatainak beolvasása
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

Ez a parancs információkat kap a ContosoVNet nevű virtuális hálózatról.

## PARAMÉTEREK

### -IncludeSharedKey
Azt jelzi, hogy ez a parancsmag a virtuális hálózatról beolvasott adatok megosztott kulcs értékét tartalmazza.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -VNetName
Az Azure RemoteApp virtuális hálózatának nevét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


