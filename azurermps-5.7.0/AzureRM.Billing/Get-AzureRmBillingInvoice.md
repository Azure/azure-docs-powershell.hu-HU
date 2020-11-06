---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 5a6ccf36f8e7aecdca4d6560614e9185a5ca26b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493245"
---
# Get-AzureRmBillingInvoice

## Áttekintés
Lekérheti az előfizetés számlázási számláit.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Legújabb
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Egyetlen
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmBillingInvoice** parancsmag az előfizetés számlázási számláit kapja. 

## Példák

### Példa 1
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

Az előfizetés legújabb számlájának beszerzése

### 2. példa
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

A megadott nevű előfizetés számlájának beszerzése

### 3. példa
```
PS C:\> Get-AzureRmBillingInvoice
```

Az előfizetés összes elérhető számlájának beszerzése fordított időrendi sorrendben, az URL-cím letöltése nélkül, a legutóbbi számlával kezdve. 

### 4. példa
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Az előfizetés legutóbbi 10 számlájának beszerzése, és az eredményben szerepel a letöltési URL-cím.

## PARAMÉTEREK

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

### -GenerateDownloadUrl
A számlák letöltési URL-címének létrehozása.

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Legújabb
A legújabb számla beszerzése.

```yaml
Type: SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
A visszaadott rekordok maximális számát adja meg.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A beolvasott vagy a legutóbbiak szerint megadott számla neve

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. számlázás. models. számla, Microsoft. Azure. commands. számlázás, verzió = 0.14.0.0, Culture = semleges, PublicKeyToken = null]]
Microsoft. Azure. Management. számlázás. modellek. számla

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

