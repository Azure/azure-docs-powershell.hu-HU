---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 9f52e2a709e2518dbc749b20afc97125e9b3ae64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930322"
---
# Get-AzDataFactoryLinkedService

## SYNOPSIS
Információkat kap a csatolt szolgáltatásokról az Azure Data Factoryban.

## SZINTAXIS

### ByFactoryName (alapértelmezett)
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzDataFactoryLinkedService** parancsmag információkat kap az Azure Data Factory csatolt szolgáltatásairól.
Ha megadja egy csatolt szolgáltatás nevét, ez a parancsmag információt kap a hivatkozott szolgáltatásról.
Ha nem ad meg nevet, ez a parancsmag információt kap az adatüzemben található összes csatolt szolgáltatásról.

## PÉLDÁK

### 1. példa: Információk az összes csatolt szolgáltatásról
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

Ez a parancs információkat kap a WikiADF nevű adatüzemeltetőben található összes csatolt szolgáltatásról, majd a folyamat műveleti Format-List segítségével átadja a csatolt szolgáltatásokat a Format-List-parancsmagnak.
Ez a parancsmag formázja az eredményeket.
További információért írja be a `Get-Help Format-List` .

### 2. példa: Információk lekérte egy adott csatolt szolgáltatásról
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

Ez a parancs információkat kap a WikiADF nevű adatszolgáltató HDILinkedService nevű csatolt szolgáltatásról.

### 3. példa: Információ lekérte egy adott csatolt szolgáltatásról a DataFactory paraméter megadásával
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Az első parancs a Get-AzDataFactory parancsmag használatával begyűjte a ContosoFactory nevű adat factoryt, majd tárolja azt a $DataFactory változóban.
A második parancs információkat kap a $DataFactory-ban tárolt adatüzemeltető csatolt szolgáltatásról, majd Format-Table folyamatkezelő parancsmag használatával átadja az adatokat a Format-Table-parancsmagnak.
**A Format-Table** a kimenetet adatkészletként formázza a megadott tulajdonságokkal adatkészletoszlopokként.

## PARAMETERS

### -DataFactory
EGY **PSDataFactory-objektumot** ad meg.
Ez a parancsmag olyan csatolt szolgáltatásokat kap, amelyek a paraméter által megadott adatüzemhez tartoznak.

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
Ez a parancsmag olyan csatolt szolgáltatásokat kap, amelyek a paraméter által megadott adatüzemhez tartoznak.

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

### -Name
Annak a csatolt szolgáltatásnak a nevét adja meg, amelyről információt kell kapnia.

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
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag olyan csatolt szolgáltatásokat kap, amelyek a paraméter által megadott csoporthoz tartoznak.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


