---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: bb88bc38f6102f18b4d45b3b80902886975e2628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936330"
---
# Get-AzAutomationDscNodeReport

## SYNOPSIS
Egy DSC-csomópontról az Automatizálásnak küldött jelentéseket kap.

## SZINTAXIS

### ByAll (alapértelmezett)
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByLatest
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzAutomationDscNodeReport** parancsmag az APS kívánt államkonfigurációs (DSC) csomópontja által az Azure Automationnek küldött jelentéseket kapja.

## PÉLDÁK

### 1. példa: A DSC-csomópontok összes jelentésének be szerezze
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

Az első parancs a Számítógép14 nevű számítógép DSC-csomópontját kapja meg a Contoso17 nevű automatizálási fiókban.
A parancs ezt az objektumot a $Node tárolja.
A második parancs a Számítógép14 nevű DSC-csomópontról a Contoso17 nevű automatizálási fiókba küldött összes jelentés metaadatait kapja.
A parancs a csomópontot  az objektum Id $Node határozza meg.

### 2. példa: DSC-csomópont jelentése jelentésazonosító alapján
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Az első parancs a Számítógép14 nevű számítógép DSC-csomópontját kapja meg a Contoso17 nevű automatizálási fiókban.
A parancs ezt az objektumot a $Node tárolja.
A második parancs a Számítógép14 nevű DSC-csomópontból a Contoso17 nevű automatizálási fiókba küldött megadott azonosítóval azonosított jelentés metaadatait kapja.

### 3. példa: A DSC-csomópontok legújabb jelentésének lekérte
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

Az első parancs a Számítógép14 nevű számítógép DSC-csomópontját kapja meg a Contoso17 nevű automatizálási fiókban.
A parancs ezt az objektumot a $Node tárolja.
A második parancs a Számítógép14 nevű DSC-csomópontról a Contoso17 nevű automatizálási fiókba küldött legújabb jelentés metaadatait kapja.

## PARAMETERS

### -AutomationAccountName
Egy automatizálási fiók nevét adja meg.
Ez a parancsmag a paraméter által megadott fiókhoz tartozó DSC-csomópont jelentéseit exportálja.

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
Ez a parancsmag olyan jelentéseket kap, amelyek szerint az automatizálás a jelen időpont előtt érkezett.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
A lekért parancsmag DSC-csomópontjelentésének egyedi azonosítója.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Latest
Azt jelzi, hogy ez a parancsmag csak a megadott csomópont legújabb DSC-jelentését kapja meg.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeId
Annak a DSC-csomópontnak az egyedi azonosítója, amelyhez a parancsmag jelentéseket kap.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amely tartalmazza azt a DSC-csomópontot, amelyhez a parancsmag jelentéseket kap.

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
Ez a parancsmag olyan jelentéseket kap, amelyek szerint az automatizálás ezt követően érkezett.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.Guid

### System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Automation.Model.DscNode

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Export-AzAutomationDscNodeReportContent](./Export-AzAutomationDscNodeReportContent.md)


