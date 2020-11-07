---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/update-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Update-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Update-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 78308306e7bc46d4a9b3fadf4b00050cf9898f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679626"
---
# Update-AzureRmAutomationSourceControl

## Áttekintés
Az Azure automatizálási adatforrás vezérlőjének frissítése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Update-AzureRmAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A Update-AzureRmAutomationSourceControl parancsmag az Azure automatizálási szolgáltatásban egy mező értékének értékét módosítja.

## Példák

### Példa 1
Ez a parancs a PublishRunbook mezőt false értékre állítja az Azure automatizálási VSTSNative nevű devAccount nevű fiókban.


```powershell
Update-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## PARAMÉTEREK

### -AccessToken
A Forrásobjektum-hozzáférési jogkivonat.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomationAccountName
Az automatizálási fiók neve.

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

### -AutoSync
A verziókövetés AutoSync tulajdonsága.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Branch
A forrás vezérlő ágat.

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

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Leírás
A forrás vezérlő leírása.

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

### -FolderPath
A verziókövetés mappa elérési útja.

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

### -Name (név)
A forrás vezérlő neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublishRunbook
A verziókövetés publishRunbook tulajdonsága.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforrás csoport neve.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. SourceControl

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
