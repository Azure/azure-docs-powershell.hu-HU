---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016087"
---
# Resize-AzureVNetGateway

## Áttekintés
VPN-átjáró átméretezése

## SZINTAXISA

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Az **átméretezés-AzureVNetGateway** parancsmag a virtuális hálózat virtuális MAGÁNHÁLÓZATI (VPN) átjáróját egy másik SKU-ba méretezi át.
A virtuális hálózati átjáró érvényes SKU-je alapértelmezés szerint normál és HighPerformance.

## Példák

### Példa 1: virtuális hálózati átjáró SKU-ának módosítása
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

Ez a parancs a virtuális hálózati átjáró SKU-ContosoVN07 a HighPerformance nevű virtuális hálózat számára módosítja.

## PARAMÉTEREK

### -GatewaySKU
Azt a SKU-ot adja meg, amelyre ez a parancsmag átméretezi a virtuális hálózati átjárót.
Az érvényes értékek a következők: 

- Alapértelmezett 
- Standard 
- HighPerformance

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
Annak a virtuális hálózatnak a meghatározása, amelyben ez a parancsmag átméretezi a virtuális hálózati átjárót.

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

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Set-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


