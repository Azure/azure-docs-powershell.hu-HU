---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016277"
---
# Get-AzureVNetGatewayDiagnostics

## Áttekintés
A diagnosztika jelenlegi állapotát kapja egy virtuális hálózati átjáróhoz.

## SZINTAXISA

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureVNetGatewayDiagnostics** parancsmag a virtuális hálózati átjárók jelenlegi diagnosztikai állapotát kapja meg.
Ha egy olyan bináris nagy objektum (blob) létezik, ahol a **Start-AzureVNetGatewayDiagnostics** mentett egy korábbi diagnosztikai munkamenetet, ez a parancsmag azt is visszaküldi a blob URL-címére, amelyben a parancsmag a diagnosztikai munkamenetet mentette.

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
A virtuális hálózati átjárót tartalmazó virtuális hálózat, amelynek a parancsmagja a diagnosztikát kapja.

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

[Start-AzureVNetGatewayDiagnostics](./Start-AzureVNetGatewayDiagnostics.md)

[Stop-AzureVNetGatewayDiagnostics](./Stop-AzureVNetGatewayDiagnostics.md)


