---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/save-azurermdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 696e2de560b67db78f24dea7e8512d85c3640902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493162"
---
# Save-AzureRmDataFactoryLog

## Áttekintés
Az Azure HDInsight-feldolgozásból letölthető naplófájlok.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Save-AzureRmDataFactoryLog** parancsmag letölti az Azure HDInsight-szal kapcsolatos, a sertés-vagy a kaptár-projektek vagy az egyéni tevékenységek helyi merevlemezre való kezelését okozó naplófájlokat.
Először futtatja az Get-AzureRmDataFactoryRun parancsmagot egy adatszelethez tartozó tevékenység AZONOSÍTÓjának beolvasásához, majd ezt az azonosítót használva beolvashatja a naplófájlokat a HDInsight-fürthöz társított bináris nagy objektum (BLOB) tárolóból.

Ha nem adja meg a *DownloadLogs* paramétert, a parancsmag csak a naplófájlok helyét adja meg.

Ha a *DownloadLogs* megadása nélkül adja meg a kimeneti könyvtárat ( *kimeneti* paraméter), a rendszer letölti a naplófájlokat az alapértelmezett dokumentumok mappába.

Ha a *DownloadLogs* a kimeneti mappával ( *output* ) együtt adja meg, a rendszer letölti a naplófájlokat a megadott mappába.

## Példák

### 1. példa: naplófájlok mentése egy adott mappába
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Ez a parancs menti a tevékenység naplófájlját azzal az AZONOSÍTÓval, ahol a tevékenység az ADF nevű erőforráscsoport LogProcessingFactory nevű 841b77c9-d56c-48d1-99a3-8c16c3e77d39 tartozik.
A naplófájlok a C:\Test mappába kerülnek.

### 2. példa: naplófájlok mentése az alapértelmezett dokumentumok mappába
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Ez a parancs naplófájlokat ment a dokumentumok mappába (alapértelmezett).

### 3. példa: naplófájlok helyének beszerzése
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Ez a parancs a naplófájlok helyét számítja ki.
Figyelje meg, hogy a *DownloadLogs* nincs megadva.

## PARAMÉTEREK

### -DataFactory
Egy **PSDataFactory** -objektumot ad meg.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Az adatfeldolgozó nevét adja meg.
Ez a parancsmag letölti az adatfeldolgozó naplófájlját, amely ezt a paramétert adja meg.

```yaml
Type: String
Parameter Sets: ByFactoryName
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

### -DownloadLogs
Jelzi, hogy a parancsmag a naplófájlokat letölti a helyi számítógépre.
Ha a *ouptut* mappa nincs megadva, a fájlok a dokumentumok mappába kerülnek a mappa almappájában.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
Az adatszelethez futtatott tevékenység AZONOSÍTÓját adja meg.
A Get-AzureRmDataFactoryRun parancsmag használatával kaphat azonosítót.

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

### -Output (kimenet)
Azt a kimeneti mappát adja meg, amelyben a letöltött naplófájlok vannak mentve.

```yaml
Type: String
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
Ez a parancsmag olyan adattípust hoz létre, amely a paraméter által definiált csoportba tartozik.

```yaml
Type: String
Parameter Sets: ByFactoryName
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

### Microsoft. Azure. Command. DataFactories. models. PSRunLogInfo

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmDataFactoryRun](./Get-AzureRmDataFactoryRun.md)

[Get-AzureRmDataFactoryPipeline](./Get-AzureRmDataFactoryPipeline.md)

[Új – AzureRmDataFactoryPipeline](./New-AzureRmDataFactoryPipeline.md)

[Remove-AzureRmDataFactoryPipeline](./Remove-AzureRmDataFactoryPipeline.md)

[Set-AzureRmDataFactoryPipelineActivePeriod](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[Felfüggesztés – AzureRmDataFactoryPipeline](./Suspend-AzureRmDataFactoryPipeline.md)


