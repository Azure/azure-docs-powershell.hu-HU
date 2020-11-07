---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: e9d117e9e81ee1189031b9e1f2f0a4094e9b9fcf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835166"
---
# Set-AzMediaServiceKey

## Áttekintés
A Media szolgáltatáshoz társított REST-végpont eléréséhez használt kulcs újragenerálása.

## SZINTAXISA

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzMediaServiceKey** parancsmag újragenerálja a médiaszolgáltató által társított reprezentációs State Transfer (REST) végpont eléréséhez használt kulcsot.

## Példák

### 1. példa: a médiaszolgáltató eléréséhez használt elsődleges kulcs újragenerálása
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

Ez a parancs újra létrehozta a MediaService001 nevű, a ResourceGroup004 nevű erőforráscsoport csoportjába tartozó elsődleges kulcsot.

### 2. példa: a Media szolgáltatáshoz való hozzáféréshez használt másodlagos kulcs újragenerálása
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

Ez a parancs újra létrehozta a MediaService002 nevű, az Resourcegroup123 nevű erőforráscsoporthoz tartozó másodlagos kulcsot.

## PARAMÉTEREK

### -AccountName
Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag újra létrehozta.

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

### -Típus
A médiaadatfolyam-szolgáltatás kulcsának típusát adja meg.
A paraméter elfogadható értékei a következők: elsődleges vagy másodlagos.

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
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

## KIMENETEK

### Microsoft. Azure. commands. Media. models. PSServiceKey

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzMediaServiceKeys](./Get-AzMediaServiceKeys.md)


