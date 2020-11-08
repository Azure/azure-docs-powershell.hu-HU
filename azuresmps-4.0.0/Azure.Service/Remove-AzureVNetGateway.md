---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015490"
---
# Remove-AzureVNetGateway

## Áttekintés
VPN-átjáró törlése

## SZINTAXISA

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureVNetGateway** parancsmag egy meglévő virtuális MAGÁNHÁLÓZATI (VPN-) átjárót töröl egy virtuális hálózathoz.

## Példák

### 1. példa: virtuális hálózati átjáró eltávolítása
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

Ez a parancs eltávolítja a virtuális hálózati átjárót a ContosoVN07 nevű virtuális hálózatból.

## PARAMÉTEREK

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

### -VNetName
Annak a virtuális hálózatnak a meghatározása, amelyben ez a parancsmag törli a VPN-átjárót.

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

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[Új – AzureVNetGateway](./New-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Átméretezés-AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Set-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


