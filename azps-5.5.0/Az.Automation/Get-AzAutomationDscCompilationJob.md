---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149426"
---
# Get-AzAutomationDscCompilationJob

## SYNOPSIS
DSC-fordítási feladatokat kap az automatizálásban.

## SZINTAXIS

### ByAll (alapértelmezett)
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByJobId
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfigurationName
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzAutomationDscCompilation Parancsmag** az APS kívánt államkonfigurációs (DSC) fordítási feladatokat kap az Azure Automationben.

## PÉLDÁK

### 1. példa: Az összes DSC-fordítási feladat lekérte
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Ez a parancs a Contoso17 nevű automatizálási fiók összes fordítási feladatát beveszi.

### 2. példa: A DSC összeállítási feladatának lekért beállítása konfigurációhoz
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

Ez a parancs a Contoso17 nevű automatizálási fiók ContosoConfiguration nevű DSC-konfigurációjának összes fordítási feladatát beállítja.

### 3. példa: Adott fordítási feladat lekérte a DSC-t
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Ez a parancs a Contoso17 nevű automatizálási fiókban megadott azonosítójú fordítási feladatot kapja meg.

## PARAMETERS

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lekért DSC-fordítási feladatokat tartalmazza.

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

### -ConfigurationName
Annak a DSC-konfigurációnak a nevét adja meg, amelyhez a parancsmag fordítási feladatokat kap.

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -EndTime
A záró időpont megadása.
Ez a parancsmag olyan összeállítási feladatokat ad vissza, amelyek a paraméter által megadott időpontig elkezdődöttek.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
A parancsmag által lekért fordítási DSC-feladat egyedi azonosítóját adja meg.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag DSC-fordítási feladatokat kap.

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

### -StartTime
Megadja a kezdési időt.
Ez a parancsmag olyan feladatokat kap, amelyek a paraméter megadásakor vagy után kezdődnek.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Állapot
A parancsmag által lekért feladatok állapotát adja meg.
Érvényes értékek: 
- Befejezve 
- Sikertelen 
- Várólistán 
- Indítás 
- Visszaúszás 
- Fut 
- Leállítva 
- Leállítás 
- Felfüggesztve 
- Felfüggesztés 
- Aktiválás
- Új

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.Guid

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Automation.Model.CompilationJob

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationDscCompilationPut](./Get-AzAutomationDscCompilationJobOutput.md)

[Start-AzAutomationDscCompilationJob](./Start-AzAutomationDscCompilationJob.md)


