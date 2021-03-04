---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 79fec34cee74dff5253724f91e07393fa65edad2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942402"
---
# Set-AzApplicationGatewayProbeConfig

## SYNOPSIS
Egy meglévő alkalmazásátjáró állapotkonfigurációját állítja be.

## SZINTAXIS

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A Set-AzApplicationGatewayProbeConfig parancsmag egy meglévő alkalmazás átjáró állapotkonfigurációját állítja be.

## PÉLDÁK

### 1. példa: Állapot állapotának beállítása egy alkalmazás-átjárón
```powershell
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

Ez a parancs beállítja az Átjáró nevű alkalmazás-átjáróhoz az 111111144-es állapotkezelő rendszer "10000000000" nevű állapotkezelő eszközének konfigurációját.
A parancs a nem megfelelő küszöbértéket is 8-ra állítja, és 120 másodperc elteltével időkorrektra állítja.

### 2. példa

Egy meglévő alkalmazásátjáró állapotkonfigurációját állítja be. (automatikusan generált)

<!-- Aladdin Generated Example -->
```powershell
Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Interval 30 -Match <PSApplicationGatewayProbeHealthResponseMatch> -Name 'Probe05' -Path '/path/custompath.htm' -PickHostNameFromBackendHttpSettings -Protocol https -Timeout 120 -UnhealthyThreshold 8
```

## PARAMETERS

### -ApplicationGateway
Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag adatokat küld.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostName
Azt a gazdanevet adja meg, amelybe a parancsmag elküldi a parancsmagot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Interval
Másodpercben megadja az intervallumot.
Ez két egymást követő sorozat között eltelt időintervallum.
Ez az érték 1 másodperc és 86400 másodperc között van.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Match
Az állapotra adott válaszban szereplő törzs.
Az alapértelmezett érték üres

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinServers
Azon kiszolgálók minimális száma, amelyek mindig kifogástalan állapotúként vannak megjelölve.
Az alapértelmezett érték 0

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A vizsgálat nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
A vizsgálat relatív elérési útját adja meg.
Az érvényes elérési utak perjellel (/) kezdődnek.
A teszt a következőnek \<Protocol\> lesz elküldve: : \<host\> \<port\> \<path\> .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PickHostNameFromBackendHttpSettings
Hogy az állomásfejlécet a háttér-http-beállítások között kell-e kivetni.
Az alapértelmezett érték hamis

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
A tamaksz küldését protokollja határozza meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timeout
A időkorlát másodpercben megadott időkorlátja.
Ez a parancsmag hibásnak jelöli a sérültet, ha nem érkezik érvényes válasz ebben az időkorlátban.
Az érvényes értékek 1 másodperc és 86400 másodperc között vannak.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnhealthyThreshold
Az újrapróbálkozás számát adja meg.
A háttérkiszolgáló le van jelölve, miután egymást követő sikertelen sikertelenségek száma elérte a nem megfelelő küszöbértéket.
Az érvényes értékek 1 másodperc és 20 másodperc között vannak.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[Get-AzApplicationGatewayProbeConfig](./Get-AzApplicationGatewayProbeConfig.md)

[New-AzApplicationGatewayProbeConfig](./New-AzApplicationGatewayProbeConfig.md)

[Remove-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

