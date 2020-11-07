---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841409"
---
# New-AzApplicationGatewayPathRuleConfig

## Áttekintés
Az alkalmazás-átjáró elérési útjának szabályát hozza létre.

## SZINTAXISA

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzApplicationGatewayPathRuleConfig** parancsmag az alkalmazás-átjáró elérési útjának szabályát hozza létre.
Az e parancsmaggal létrehozott szabályok hozzáadhatók az URL-elérésiút-Térkép konfigurációs beállításainak gyűjteményéhez, majd a hozzájuk rendelt átjáróhoz.

Az elérésiút-Térkép konfigurációs beállításait az Application Gateway terheléselosztási funkciói használja.

## Példák

### Példa 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Ezekkel a parancsokkal új alkalmazás-átjáró elérésiút-szabályt hozhat létre, majd az **Add-AzApplicationGatewayUrlPathMapConfig** parancsmaggal társíthatja ezt a szabályt egy alkalmazás-átjáróhoz.
Ehhez az első parancs objektumra mutató hivatkozást hoz létre az átjáró ContosoApplicationGateway.
Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.

A következő két parancs a backend-címkészletet és a backend-alapú HTTP-beállítások objektumot hozza létre; Ezek az objektumok (a változók $AddressPool és a $HttpSettings) szükségesek az elérésiút-szabály objektum létrehozása érdekében.

A negyedik parancs a Path Rule objektumot hozza létre, és a $PathRuleConfig nevű változóban tárolja.

Az ötödik parancs az **Add-AzApplicationGatewayUrlPathMapConfig** használatával hozzáadja a konfigurációs beállításokat és az új elérésiút-szabályt a beállítások között a ContosoApplicationGateway.

## PARAMÉTEREK

### -BackendAddressPool
Itt adhatja meg a backend-címkészlet beállításai között az objektum hivatkozását, amelyet az átjáró elérési útjának konfigurációs beállításaihoz kell hozzáadni.
Az objektum hivatkozását az New-AzApplicationGatewayBackendAddressPool parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre:

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

Az előző parancs két IP-címet (192.16.1.1 és 192.168.1.2) ad hozzá a címkészlet számára.
Ügyeljen arra, hogy az IP-cím idézőjelek közé van írva, és vesszőkkel elválasztva.

Az eredményül kapott változó ($AddressPool) a *DefaultBackendAddressPool* paraméter paraméterének értéke lehet.

A backend Address Pool a backend-kiszolgálók IP-címét jelöli.
Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.
Ha ezt a paramétert használja, a *DefaultBackendAddressPoolId* paraméter nem használható ugyanabban a parancsban.

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Annak a meglévő backend-címkészlet az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.
A címkészlet-azonosítók az Get-AzApplicationGatewayBackendAddressPool parancsmag használatával adhatók vissza.
Miután megtörtént az azonosító, a *DefaultBackendAddressPoolId* paramétert használhatja a *DefaultBackendAddressPool* paraméter helyett.
Például:

-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"

A backend Address Pool a backend-kiszolgálók IP-címét jelöli.
Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettings
Az átjáró elérési útjának konfigurációs beállításaihoz hozzáadott backend-HTTP-beállításokra mutató objektum hivatkozását adja meg.
Az objektum hivatkozását az New-AzApplicationGatewayBackendHttpSetting parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre:

$HttpSettings = New-AzApplicationGatewayBackendHttpSetting név "ContosoHttpSetings"-port 80-Protocol "http"-CookieBasedAffinity "disabled"

Az eredményül kapott változó ($HttpSettings) a *DefaultBackendAddressPool* paraméter paraméterének értéke lehet:

-DefaultBackendHttpSettings $HttpSettings

A backend HTTP-beállításai olyan tulajdonságokat (például portot, protokollt és cookie-alapú affinitást) konfigurálnak, amelyek a backend-készletekhez használhatók.
Ha ezt a paramétert használja, a *DefaultBackendHttpSettingsId* paraméter nem használható ugyanabban a parancsban.

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Annak a meglévő backend-adatgyűjteménynek az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.
A HTTP-beállítás azonosítói az Get-AzApplicationGatewayBackendHttpSetting parancsmag használatával adhatók vissza.
Miután megtörtént az azonosító, a *DefaultBackendHttpSettingsId* paramétert használhatja a *DefaultBackendHttpSettings* paraméter helyett.
Például:

-DefaultBackendSettings-azonosító "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"

A backend HTTP-beállításai olyan tulajdonságokat (például portot, protokollt és cookie-alapú affinitást) konfigurálnak, amelyek a backend-készletekhez használhatók.
Ha ezt a paramétert használja, a *DefaultBackendHttpSettings* paraméter nem használható ugyanabban a parancsban.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
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

### -Name (név)
A parancsmag által létrehozott elérésiút-szabály konfigurációjának nevét adja meg.

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

### -Paths
Egy vagy több alkalmazásobjektum-elérésiút-szabályt ad meg.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
Az Application Gateway RedirectConfiguration

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
Az alkalmazás-átjáró RedirectConfiguration azonosítója

```yaml
Type: String
Parameter Sets: SetByResourceId
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

###  
A **New-AzApplicationGatewayPathRuleConfig** nem fogadja el a csővezetékes bevitelt.

## KIMENETEK

###  
A **New-AzApplicationGatewayPathRuleConfig** a **Microsoft. Azure. commands. Network. models. PSApplicationGatewayPathRule** objektum új példányait hozza létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[Új – AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[Új – AzApplicationGatewayBackendHttpSetting](./New-AzApplicationGatewayBackendHttpSetting.md)

[Új – AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[Új – AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


