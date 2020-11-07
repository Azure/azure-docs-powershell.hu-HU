---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/resume-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 635b08c90ea87dab98b724110b2228f5b46d61fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672040"
---
# Resume-AzureRmAutomationJob

## Áttekintés
Befejezi a felfüggesztett automatizálási feladatot.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **resume-AzureRmAutomationJob** parancsmag felfüggesztette az Azure automatizálási feladatot.
Adja meg a felfüggesztett feladatot.

A feladat felfüggesztéséhez használja az Suspend-AzureRmAutomationJob parancsmagot.

## Példák

### 1. példa: felfüggesztett feladat folytatása
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

Ez a parancs folytatja a megadott azonosítót tartalmazó munkát.

## PARAMÉTEREK

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag folytatja a munkát.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag visszatér.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag folytatja a feladatot.

```yaml
Type: String
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

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmAutomationJob](./Get-AzureRMAutomationJob.md)

[Get-AzureRmAutomationJobOutput](./Get-AzureRMAutomationJobOutput.md)

[Stop-AzureRmAutomationJob](./Stop-AzureRMAutomationJob.md)

[Felfüggesztés – AzureRmAutomationJob](./Suspend-AzureRMAutomationJob.md)


