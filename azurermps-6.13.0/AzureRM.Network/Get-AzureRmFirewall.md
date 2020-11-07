---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680329"
---
# Get-AzureRmFirewall

## Áttekintés
Azure-tűzfalat kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmFirewall** parancsmag egy vagy több tűzfalat kap egy erőforráscsoportben.

## Példák

### 1: az összes tűzfal lekérése egy erőforrás csoportban
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

Ebben a példában a "rgName" erőforráscsoporthoz tartozó összes tűzfalat beolvassa.

### 2: tűzfal beolvasása név szerint
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

Ez a példa a "azFw" nevű tűzfalat olvassa be a "rgName" erőforráscsoport nevében.

### 3: a tűzfal lekérése, majd az alkalmazási szabályok gyűjteményének hozzáadása a tűzfalhoz
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

Ez a példa beolvassa a tűzfalat, majd felvesz egy alkalmazási szabályt a tűzfalba a hívási mód AddApplicationRuleCollection.

### 4: a tűzfal lekérése, majd a hálózati szabályok gyűjteményének hozzáadása a tűzfalhoz
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

Ez a példa beolvassa a tűzfalat, majd egy hálózati szabály gyűjteményt ad a tűzfalhoz a hívási mód AddNetworkRuleCollection.

### 5: a tűzfal lekérése, majd egy alkalmazási szabály gyűjteményének beolvasása a tűzfalból
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

Ez a példa beolvassa a tűzfalat, és a GetApplicationRuleCollectionByName a tűzfal objektumon név szerint begyűjti a szabályok gyűjteményét. A szabály GetApplicationRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.

### 6: a tűzfal lekérése, majd egy hálózati szabály-gyűjtemény beolvasása a tűzfalból
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

Ez a példa beolvassa a tűzfalat, és a GetNetworkRuleCollectionByName a tűzfal objektumon név szerint begyűjti a szabályok gyűjteményét. A szabály GetNetworkRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.

### 7: a tűzfal lekérése, majd az alkalmazás szabály-gyűjteményének eltávolítása a tűzfalból
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

Ez a példa beolvassa a tűzfalat, majd eltávolítja a szabályok gyűjteményét név szerint, a hívási mód RemoveApplicationRuleCollectionByName a tűzfal objektumon. A szabály RemoveApplicationRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.

### 8: a tűzfal lekérése, majd egy hálózati szabály-gyűjtemény eltávolítása a tűzfalból
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

Ez a példa beolvassa a tűzfalat, majd eltávolítja a szabályok gyűjteményét név szerint, a hívási mód RemoveNetworkRuleCollectionByName a tűzfal objektumon. A szabály RemoveNetworkRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.

### 9: a tűzfal lekérése, majd a tűzfal lefoglalása
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

Ebben a példában egy tűzfal és a hívások lefoglalása a tűzfalon a tűzfalhoz társított konfiguráció (alkalmazás és hálózati szabály gyűjtemény) segítségével indítható el.

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

### -Name (név)
Annak a tűzfalnak a neve, amely a parancsmagot kapja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csoportnak a neve, amelyhez a tűzfal tartozik.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSAzureFirewall

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
