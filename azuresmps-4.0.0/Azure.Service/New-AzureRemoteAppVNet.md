---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015994"
---
# New-AzureRemoteAppVNet

## Áttekintés
Azure RemoteApp virtuális hálózatot hoz létre.

## SZINTAXISA

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureRemoteAppVNet** parancsmag létrehoz egy Azure RemoteApp virtuális hálózatot.

## Példák

### Példa 1: virtuális hálózat létrehozása
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

Ez a parancs létrehoz egy ContosoVNet nevű virtuális hálózatot.

A művelet állapotának meghatározásához használja a **Get-AzureRemoteAppOperationResult** parancsmagot annak a NYOMKÖVETÉSi azonosítónak a megadásával, amelyet a parancsmag ad eredményül.

## PARAMÉTEREK

### -DnsServerIpAddress
A DNS-kiszolgálók IPv4-címeinek tömbjét adja meg.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -GatewayType
A használni kívánt átjáró típusának meghatározása.
A paraméter elfogadható értékei a következők: StaticRouting vagy DynamicRouting.

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LocalNetworkAddressSpace
Olyan karakterláncokat ad meg, amelyek megadják a helyi hálózati címtartomány, az osztály nélküli többtartományos útválasztási (CIDR) jelölést.
Ez a Címterület nem fedi át a virtuális hálózati címterület által az *VirtualNetworkAddressSpace* paraméter által megadott helyet.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Hely
A virtuális hálózat létrehozásának helyét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
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

### -VirtualNetworkAddressSpace
Olyan karakterláncot ad meg, amely megadja a virtuális hálózati címterület CIDR jelölését.
Ennek a magánhálózati IP-címtartomány-tartománynak kell lennie, és nem lehet átfedésben a *LocalNetworkAddressSpace* paraméter által megadott helyi hálózati címterület segítségével.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VNetName
Az Azure RemoteApp virtuális hálózatának nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VpnDeviceIpAddress
A virtuális magánhálózat (VPN) eszköz címét adja meg.
Ennek csak nyilvános címnek kell lennie.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRemoteAppOperationResult](./Get-AzureRemoteAppOperationResult.md)

[Get-AzureRemoteAppVNet](./Get-AzureRemoteAppVNet.md)

[Remove-AzureRemoteAppVNet](./Remove-AzureRemoteAppVNet.md)

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


