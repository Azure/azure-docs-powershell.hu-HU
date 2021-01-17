---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366364"
---
# New-AzStreamAnalyticsInput

## SYNOPSIS
Létrehozza vagy frissíti a munkabemenetet.

## SZINTAXIS

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzStreamAnalyticsInput** parancsmag bemeneti adatokat hoz létre egy Stream Analytics-feladaton belül, vagy frissíti a meglévő bemeneteket.
A bemeneti érték nevét meg lehet adni a JSON-fájlban vagy a parancssorban.
Ha mindkettő meg van adva, a parancssorban található névnek meg kell egyeznie a fájlban található névvel.
Ha olyan bemenetet ad meg, amely már létezik, és nem adja meg a *Force* paramétert, a parancsmag megkérdezi, hogy lecseréli-e a meglévő bemenetet.
Ha megadja az *Kényszerítés* paramétert, és megad egy meglévő bemeneti nevet, a rendszer megerősítés nélkül lecseréli a bemenetet.

## PÉLDÁK

### 1. példa: Fájlból származó definícióval bevitt feladat létrehozása
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

Ez a parancs bemenetet hoz létre a be Input.jsfájlból.
Ha a bemeneti definíciós fájlban megadott nevű meglévő beviteli mező már definiálva van, a parancsmag megkérdezi, hogy lecseréli-e azt.

### 2. példa: Feladatbevitel létrehozása
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

Ez a parancs új bevitelt hoz létre a EntryStream nevű feladatban.
Ha már definiált egy ilyen nevű meglévő bemenetet, a parancsmag megkérdezi, hogy lecseréli-e azt.

### 3. példa: Feladatbemenet cseréje egy fájlból származó definícióval
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

Ez a parancs jóváhagyás nélkül lecseréli az EntryStream nevű meglévő bemeneti forrás definícióját a fájlból származó definícióra.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -File
Egy JSON-fájl elérési útját adja meg, amely tartalmazza a létrehozni kívánt Azure Stream Analytics-bemenet JSON-ábrázolásait.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.

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

### -JobName
Megadja annak az Azure Stream Analytics-feladatnak a nevét, amely alatt létre kell hoznia az Azure Stream Analytics-bemenetet.

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

### -Name
Megadja a létrehozni szükséges Azure Stream Analytics-bemenet nevét.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amely alatt létre kell hoznia az Azure Streaming-bemenetet.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStreamAnalyticsInput](./Get-AzStreamAnalyticsInput.md)

[Remove-AzStreamAnalyticsInput](./Remove-AzStreamAnalyticsInput.md)

[Test-AzStreamAnalyticsInput](./Test-AzStreamAnalyticsInput.md)


