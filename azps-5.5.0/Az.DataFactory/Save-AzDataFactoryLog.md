---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144387"
---
# Save-AzDataFactoryLog

## SYNOPSIS
Naplófájlokat tölt le az Azure HDInsight-feldolgozásból.

## SZINTAXIS

### ByFactoryName (alapértelmezett)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Save-AzDataFactoryLog** parancsmag letölti a vírus- vagy hive-projektek Azure HDInsight-feldolgozásával vagy egyéni tevékenységekkel kapcsolatos naplófájlokat a helyi merevlemezre.
Először a Get-AzDataFactoryRun-parancsmag futtatásával lekéri egy tevékenység azonosítóját egy adatszelethez, majd ezzel az azonosítóval beolvassa a naplófájlokat a HDInsight-fürttel társított bináris nagy objektum (BLOB) tárolóból.
Ha nem adja meg *a DownloadLogs* paramétert, a parancsmag csak a naplófájlok helyét adja vissza.
Ha a *DownloadLogs paramétert* kimeneti könyvtár *(kimeneti* paraméter) megadása nélkül adja meg, a naplófájlok az alapértelmezett Dokumentumok mappába kerülnek.
Ha a *DownloadLogs mappát* egy kimeneti mappával *(Kimenet)* együtt adja meg, a naplófájlok a megadott mappába kerülnek.

## PÉLDÁK

### 1. példa: Naplófájlok mentése egy adott mappába
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Ez a parancs a 841b77c9-d56c-48d1-99a3-8c16c3e77d39 azonosítóval menti a tevékenységhez tartozó naplófájlokat, ahol a tevékenység az ADF nevű erőforráscsoport LogProcessingFactory nevű adat factoryjának egyik folyamatába tartozik.
A naplófájlokat a rendszer a C:\Test mappába menti.

### 2. példa: Naplófájlok mentése az alapértelmezett Dokumentumok mappába
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Ez a parancs a naplófájlokat a Dokumentumok mappába (alapértelmezés szerint) menti.

### 3. példa: A naplófájlok helyének lekérte
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Ez a parancs a naplófájlok helyét adja vissza.
Ne feledje, *hogy a DownloadLogs* nincs megadva.

## PARAMETERS

### -DataFactory
EGY **PSDataFactory-objektumot** ad meg.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Egy adatüzem nevét adja meg.
Ez a parancsmag letölti a paraméter által megadott adatüzem naplófájlját.

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

### -DownloadLogs
Azt jelzi, hogy ez a parancsmag letölti a naplófájlokat a helyi számítógépre.
Ha *nincs* megadva kimeneti mappa, a program a fájlokat egy almappa Dokumentumok mappájába menti.

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

### -Id
Az adatszelethez futtatott tevékenység azonosítóját adja meg.
A Get-AzDataFactoryRun parancsmag használatával lekérte az azonosítót.

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

### -Kimenet
Azt a kimeneti mappát adja meg, amelybe a letöltött naplófájlok mentve vannak.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag létrehoz egy adatüzemet, amely a paraméter által megadott csoporthoz tartozik.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


