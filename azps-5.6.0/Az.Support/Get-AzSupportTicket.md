---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: c5f68e947af383787b3ed1e7d9c9c3983c45769b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008278"
---
# Get-AzSupportTicket

## SYNOPSIS
Támogatási jegyeket is vásárolhat.

## SZINTAXIS

### ListParameterSet (alapértelmezett)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## LEÍRÁS
A támogatási jegylista lekérte. Ha nem ad meg paramétereket, a rendszer beolvassa az összes támogatási jegyet. A támogatási jegyeket állapot vagy CreatedDate szerint is szűrheti a Szűrő paraméter használatával. Íme néhány példa a megadható szűrőértékek használatára.

| Eset                                                         | Szűrés                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Nyitott állapotban elérhető jegyek lekérte                               | "Status eq 'Open'" (Állapot eq 'Megnyitás')                               |
| Lezárt állapotban elérhető jegyek lekérte                             | "Status eq 'Closed'"                             |
| 2019. december 20-án vagy azt követően létrehozott jegyek lekérte         | "CreatedDate ge 2019-12-20"                      |
| 2019. december 20. után létrehozott jegyek lekértek               | "CreatedDate gt 2019-12-20"                      |
| 2019. december 20. után létrehozott jegyeket kap, amelyek nyitott állapotban vannak | "CreatedDate gt 2019-12-20 and Status eq 'Open'" |


Ez a parancsmag az Első és a Kihagyás paraméteren keresztüli lapozást támogatja.

A jegy nevének megadásával egyetlen támogatási jegyet is lekérhet. 

## PÉLDÁK

### 1. példa: Az első 2 jegy lekérte
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### 2. példa: Az első 2 jegy leugrása után az első 2 jegy lekérte
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### 3. példa: Támogatási jegy lekért név szerint
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### 4. példa: Az első 2 támogatási jegy állapot szerint szűrve
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### 5. példa: Az összes nyitott állapotban létrehozott és 2019. december 20. után létrehozott támogatási jegy lekérte
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Filter
A parancsmag eredményéhez alkalmazandó szűrő.

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A parancsmag támogatási jegyének neve.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Az adatkészletben lévő objektumok teljes számát (egész számot) és a kijelölt objektumokat jelenti.
Ha a parancsmag nem tudja megállapítani a teljes számát, az "Ismeretlen teljes szám" üzenetet jeleníti meg. Az egész szám pontossági tulajdonsága a teljes darabszám megbízhatóságát jelzi.
A pontosság értéke 0,0 és 1,0 között van, ahol a 0,0 azt jelenti, hogy a parancsmag nem tudta megszámolni az objektumokat, az 1,0 azt jelenti, hogy a szám pontos, és a 0,0 és 1,0 közötti érték egyre megbízhatóbb becslést jelez.

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

### -Skip
Figyelmen kívül hagyja a megadott számú objektumot, majd beveszi a fennmaradó objektumokat.
Adja meg, hogy hány objektumot kell kihagyni.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
Csak a megadott számú objektumot kapja meg.
Adja meg a lekért objektumok számát.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
