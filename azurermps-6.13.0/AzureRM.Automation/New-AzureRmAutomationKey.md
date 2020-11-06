---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 8bd043f11294b2290a5f54289232bc826c1f0d88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492029"
---
# New-AzureRmAutomationKey

## Áttekintés
Automatizálja a regisztrációs kulcsokat egy automatizálási fiókhoz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmAutomationKey** parancsmag újragenerálja a regisztrációs kulcsokat az Azure automatizálási fiókhoz.

## Példák

### 1. példa: egy automatizálási fiók kulcsának újragenerálása
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

Ez a parancs újra létrehozta a AutomationAccount01 nevű Azure Automation fiók elsődleges kulcsát a ResourceGroup01 nevű erőforráscsoport számára.

## PARAMÉTEREK

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelyre a parancsmag újragenerálja a kulcsokat.

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

### -Típus
Az ügynök regisztrációs kulcsának típusát adja meg.
Az érvényes értékek a következők: 
- Elsődleges 
- Másodlagos

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.
Ez a parancsmag újragenerálja az automatizálási fiók kulcsait abban az erőforráscsoport-ban, amelyet a paraméter határoz meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. AgentRegistration

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
