---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015625"
---
# Get-AzureRemoteAppVpnDeviceConfigScript

## Áttekintés
Beolvassa az Azure RemoteApp VPN-eszközök konfigurációs parancsfájlját.

## SZINTAXISA

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRemoteAppVpnDeviceConfigScript** parancsmag beolvassa az Azure RemoteApp virtual private Network (VPN) eszközök konfigurációs parancsfájlját.

## Példák

### Példa 1: konfigurációs parancsfájl beszerzése VPN-eszközön
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

Ez a parancs azt a parancsfájl-vagy konfigurációs fájlt adja eredményül, amely a ContosoVNet nevű virtuális hálózat VPN-eszközének konfigurálására szolgál.
Ezt a parancsfájl-vagy konfigurációs fájlt a megfelelő módon kell futtatni vagy betölteni a VPN-eszközre.
Tekintse meg az egyes eszközökre vonatkozó egyedi követelményeket a VPN-eszköz forgalmazójától.

## PARAMÉTEREK

### -OSFamily
Annak az operációs rendszernek a családját adja meg, amely az eszköz platformján fut.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Platform
Az eszköz platformját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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

### -Vendor
A VPN-eszköz szállítóját adja meg.

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

### -VNetName
Egy Azure RemoteApp virtuális hálózat nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

[Get-AzureRemoteAppVpnDevice](./Get-AzureRemoteAppVpnDevice.md)


