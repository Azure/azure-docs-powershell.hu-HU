---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 22a9c9b11063dfd9a84e8ecf292af6e9e0f7f97f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835201"
---
# Get-AzMarketplaceTerms

## Áttekintés
Az adott közzétevői azonosító (közzétevő), ajánlati azonosító (PRODUCT) és Plan azonosító (név) szerződési feltételeinek beszerzése. Az e parancs által visszaadott kitételeket a program átadja Set-AzMarketplaceTerms a jogi fogalmak elfogadásához.

## SZINTAXISA

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzMarketplaceTerms** parancsmag a Publisher-azonosító (Publisher), az ajánlat-azonosító (PRODUCT) és a Plan ID (név) rekord feltételeit adja eredményül.

## Példák

### Példa 1
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Name (név)
A telepítendő kép terv azonosító karakterlánca.

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

### -Szorzat
A telepített lemezkép azonosító karakterlánca.

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

### -Publisher
A telepítendő lemezkép közzétevő azonosító karakterlánca.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
