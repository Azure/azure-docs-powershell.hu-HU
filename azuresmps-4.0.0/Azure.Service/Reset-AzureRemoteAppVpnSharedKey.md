---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015471"
---
# Reset-AzureRemoteAppVpnSharedKey

## Áttekintés
Az Azure RemoteApp VPN megosztott kulcsának alaphelyzetbe állítása.

## SZINTAXISA

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **reset-AzureRemoteAppVpnSharedKey** parancsmag visszaállítja az Azure RemoteApp virtual private Network (VPN) megosztott kulcsát.

## Példák

### 1. példa: virtuális hálózat megosztott kulcsának alaphelyzetbe állítása
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

Ez a parancs visszaállítja a ContosoVNet nevű virtuális hálózat megosztott kulcsát.
A helyszíni hálózat VPN-kapcsolata offline állapotban marad mindaddig, amíg az új megosztott kulcs nincs konfigurálva a VPN-eszközön.
A VPN-eszköz konfigurálásához a **Get-AzureRemoteAppVpnDeviceConfigScript** parancsmaggal megkeresheti a megfelelő parancsfájl-vagy konfigurációs fájlt a VPN-eszközön, majd betölthet egy parancsfájlt vagy konfigurációs fájlt a VPN-eszközre.

## PARAMÉTEREK

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

### -VNetName
Az Azure RemoteApp virtuális hálózatának nevét adja meg.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. String

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRemoteAppVNet](./Get-AzureRemoteAppVNet.md)

[Get-AzureRemoteAppVpnDeviceConfigScript](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


