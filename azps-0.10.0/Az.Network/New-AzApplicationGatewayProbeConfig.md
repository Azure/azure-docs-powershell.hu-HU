---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 43c74d2edd2cfd07f65b7d5437bf1cf5c0dfca9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841406"
---
# New-AzApplicationGatewayProbeConfig

## Áttekintés
Létrehoz egy egészségi szondát.

## SZINTAXISA

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az New-AzApplicationGatewayProbeConfig parancsmag létrehoz egy állapottanúsítvány-adatszondát.

## Példák

### Example1: állapot-szonda létrehozása
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

Ez a parancs létrehoz egy Probe03 nevű, HTTP protokollt tartalmazó, 30 másodperces, 120 másodperces időkorlátot, valamint 8 újrapróbálkozáskor egy egészségtelen küszöböt.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostName (állomásnév)
Azt az állomásnevet adja meg, amelyre a parancsmag elküldi a szonda nevet.

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

### -Intervallum
A szonda intervallumát másodpercben kifejezve adja meg.
Ez a két egymást követő szonda közötti időtartam.
Ez az érték 1 másodperc és 86400 másodperc között van.

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

### -Hol. van
Az egészségvédelmi válaszban szerepelnie kell.
Az alapértelmezett érték üres

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinServers
A mindig egészségesként megjelölt kiszolgálók minimális száma.
Az alapértelmezett érték 0

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A szonda nevét adja meg.

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

### -Path (elérési út)
A szonda relatív elérési útját adja meg.
Az érvényes elérési utak a perjel karakterrel (/) kezdődnek.
A szondát a rendszer elküldi a következő \< protokollnak \> ::// \< Host \> : \< port \> \< path \> .

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

### -PickHostNameFromBackendHttpSettings
Azt, hogy az állomásfejléc a backend http-beállításai között legyen-e kiválasztva.
Az alapértelmezett érték a hamis

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
A szonda küldéséhez használt protokollt adja meg.

```yaml
Type: String
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
A szonda időkorlátját adja meg másodpercben.
Ez a parancsmag a szondát hibásnak minősíti, ha az időtúllépési időszakmal nem érkezik érvényes válasz.
Az érvényes értékek 1 másodperc és 86400 másodperc között jelennek meg.

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

### -UnhealthyThreshold
A szonda ismételt ismételt számát adja meg.
A backend-kiszolgáló az egymást követő Szondák meghibásodása után nem éri el az egészségtelen küszöböt.
Az érvényes értékek 1 másodperc és 20 másodperc között jelennek meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Egyéni szonda létrehozása az alkalmazás-átjáróhoz az Azure Resource Manager PowerShell használatával](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[Add-AzApplicationGatewayProbeConfig]()

[Get-AzApplicationGatewayProbeConfig]()

[Remove-AzApplicationGatewayProbeConfig]()

[Set-AzApplicationGatewayProbeConfig]()

