---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016334"
---
# Get-AzureNetworkSecurityGroup

## Áttekintés
Megkeresi a hálózat biztonsági csoportjának részleteit.

## SZINTAXISA

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureNetworkSecurityGroup** parancsmag információt ad az Azure hálózat biztonsági csoportjairól.
A hálózati biztonsági szabályok megjelenítéséhez adja meg a *részletes* paramétert.

## Példák

## PARAMÉTEREK

### – Részletes
Jelzi, hogy ez a parancsmag a hálózatbiztonsági csoport hálózati biztonsági szabályait adja eredményül.

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

### -Name (név)
Annak a hálózati biztonsági csoportnak a neve, amely a parancsmagot kapja.

> [!NOTE]
> Ha egy klasszikus hálózati biztonsági csoportot az Azure portálon kívüli ***alapértelmezett hálózati*** kapcsolaton kívüli csoportba hoz létre, a következő PowerShell-szintaxist kell `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` használnia:

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

[Új – AzureNetworkSecurityGroup](./New-AzureNetworkSecurityGroup.md)

[Remove-AzureNetworkSecurityGroup](./Remove-AzureNetworkSecurityGroup.md)

