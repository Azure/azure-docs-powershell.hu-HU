---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016026"
---
# Start-AzureVNetGatewayDiagnostics

## Áttekintés
Átjáró diagnosztikát indít a VPN-átjáróhoz.

## SZINTAXISA

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Start-AzureVNetGatewayDiagnostics** parancsmag új átjáró-diagnosztikai munkamenetet indít egy virtuális magánhálózati (VPN-) átjáróhoz.
Egyszerre csak egy átjáró-diagnosztikai munkamenet futhat.
Ha futtatja ezt a parancsmagot egy átjáró-diagnosztikai munkamenet futása közben, ez a parancsmag hibát jelez.

## Példák

## PARAMÉTEREK

### -CaptureDurationInSeconds
A rögzítés időtartamát adja meg másodpercben.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerName
Egy Azure-tároló nevét adja meg.
Ez a parancsmag a paraméter által megadott tárolóba menti a találatokat.

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

### -StorageContext
Az Azure tárolási környezetét adja meg.
Ez a parancsmag a paraméter által megadott tárolási környezettel menti az eredményeket.

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Azt a virtuális hálózati átjárót tartalmazó virtuális hálózat, amelyhez ez a parancsmag futtatja a diagnosztikát.

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

[Get-AzureVNetGatewayDiagnostics](./Get-AzureVNetGatewayDiagnostics.md)

[Stop-AzureVNetGatewayDiagnostics](./Stop-AzureVNetGatewayDiagnostics.md)


