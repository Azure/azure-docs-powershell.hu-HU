---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016413"
---
# Set-AzureVNetGatewayDefaultSite

## Áttekintés
A kényszerített bújtatási forgalom alapértelmezett webhelyének beállítása.

## SZINTAXISA

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureVNetGatewayDefaultSite** parancsmag az alapértelmezett útvonalat állítja be a helyszíni webhelyre a kényszerített bújtatási forgalom eléréséhez.
Ez a parancs a virtuális hálózatokra vonatkozóan egy Azure virtuális magánhálózati (VPN-) átjáró útvonalát állítja be.

## Példák

## PARAMÉTEREK

### -DefaultSite
A helyszíni helyi hálózat webhelyének nevét adja meg a kényszeres bújtatási forgalomhoz.

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
Virtuális hálózatot ad meg.
Ez a parancsmag a VPN-átjáró alapértelmezett útvonalát állítja be a virtuális hálózat számára, amelyet ez a paraméter határoz meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureVNetGatewayDefaultSite](./Remove-AzureVNetGatewayDefaultSite.md)
