---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846161"
---
# Get-AzSupportTicketCommunication

## Áttekintés
Támogatási menetjegy-kommunikáció kérése

## SZINTAXISA

### GetByNameParameterSet (alapértelmezett)
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### GetByParentObjectParameterSet
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## Leírás
Kommunikációt kap a támogatási jegyekhez. Ha nem ad meg semmilyen egyéb paramétert, a program minden kommunikációt lekérdez a jegyben. A CreatedDate vagy a CommunicationType segítségével is szűrheti a kommunikációt a szűrő paraméterrel. Íme néhány példa a megadható értékek szűrésére.


| Forgatókönyv                                                        | Szűrő                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| Webes kommunikáció beszerzése                                          | "CommunicationType EQ" web ""                               |
| Telefonos kommunikáció beszerzése                                        | "CommunicationType EQ" telefon ' "                             |
| A december 20-ig vagy később létrehozott közlemények beszerzése, 2019 | "CreatedDate GE 2019-12-20"                                |
| A december 20.2019 után létrehozott kommunikáció beszerzése       | "CreatedDate gt 2019-12-20"                                |
| A december 20., 2019 után létrehozott webes kommunikációt kapja.            | "CreatedDate gt 2019-12-20 és CommunicationType EQ ' Web '" |


Ez a parancsmag az első és a kihagyott paraméterek segítségével támogatja a lapozást.

A kommunikációs név megadásával is lekérheti az egyetlen támogatási jegy kommunikációját. 

## Példák

### Példa 1: támogatási jegy minden kommunikációjának lekérése
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### 2. példa: egyetlen kommunikáció lekérése a támogatási jegy nevében
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### 3. példa: a támogatási jegy első 2 kommunikációjának beolvasása
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Példa 4: a következő 2 kommunikáció lekérése az első 2 kommunikáció kihagyása után támogatási jegyhez
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### Példa 5: a támogatási jegy összes webes kommunikációjának lekérése
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Példa 6: a december 20-án vagy azt követően létrehozott összes kommunikáció lekérése, 2019 a támogatási jegyhez
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 7. példa: a támogatási jegyhez az 2019 december 20-án vagy azt követően létrehozott összes webes kommunikáció lekérése
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 8. példa: a támogatási jegy minden kommunikációjának lekérése a csővezeték-támogatási jegy objektummal
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Szűrő
A parancsmag eredményeire alkalmazott szűrő.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Kommunikációs név.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportTicketName
Támogatási jegy neve

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

### -SupportTicketObject
Támogatási jegy objektum.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IncludeTotalCount
A kijelölt objektumok által követett összes objektum (egész) számát adja eredményül.
Ha a parancsmag nem tudja megállapítani a teljes számlálást, az "ismeretlen összeg száma" szöveget jeleníti meg. Az egész számnak van egy pontossági tulajdonsága, amely az összeg megbízhatóságát jelzi.
Az 0,0-től 1,0-ig terjedő pontossági értékek értéke, ahol az 0,0 azt jelenti, hogy a parancsmag nem tudta megszámolni az objektumokat, az 1,0 azt jelenti, hogy a darab pontos, és a 0,0 és a 1,0 közötti érték egyre megbízhatóbb becslést ad.

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

### -Skip (kihagyás)
Figyelmen kívül hagyja a megadott számú objektumot, majd Kinyeri a fennmaradó objektumokat.
Adja meg, hogy hány objektum legyen kihagyva.

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

### – Első
Csak a megadott számú objektumot kapja meg.
Adja meg a bejutni kívánt objektumok számát.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. commands. support. models. PSSupportTicket

## KIMENETEK

### Microsoft. Azure. commands. support. models. PSSupportTicketCommunication

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
