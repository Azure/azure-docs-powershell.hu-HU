---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015910"
---
# New-AzureNetworkSecurityGroup

## Áttekintés
Azure-hálózati biztonsági csoportot hoz létre.

## SZINTAXISA

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureNetworkSecurityGroup** parancsmag az Azure hálózat biztonsági csoportját hozza létre egy helyen.

## Példák

## PARAMÉTEREK

### -Label (címke)
Az új hálózati biztonsági csoport leírását adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
Azt az Azure-helyet adja meg, ahol a parancsmag hálózati biztonsági csoportot hoz létre.
Ha érvényes helyeket szeretne beolvasni, használja az Get-AzureLocation parancsmagot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Az új hálózati biztonsági csoport nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

[Get-AzureNetworkSecurityGroup](./Get-AzureNetworkSecurityGroup.md)


