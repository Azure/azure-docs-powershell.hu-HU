---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016508"
---
# Get-WAPackCloudVMRoleSizeProfile

## Áttekintés
Cloud VM-szerepkörök méretének lekérdezési objektumait kapja.

## SZINTAXISA

### Üres (alapértelmezett)
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-WAPackCloudVMRoleSizeProfile** parancsmag a virtuális gépek felhőalapú VM-beli szerepkör-profil objektumait kapja.

## Példák

### Példa 1: felhőalapú VM-beli szerepkör-méret profiljának beszerzése név használatával
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

Ez a parancs a Small nevű méret profilt kapja.

### 2. példa: a felhőalapú VM-szerepkörök méret-profiljainak beolvasása
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

Ez a parancs a teljes méretű profilokat kapja.

## PARAMÉTEREK

### -Name (név)
A Felhőbeli VM-szerepkörök méretére vonatkozó profil nevét adja meg.

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Get-WAPackVM](./Get-WAPackVM.md)


