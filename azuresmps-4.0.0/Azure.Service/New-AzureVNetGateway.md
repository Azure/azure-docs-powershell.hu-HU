---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016187"
---
# New-AzureVNetGateway

## Áttekintés
Virtuális hálózatban VPN-átjárót hoz létre.

## SZINTAXISA

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureVNetGateway** parancsmag virtuális MAGÁNHÁLÓZAT (VPN) átjárót hoz létre virtuális hálózatban.
Az átjáró SKU-ának alapértelmezett, normál vagy HighPerformance is megadható.
Megadhatja, hogy milyen típusú, vagy StaticRouting vagy DynamicRouting.

## Példák

### Példa 1: virtuális hálózati átjáró létrehozása
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

Ez a parancs virtuális hálózati átjárót hoz létre a ContosoVN07 nevű virtuális hálózathoz.
Az átjáró az alapértelmezett SKU, és dinamikus művelettervet használ.

## PARAMÉTEREK

### -GatewaySKU
Annak a virtuális hálózati átjárónak az SKU-számát adja meg, amelyre a parancsmag létrehozta.
Az érvényes értékek a következők: 

- Alapértelmezett 
- Standard 
- HighPerformance

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

### -GatewayType
A parancsmag által létrehozott átjáró típusát adja meg.
Az érvényes értékek a következők: 

- StaticRouting 
- DynamicRouting

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
Annak a virtuális hálózatnak a megadása, amelyben ez a parancsmag virtuális hálózati átjárót ad hozzá.

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

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Átméretezés-AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Set-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


