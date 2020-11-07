---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 3696b33b18314d58e950fa9786e1febac5c3d22c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843701"
---
# Set-AzApplicationGatewayBackendHttpSetting

## Áttekintés
Az alkalmazás-átjárók végfelhasználói HTTP-beállításainak frissítése

## SZINTAXISA

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A Set-AzApplicationGatewayBackendHttpSetting parancsmag frissíti az Azure-alkalmazások átjárójának HTTP-beállításait.
A back-end HTTP-beállítások a készlet minden back-end kiszolgálójára érvényesek.

## Példák

### Példa 1: az alkalmazás-átjárók back-end HTTP-beállításainak frissítése
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.

A második parancs frissíti a $AppGw változóban lévő alkalmazás-átjáró HTTP-beállításait a 88-as port, a HTTP-protokoll és a cookie-alapú affinitás használatához.

## PARAMÉTEREK

### -AffinityCookieName
Az affinitáshoz használt cookie-név

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

### -ApplicationGateway
Itt adhatja meg azt az alkalmazásobjektum-objektumot, amelynek a parancsmagja a back-end HTTP-beállításait társítja.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AuthenticationCertificates
Az Application Gateway hitelesítési tanúsítványait adja meg.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionDraining
A backend http Settings erőforrás kapcsolatának kiürítése

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CookieBasedAffinity
Azt adja meg, hogy engedélyezve van-e a cookie-alapú affinitás a backend Server-készlethez, vagy le legyen tiltva.
A paraméter elfogadható értékei a következők: letiltva vagy engedélyezve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Beállítja az állomásfejléc-ot, amelyet a backend-kiszolgálókra kell elküldeni.

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

### -Name (név)
A back-end HTTP Settings objektum nevét adja meg.

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
Az elérési út, amelyet az összes HTTP-kéréshez előtagként kell használni.
Ha a paraméterhez nincs megadva érték, akkor a program nem fogja előre rögzíteni az elérési utat.

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

### -PickHostNameFromBackendAddress
Megjelölés ha az állomás fejlécét a backend-kiszolgáló állomásnevét kell választani.

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

### -Port
Megadja, hogy melyik portot használja az egyes kiszolgálók a back-end Server-készletben.

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

### -Szonda
A back-end HTTP-beállításaival társítani kívánt szondát adja meg.

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeEnabled
Megjelölés ha a szonda engedélyezve van.

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

### -ProbeId
Annak a szondanak az AZONOSÍTÓját adja meg, amely a back-end HTTP-beállításaihoz társítva van.

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

### -Protocol
Az Application Gateway és a back-end-kiszolgálók közötti kommunikációhoz használandó protokollt adja meg.
A paraméter elfogadható értékei a következők: http és HTTPS.
Ez a paraméter megkülönbözteti a kis-és nagybetűket.

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

### -RequestTimeout
A kérés időtúllépési értékét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSApplicationGateway

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzApplicationGatewayBackendHttpSetting]()

[Get-AzApplicationGatewayBackendHttpSetting]()

[Új – AzApplicationGatewayBackendHttpSetting]()

[Remove-AzApplicationGatewayBackendHttpSetting]()

