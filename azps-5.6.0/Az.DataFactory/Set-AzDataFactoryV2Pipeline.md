---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b059e48eda6367459bd90bd7ccdf93ea14387ae7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925074"
---
# Set-AzDataFactoryV2Pipeline

## SYNOPSIS
Létrehoz egy prognózist a Data Factoryban.

## SZINTAXIS

### ByFactoryName (alapértelmezett)
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByResourceId
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A Set-AzDataFactoryV2Pipeline parancsmag létrehoz egy folyamatot az Azure Data Factoryban.
Ha egy már létező folyamat nevét adja meg, a parancsmag megerősítést kér, mielőtt lecseréli a folyamatot.
Ha a Force paramétert adja meg, a parancsmag jóváhagyás nélkül lecseréli a meglévő folyamatot.
Végezze el ezeket a műveleteket a következő sorrendben: - Adatüzem létrehozása.
– Csatolt szolgáltatások létrehozása.
– Adatkészletek létrehozása.
– Folyamat létrehozása.
Ha egy azonos nevű folyamat már létezik az adatüzemben, a parancsmag megkérdezi, hogy felül kell-e írnia a meglévő prognózist az új prognózissal.
Ha megerősíti, hogy felülírja a meglévő folyamatot, a program a folyamatdefiníciót is lecseréli.

## PÉLDÁK

### 1. példa: Folyamat létrehozása
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

Ez a parancs létrehoz egy DPWikisample nevű prognózist az ADF nevű adatüzemben.
A parancs a folyamat alapja a fájlon DPWikisample.jsadatok.
Ez a fájl információkat tartalmaz a folyamat tevékenységeiről, például a Másolási tevékenység és a HDInsight-tevékenységről.

## PARAMETERS

### -DataFactoryName
Egy adatüzem nevét adja meg.
Ez a parancsmag létrehoz egy folyamatot a paraméter által megadott adat factoryhoz.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DefinitionFile
A JSON fájl elérési útja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Azt jelzi, hogy ez a parancsmag a megerősítés kérése nélkül lecserél egy meglévő folyamatot.

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

### -Name
A létrehozni szükséges folyamat nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag létrehoz egy prognózist a paraméter által megadott csoporthoz.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az Azure-erőforrásazonosító.

```yaml
Type: System.String
Parameter Sets: ByResourceId
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline

## MEGJEGYZÉSEK
Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDataFactoryV2Pipeline]()

[Remove-AzDataFactoryV2Pipeline]()

[Invoke-AzDataFactoryV2Pipeline]()
