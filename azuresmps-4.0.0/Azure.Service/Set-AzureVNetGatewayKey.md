---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015810"
---
# Set-AzureVNetGatewayKey

## Áttekintés
Az Azure VPN-átjáró és egy helyi hálózati webhely közötti kapcsolathoz tartozó előmegosztott kulcs beállítása.

## SZINTAXISA

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureVNetGatewayKey** parancsmag az Azure virtual private Network (VPN) átjáró és a helyszíni helyi hálózat webhelye közötti kapcsolat előmegosztott kulcsát állítja be.
A kulcsnak egyenlőnek kell lennie a helyi hálózati webhely átjáróján beállított kulccsal.
Ha a billentyűk nem egyeznek meg, a kapcsolat nem hozható létre.

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

### -SharedKey
A VPN-átjáróhoz hozzárendelni kívánt megosztott kulcsot adja meg.
Az értéknek a 128 karakternél nem hosszabb alfa-numerikus karakterláncnak kell lennie.

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

### -VNetName
Annak a virtuális hálózatnak a megadása, amelynek a parancsmagja a kapcsolat megosztott kulcsát állítja be.

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

[Get-AzureVNetGatewayKey](./Get-AzureVNetGatewayKey.md)


