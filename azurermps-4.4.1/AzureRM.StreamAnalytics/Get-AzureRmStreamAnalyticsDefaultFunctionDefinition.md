---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 307a07254f61bcbd37127a2a4d15bb41944a3508
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495517"
---
# Get-AzureRmStreamAnalyticsDefaultFunctionDefinition

## Áttekintés
Az adatfolyam-elemzés függvény alapértelmezett definícióját kapja meg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** parancsmag az Azure stream Analytics függvény alapértelmezett definícióját kapja meg.
Az alapértelmezett definíció és a New-AzureRmStreamAnalyticsFunction parancsmag használatával is létrehozhatja a függvényeket.
A függvény létrehozása előtt módosíthatja az alapértelmezett definíciót.

## Példák

### Példa 1: az adatfolyam-elemzés függvény alapértelmezett definíciójának beszerzése
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

Ez a parancs a ScoreTweet nevű függvény alapértelmezett definícióját kapja meg a fájl RetrieveDefaultDefinitionRequest.jsben megadott paraméterekkel.

## PARAMÉTEREK

### -Fájl
Annak a. JSON fájlnak az elérési útját adja meg, amely a kérelem törzsének alapértelmezett függvény-definíciós kérésének beolvasására szolgáló JavaScript-objektum jelölését (JSON) tartalmazza.

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

### -Feladatnév
Annak az adatfolyam-elemzési feladatnak a nevét adja meg, amelybe a függvény tartozik.
Ez a parancsmag a megfelelő függvény alapértelmezett definícióját adja meg a projektben, amely ezt a paramétert adja meg.

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

### -Name (név)
Annak az adatfolyam-elemzési függvénynek a nevét adja meg, amelyhez ez a parancsmag az alapértelmezett definíciót kapja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnek a nevét adja meg, amelybe az adatfolyam-elemzés függvény tartozik.
Ez a parancsmag a paraméter által megadott csoport függvényének definícióját kapja meg.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. StreamAnalytics. models. PSFunction

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmStreamAnalyticsFunction](./New-AzureRmStreamAnalyticsFunction.md)


