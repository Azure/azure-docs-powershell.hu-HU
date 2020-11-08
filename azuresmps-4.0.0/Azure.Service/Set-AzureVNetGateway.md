---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016414"
---
# Set-AzureVNetGateway

## Áttekintés
Engedélyezi vagy letiltja az Azure virtuális hálózat VPN-átjáróját.

## SZINTAXISA

### Connect (alapértelmezett)
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Leválasztása
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureVNetGateway** parancsmag engedélyezi vagy letiltja a virtuális MAGÁNHÁLÓZATI (VPN) átjárót egy Azure virtuális hálózathoz.
A virtuális hálózati átjáró a virtuális hálózathoz való csatlakozáshoz szükséges virtuális MAGÁNHÁLÓZATI végpont.
Adja meg a *Connect* vagy a *Disconnect* paramétert a VPN-kapcsolat engedélyezéséhez vagy letiltásához egy helyszíni helyi hálózati webhely és egy virtuális hálózat között.

## Példák

### 1. példa: virtuális hálózati átjáró engedélyezése virtuális hálózatokhoz
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Ez a parancs engedélyezi a virtuális hálózati átjárót a ContosoProdNet nevű Azure virtuális hálózat és a ContosoBranchOffice nevű helyi hálózati webhely VPN-eszköze között.

### 2. példa: virtuális hálózati átjáró letiltása virtuális hálózat esetén
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Ez a parancs letiltja a virtuális hálózati átjárót a ContosoProdNet nevű Azure virtuális hálózat és a ContosoBranchOffice nevű helyi hálózati webhely VPN-eszköze között.

## PARAMÉTEREK

### -Connect
Azt jelzi, hogy ez a parancsmag lehetővé teszi a virtuális hálózat és a helyi hálózati webhely közötti VPN-kapcsolat használatát.

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disconnect
Jelzi, hogy ez a parancsmag letiltja a virtuális hálózat és a helyi hálózati webhely közötti VPN-kapcsolatot.

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
Annak a helyszíni helyi hálózati webhelynek a neve, amelyhez ez a parancsmag engedélyezi vagy letiltja a VPN-kapcsolatot.

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
Annak a virtuális hálózatnak a megadása, amelyhez ez a parancsmag engedélyezi vagy letiltja a VPN-kapcsolatot.

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

[Átméretezés-AzureVNetGateway](./Resize-AzureVNetGateway.md)


