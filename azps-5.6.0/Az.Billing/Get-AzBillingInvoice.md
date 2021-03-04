---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 604109a80171ff4bb294dc1643081cd8e933d728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922490"
---
# Get-AzBillingInvoice

## SYNOPSIS
Lekérte az előfizetés számlázási számláit.
Számlázási fiók és számlázási profil számlázási számláinak lekérte

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### Legújabb
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### Single
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzBillingInvoice** parancsmag az előfizetés számlázási számláit kapja meg. 

## PÉLDÁK

### 1. példa
```
PS C:\> Get-AzBillingInvoice -Latest
```

Szerezze be az előfizetés legújabb számláját.

### 2. példa
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

Szerezze be a megadott nevű előfizetés számláját.

### 3. példa
```
PS C:\> Get-AzBillingInvoice
```

Szerezze be az előfizetés összes elérhető számláját fordított időrendi sorrendben a legutóbbi számlával kezdve, az URL-cím letöltése nélkül. 

### 4. példa
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Szerezze be az előfizetés legutóbbi 10 számláját, és az eredményben foglalja bele a letöltési URL-címet.

### 5. példa
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

Szerezze be az adott számlát név szerint, és töltse le az URL-címet az eredményben.

### 6. példa
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

A számlákat a számlázási fiók nevével töltheti le, és az eredményben minden egyes számla letöltési URL-címét meg kell kapnia.

### 7. példa
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Szerezze be a megfelelő számlát számlanévvel és számlázási fióknévvel, és az eredményben minden egyes számla letöltési URL-címét foglalja bele.

### 8. példa
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Töltse le a legújabb számlát a számlázási fiók nevével, és az eredményben tartalmazza a számla letöltési URL-címét.

### 9. példa
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

Szerezze be az adott számlázási fiók és az adott számlázási profil legfrissebb 10 számláját, és az eredményben tartalmazza a letöltési URL-címet.

### 10. példa
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

A legújabb számlát a számlázási fiók neve és a számlázási profil neve alapján töltheti le, és az eredményben szerepel a számla letöltési URL-címe.

### 10. példa
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

A számlakivonatokat a számlázási fiók neve és a számlázási profil neve alapján, a kezdő dátum és az időszakOn belül dátum szerint megadott számlázási időszakra vonatkozóan is leküldi.


## PARAMETERS

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

### -GenerateDownloadUrl
Hozza létre a számlák letöltési URL-címét.

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

### -Latest
Szerezze be a legújabb számlát.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Azt határozza meg, hogy legfeljebb hány rekordot kell visszaadni.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Egy behozni vagy a legutóbbi számla neve, ha nincs megadva.

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

### -BillingAccountName
Annak a számlázási fióknak a neve, amelyről számlát kell kapnia.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BillingProfileName
Annak a számlázási profilnak a neve, amelyről le kell kapnia a számlákat.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeriodStartDate
Számla kezdő dátuma.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeriodEndDate
Számla záró dátuma.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Billing.Models.PSInvoice

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
