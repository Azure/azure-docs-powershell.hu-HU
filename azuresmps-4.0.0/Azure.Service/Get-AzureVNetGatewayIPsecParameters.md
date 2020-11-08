---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016276"
---
# Get-AzureVNetGatewayIPsecParameters

## Áttekintés
A virtuális hálózati átjáró és a helyi hálózati webhely közötti kapcsolat IPsec-paramétereit kapja meg.

## SZINTAXISA

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureVNetGatewayIPsecParameters** parancsmag az Internet Protocol Security (IPSec) és az internetes KULCSCSERE (IKE) paramétereit kapja meg a virtuális hálózati átjáró és egy helyi hálózati webhely közötti kapcsolathoz.

## Példák

## PARAMÉTEREK

### -LocalNetworkSiteName
Annak a helyi hálózati webhelynek a neve, amely a virtuális hálózati átjáróhoz csatlakozik.

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

### -VNetName
Annak a virtuális hálózatnak a megadása, amelyhez ez a parancsmag az IPsec-paramétereket kapja a kapcsolathoz.

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

[Set-AzureVNetGatewayIPsecParameters](./Set-AzureVNetGatewayIPsecParameters.md)


