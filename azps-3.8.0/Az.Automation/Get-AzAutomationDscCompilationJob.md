---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012707"
---
# Get-AzAutomationDscCompilationJob

## Áttekintés
A DSC fordítási feladatokat automatizálja az automatizálásban.

## SZINTAXISA

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

## Leírás
A **Get-AzAutomationDscCompilationJob** parancsmag az Azure automatizálási lehetőségeinek megfelelő állami konfigurációs (DSC) fordítási feladatokat kap.

## Példák

### Példa 1: az összes DSC fordítási feladat beszerzése
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Ez a parancs a Contoso17 nevű automatizálási fiókban minden fordítási feladatot kap.

### 2. példa: a DSC fordítási feladatok beszerzése egy konfigurációhoz
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

Ez a parancs a ContosoConfiguration nevű DSC-konfiguráció minden fordítási feladatát a Contoso17 nevű automatizálási fiókban kapja meg.

### 3. példa: speciális DSC-összeállítási feladat beszerzése
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Ez a parancs a Contoso17 nevű automatizálási fiókban megadott AZONOSÍTÓJÚ fordítási feladatot kapja.

## PARAMÉTEREK

### -AutomationAccountName
Megadja annak az automatizálási fióknak a nevét, amely a parancsmag által kapott DSC-összeállítási feladatokat tartalmazza.

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
Annak a DSC-konfigurációnak a neve, amelyhez ez a parancsmag befordítási feladatokat kap.

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

### -A befejezési időpont
A befejezési időpontot adja meg.
Ez a parancsmag azokat a fordítási feladatokat kapja meg, amelyek a paraméter által megadott időpontig kezdődtek.

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

### -Azonosító
Annak a DSC-összeállítási munkának az egyedi AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.

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
Annak a csoportnak a nevét adja meg, amelyben a parancsmag a DSC összeállítási feladatokat kapja.

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

### -Kezdő időpont
Megadja a kezdés időpontját.
Ez a parancsmag olyan feladatokat kap, amelyek a paraméter által megadott időpontnál vagy azt követően kezdődnek.

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
A parancsmag által kapott feladatok állapotát adja meg.
Az érvényes értékek a következők: 
- Kész 
- Sikertelen 
- Várólistán töltött 
- Kezdve 
- Újrakezd 
- Fut 
- Megállt 
- Megállás 
- Felfüggesztve 
- Indokolva kéri 
- Aktiválása
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. GUID

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. CompilationJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationDscCompilationJobOutput](./Get-AzAutomationDscCompilationJobOutput.md)

[Start-AzAutomationDscCompilationJob](./Start-AzAutomationDscCompilationJob.md)


