---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: CD735391-62A8-40EC-B2F1-9044DC0676CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc46fb250a7bc76d05193ea231c81d61668e853
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016090"
---
# Reset-AzureVirtualNetworkGateway

## Áttekintés
Virtuális hálózati átjáró alaphelyzetbe állítása.

## SZINTAXISA

```
Reset-AzureVirtualNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **reset-AzureVirtualNetworkGateway** parancsmag visszaállítja a virtuális hálózati átjárót.

## Példák

## PARAMÉTEREK

### -GatewayId
Az átjáró AZONOSÍTÓját adja meg.

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

[Get-AzureVirtualNetworkGateway](./Get-AzureVirtualNetworkGateway.md)

[Új – AzureVirtualNetworkGateway](./New-AzureVirtualNetworkGateway.md)

[Remove-AzureVirtualNetworkGateway](./Remove-AzureVirtualNetworkGateway.md)

[Átméretezés-AzureVirtualNetworkGateway](./Resize-AzureVirtualNetworkGateway.md)


