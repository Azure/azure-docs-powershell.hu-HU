---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491907"
---
# Set-AzureRmFirewall

## Áttekintés
Módosított tűzfal mentése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmFirewall** parancsmag egy Azure-tűzfalat frissít.

## Példák

### 1: a tűzfal-alkalmazási szabályok gyűjteményének frissítési prioritása
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

Ez a példa frissíti egy Azure-tűzfal meglévő szabálykészlet-gyűjteményének prioritását.
Feltételezve, hogy az Azure Firewall "AzureFirewall" az erőforráscsoport "RG" nevű ruleCollectionName tartalmaz, a fenti parancsok a szabály-gyűjtemény prioritását fogják módosítani, majd később frissítik az Azure tűzfalat. A Set-AzureRmFirewall parancs nélkül a helyi $azFw-objektumon végrehajtott összes művelet nem tükröződik a kiszolgálón.

### 2: Azure-tűzfal létrehozása és egy alkalmazási szabály gyűjteményének beállítása később
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

Ebben a példában a tűzfal először az alkalmazási szabályok gyűjteménye nélkül jön létre. Ezt követően egy alkalmazási szabály és egy alkalmazási szabály gyűjtemény jön létre, a tűzfal objektum a memóriában módosul, és nem befolyásolja a Felhőbeli valós konfigurációt. Ha a változásokat a felhőben szeretné tükrözni, Set-AzureRmFirewall kell nevezni.

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben

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

### -AzureFirewall
A AzureFirewall

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSAzureFirewall
A ' AzureFirewall ' paraméter az "PSAzureFirewall" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSAzureFirewall

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)

[Új – AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)
