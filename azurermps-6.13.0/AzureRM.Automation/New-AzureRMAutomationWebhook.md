---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: 97b9c37613563f269ba035062ba557de810e9ec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671990"
---
# New-AzureRmAutomationWebhook

## Áttekintés
Egy webkampót hoz létre automatizálási runbook.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureRmAutomationWebhook** parancsmag egy webhorogot hoz létre az Azure automatizálási runbook.
Ügyeljen arra, hogy mentse a parancsmag által visszaadott webhook-URL-címet, mert az nem olvasható vissza.

## Példák

### Példa 1: webhook létrehozása
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

Ez a parancs létrehoz egy Webhook06 nevű webkampót a AutomationAccount01 nevű automatizálási fiók ContosoRunbook nevű runbook.
A parancs a $Webhook változóban tárolja a webkampót.
A webhook engedélyezve van.
A webhook a megadott időpontban lejár.
Ez a parancs nem ad értéket a webhook paraméternek.
Ez a parancs az *erő* paramétert adja meg.
Ezért nem kéri a megerősítést.

### 2. példa: webkampó létrehozása paraméterekkel
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

Az első parancs létrehozza a paraméterek szótárát, és a $Params változóban tárolja őket.
A második parancs létrehoz egy Webhook11 nevű webkampót a ContosoRunbook nevű runbook nevű a AutomationAccount01 nevű automatizálási fiókban.
A parancs kiosztja a paramétereket $Params a webhook-hoz.

## PARAMÉTEREK

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag webkampót hoz létre.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -ExpiryTime
A **DateTimeOffset** -objektumhoz a webhook lejárati időpontját adja meg.
Megadhat egy karakterláncot vagy egy **datetime** értéket, amelyet átalakíthat érvényes **DateTimeOffset**.

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
ps_force

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

### -IsEnabled
Megadja, hogy engedélyezve van-e a webhook.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A webkampó nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Paraméterek
A kulcs/érték párok szótárát adja meg.
A kulcsok a runbook paraméterek nevei.
Az értékek a runbook paraméter értékei.
Ha a runbook egy webkampóra válaszol, ezek a paraméterek a runbook kerülnek.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport-csoportnak a neve, amelyhez a parancsmag létrehoz egy webkampót.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunbookName
A webkampóhoz társítani kívánt runbook nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunOn
Annak a hibrid munkacsoportnak a neve, amely a runbook végrehajtani

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Boolean

### System. DateTimeOffset

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. webhook

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmAutomationWebhook](./Get-AzureRMAutomationWebhook.md)

[Remove-AzureRmAutomationWebhook](./Remove-AzureRMAutomationWebhook.md)

[Set-AzureRmAutomationWebhook](./Set-AzureRMAutomationWebhook.md)


