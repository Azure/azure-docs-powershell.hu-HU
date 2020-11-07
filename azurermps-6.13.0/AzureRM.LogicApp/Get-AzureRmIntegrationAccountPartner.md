---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: c1fe4474ec7a35451c1f58c66c0b123d4d9d31b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679549"
---
# Get-AzureRmIntegrationAccountPartner

## Áttekintés
Bekerül az integrációs fiók partnereibe.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmIntegrationAccountPartner** parancsmag egy erőforráscsoport integrációs partnereivel válik elérhetővé.
Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a partner nevét.
Ez a modul támogatja a dinamikus paramétereket.
Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.
A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.
Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.

## Példák

### Példa 1: integrációs fiókpartner beszerzése
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
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
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

[Új – AzureRmIntegrationAccountPartner](./New-AzureRmIntegrationAccountPartner.md)

[Remove-AzureRmIntegrationAccountPartner](./Remove-AzureRmIntegrationAccountPartner.md)

[Set-AzureRmIntegrationAccountPartner](./Set-AzureRmIntegrationAccountPartner.md)


