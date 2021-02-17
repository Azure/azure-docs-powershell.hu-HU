---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147578"
---
# Test-AzLogicApp

## SYNOPSIS
Logikai alkalmazásdefiníciót ellenőriz.

## SZINTAXIS

### LogicAppWithDefinitionParameterSet
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LogicAppWithDefinitionFileParameterSet
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Test-AzCmApp** parancsmag egy logikai appdefiníciót ellenőriz egy erőforráscsoportban.
Adja meg a logikai alkalmazás nevét, az erőforráscsoport nevét, a helyet, az állapotot, az integrációs fiókazonosítót vagy a paramétereket.
Ez a modul támogatja a dinamikus paramétereket.
Ha dinamikus paramétert használ, írja be a parancsba.
A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.
Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.

## PÉLDÁK

### 1. példa: Logikai alkalmazás érvényesítése fájl elérési utak használatával
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

Ez a parancs ellenőrzi a LogicApp01 nevű logikai appot a megadott erőforráscsoportban.
A parancs megadja a definíció és a paraméter elérési útját.

### 2. példa: Logikai alkalmazás érvényesítése objektumok használatával
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

Ez a parancs ellenőrzi a LogicApp01 nevű logikai appot a megadott erőforráscsoportban.
A parancs definíciót és paraméterobjektumokat ad meg.

### 3. példa

Logikai alkalmazásdefiníciót ellenőriz. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## PARAMETERS

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

### -Definition
Egy logikai alkalmazás definícióját adja meg objektumként vagy karakterláncként JavaScript Objektum-notation (JSON) formátumban.

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefinitionFilePath
A logikai alkalmazás definícióját adja meg egy JSON formátumú definíciós fájl elérési útjaként.

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IntegrationAccountId
A logikai alkalmazás integrációs fiókazonosítóját adja meg.

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

### -Location
A logikai alkalmazás helyét határozza meg.
Adja meg az Azure-adatközpont helyét, például Nyugat-Egyesült Államok vagy Délkelet-Ázsia.
A logikai alkalmazásokat bármilyen helyen el lehet helyezése.

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

### -Name
A logikai alkalmazás nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParameterFilePath
Egy JSON formátumú paraméterfájl elérési útját adja meg.

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

### -Parameters
A logikai alkalmazás paramétergyűjtemény-objektumát adja meg.
Adjon meg egy kivonattáblát, szótárat \<string\> vagy \<string, WorkflowParameter\> szótárat.

```yaml
Type: System.Object
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

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
A logikai alkalmazás állapotát adja meg.
A paraméter elfogadható értékei: Engedélyezve és Letiltva.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### System.Void

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzApp](./Get-AzLogicApp.md)

[New-AzApp](./New-AzLogicApp.md)

[Remove-AzApp](./Remove-AzLogicApp.md)

[Set-AzApp](./Set-AzLogicApp.md)

[Start-AzApp](./Start-AzLogicApp.md)


