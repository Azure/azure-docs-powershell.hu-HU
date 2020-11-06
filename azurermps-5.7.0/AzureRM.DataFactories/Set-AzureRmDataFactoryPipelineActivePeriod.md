---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 1c6290f21693f599925f34f950256005df8be670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493156"
---
# Set-AzureRmDataFactoryPipelineActivePeriod

## Áttekintés
Az adatszeletek aktív időszakának beállítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmDataFactoryPipelineActivePeriod** parancsmag beállítja az adatszeletek aktív időszakát az Azure Data Factory által feldolgozott csővezetékekkel.
Ha az Set-AzureRmDataFactorySliceStatus parancsmagot használja az adatkészlet szeletei állapotának módosításához, győződjön meg arról, hogy a szelet kezdési és befejezési időpontja a csővezeték aktív időszakában van.

Miután létrehozta a csővezetéket, megadhatja, hogy milyen időszakon belül történjen az adatfeldolgozás.
A csővezetékek aktív időszakának meghatározása: azt az időtartamot adja meg, amelyben az adatszeletek feldolgozása az egyes adatfeldolgozó-adatkészletekhez meghatározott **elérhetőségi** tulajdonságok alapján történik.

## Példák

### 1. példa: az aktív időszak beállítása
```
PS C:\>Set-AzureRmDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

Ez a parancs beállítja az adatszeletek aktív időszakát a DPWikisample folyamatok nevű csővezetékhez.
A parancs az adatszeletek kezdő és záró pontját adja meg értékként.
A parancs a $True értékét számítja ki.

## PARAMÉTEREK

### -Autofeloldás
Azt jelzi, hogy ez a parancsmag az automatikus feloldást használja.

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

### -DataFactory
Egy **PSDataFactory** -objektumot ad meg.
Ez a parancsmag módosította az adatfeldolgozóhoz tartozó csővezeték aktív időszakát, amely ezt a paramétert adja meg.

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
Ez a parancsmag módosította az adatfeldolgozóhoz tartozó csővezeték aktív időszakát, amely ezt a paramétert adja meg.

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

### -EndDateTime
Az időszak végét **datetime** -objektumként adja meg.
Ebben az időszakban dolgozzák fel az adatfeldolgozást vagy az adatszeleteket.
A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .

A *EndDateTime* a ISO8601 formátumban kell megadni az alábbi példákban: 

2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time)

Az alapértelmezett időzóna-kijelölés az UTC.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceRecalculate
Azt jelzi, hogy ez a parancsmag a kényszerített újraszámítást használja.

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

### -PipelineName
A csővezeték nevét adja meg.
Ez a parancsmag az aktív időszakot adja meg ahhoz a csővezetékhez, amelyet a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag módosítja egy olyan csővezeték aktív időszakát, amely a paraméter által meghatározott csoportba tartozik.

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

### -StartDateTime
Az időszak kezdését **datetime** -objektumként adja meg.
Ebben az időszakban dolgozzák fel az adatfeldolgozást vagy az adatszeleteket.

A *StartDateTime* a ISO8601 formátumban kell megadni.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### System. Boolean

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmDataFactoryPipeline](./New-AzureRmDataFactoryPipeline.md)

[Set-AzureRmDataFactorySliceStatus](./Set-AzureRmDataFactorySliceStatus.md)


