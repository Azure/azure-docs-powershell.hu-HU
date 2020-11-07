---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 2a449235ac2b3fa98357e91e15602a0c7bd9eedb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671459"
---
# Remove-AzBatchApplication

## Áttekintés
Egy alkalmazást töröl egy köteg fiókból.

## SZINTAXISA

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Remove-AzBatchApplication** parancsmag egy alkalmazást egy Azure-kötegbeli fiókból töröl.

## Példák

### Példa 1: alkalmazás törlése egy köteg fiókból
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

Ez a parancs törli a Bárdos Iparcikk alkalmazást az ContosoBatch-fiókból.
A parancs nem működik, ha az alkalmazás bármely csomagot tartalmaz.

## PARAMÉTEREK

### -AccountName
Annak a kötegelt fióknak a neve, amelyből a parancsmag eltávolítja az alkalmazást.

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

### -ApplicationId
Az alkalmazás AZONOSÍTÓját adja meg.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchApplication](./Get-AzBatchApplication.md)

[Get-AzBatchApplicationPackage](./Get-AzBatchApplicationPackage.md)

[Új – AzBatchApplication](./New-AzBatchApplication.md)

[Új – AzBatchApplicationPackage](./New-AzBatchApplicationPackage.md)

[Remove-AzBatchApplicationPackage](./Remove-AzBatchApplicationPackage.md)

[Set-AzBatchApplication](./Set-AzBatchApplication.md)


