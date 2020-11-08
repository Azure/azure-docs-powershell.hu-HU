---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016019"
---
# Stop-AzureVNetGatewayDiagnostics

## Áttekintés
Egy futó VPN-átjáró diagnosztikai munkamenetének leállítása.

## SZINTAXISA

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **stop-AzureVNetGatewayDiagnostics** parancsmag leállítja a virtuális MAGÁNHÁLÓZATI (VPN-) átjáró diagnosztikai munkamenetét.
Ez a parancs a diagnosztikai munkamenet eredményét a **Start-AzureVNetGatewayDiagnostics** parancsmag által megadott tárolási fiókba menti.

## Példák

## PARAMÉTEREK

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
Azt a virtuális hálózati átjárót tartalmazó virtuális hálózat, amelyhez ez a parancsmag leállítja a diagnosztikát.

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

[Start-AzureVNetGatewayDiagnostics](./Start-AzureVNetGatewayDiagnostics.md)


