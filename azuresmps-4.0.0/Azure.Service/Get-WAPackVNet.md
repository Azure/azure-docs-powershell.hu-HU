---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016263"
---
# Get-WAPackVNet

## Áttekintés
Virtuális hálózatokat kap.

## SZINTAXISA

### Üres (alapértelmezett)
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-WAPackVNet** parancsmag virtuális hálózatokat kap.

## Példák

### Példa 1: az összes virtuális hálózat beszerzése
```
PS C:\> Get-WAPackVNet
```

Ez a parancs a virtuális hálózatokat kapja.

### 2. példa: virtuális hálózat beszerzése azonosító használatával
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

Ez a parancs a megadott azonosítót tartalmazó virtuális hálózatot kapja.

### 3. példa: virtuális hálózat beszerzése név használatával
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

Ez a parancs a ContosoVNet08 nevű virtuális hálózatot kapja.

## PARAMÉTEREK

### -AZONOSÍTÓ
A virtuális hálózat egyedi AZONOSÍTÓját adja meg.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A virtuális hálózat nevét adja meg.

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
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

