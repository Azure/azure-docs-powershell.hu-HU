---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F380D98B-98EA-4013-8744-549A6F18C9B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04562bd9125617cfa9dbd76d47a3dd6c769e5b25
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016470"
---
# Remove-AzureLocalNetworkGateway

## Áttekintés
Azure helyi hálózati átjáró eltávolítása.

## SZINTAXISA

```
Remove-AzureLocalNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureLocalNetworkGateway** parancsmag eltávolítja az Azure local Network átjárót.

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

[Get-AzureLocalNetworkGateway](./Get-AzureLocalNetworkGateway.md)

[Új – AzureLocalNetworkGateway](./New-AzureLocalNetworkGateway.md)

[Reset-AzureLocalNetworkGateway](./Reset-AzureLocalNetworkGateway.md)


