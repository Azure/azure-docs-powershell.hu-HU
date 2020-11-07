---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: c1f96d462d1556078159d70a47a9869ec21a0e63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835506"
---
# Get-AzIntegrationAccountPartner

## Áttekintés
Bekerül az integrációs fiók partnereibe.

## SZINTAXISA

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzIntegrationAccountPartner** parancsmag egy erőforráscsoport integrációs partnereivel válik elérhetővé.
Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a partner nevét.
Ez a modul támogatja a dinamikus paramétereket.
Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.
A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.
Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.

## Példák

### Példa 1: integrációs fiókpartner beszerzése
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

Ez a parancs beolvassa a IntegrationAccountPartner22 nevű integrációs fiókpartner-partnert.

### 2. példa: integrációs fiókkal rendelkező partnerek beszerzése az integrációs fiók nevének használatával
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

Ez a parancs beilleszti a IntegrationAccount31 nevű integrációs fiók integrációs fiókjának partnereit.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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
Az integrációs fiók nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerName
Az integrációs fiókpartner nevét adja meg.

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

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.

```yaml
Type: System.String
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

### System. String

## KIMENETEK

### Microsoft. Azure. Management. Logic. models. IntegrationAccountPartner

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzIntegrationAccountPartner](./New-AzIntegrationAccountPartner.md)

[Remove-AzIntegrationAccountPartner](./Remove-AzIntegrationAccountPartner.md)

[Set-AzIntegrationAccountPartner](./Set-AzIntegrationAccountPartner.md)


