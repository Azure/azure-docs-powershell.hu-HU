---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: d035890f6478c0b7fd767f12b8f9a27d4f765837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835173"
---
# Set-AzMediaService

## Áttekintés
Módosítja egy meglévő Media-szolgáltatás megadott tulajdonságait.

## SZINTAXISA

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **set-AzMediaService** parancsmag egy meglévő Media-szolgáltatás megadott tulajdonságait módosítja.

## Példák

### Példa 1: meglévő Media-szolgáltatás módosítása
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

Az első parancs létrehozza a címkék sorozatát, és azokat a címkéket a $Tags nevű változóban tárolja.
Ez a második parancs frissíti a MediaService001 nevű, a ResourceGroup123 nevű erőforráscsoporthoz tartozó Media szolgáltatását, amely a $Tags változóban tárolt címkéket tartalmazza.
A parancs a $StorageAccounts változóban tárolt tárolási konfigurációs objektumok tömbjét is használja.

## PARAMÉTEREK

### -AccountName
Annak a médiafájlnak a nevét adja meg, amelyet a parancsmag módosított.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ResourceGroupName
A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.

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

### -StorageAccounts
Megadja azokat a tárolási fiókokat, amelyeket ez a parancsmag a Media szolgáltatással társít.

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A médiafájlhoz társított címkék.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Collections. Hashtable

### Microsoft. Azure. commands. Media. models. PSStorageAccount []

## KIMENETEK

### Microsoft. Azure. commands. Media. models. PSMediaService

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzMediaService](./Get-AzMediaService.md)

[Új – AzMediaService](./New-AzMediaService.md)

[Remove-AzMediaService](./Remove-AzMediaService.md)


