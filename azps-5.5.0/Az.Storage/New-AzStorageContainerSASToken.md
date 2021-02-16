---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165658"
---
# New-AzStorageContainerSASToken

## SYNOPSIS
Egy Azure-tárolóhoz egy SAS-jogkivonatot hoz létre.

## SZINTAXIS

### SasPolicy
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SasPermission
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzStorageContainerSASToken** parancsmag létrehoz egy SAS-jogkivonatot egy Azure-tárolóhoz.

## PÉLDÁK

### 1. példa: Tároló SAS-jogkivonat létrehozása teljes tároló engedéllyel
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

Ez a példa egy teljes tároló engedéllyel rendelkező tároló SAS-jogkivonatot hoz létre.

### 2. példa: Több tároló SAS-jogkivonat létrehozása folyamat szerint
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

Ez a példa több tároló SAS-jogkivonatot hoz létre a folyamat használatával.

### 3. példa: Tároló SAS-jogkivonat létrehozása megosztott hozzáférési házirend használatával
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

Ez a példa megosztott hozzáférési házirendet tartalmazó tároló SAS-jogkivonatot hoz létre.

### 3. példa: Felhasználói identitás tároló SAS-jogkivonat létrehozása OAuth-hitelesítésen alapuló tárterületkörnyezetben
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

Ebben a példában egy OAuth-hitelesítésen alapuló tárterületkörnyezetet tartalmazó Felhasználói identitás tároló SAS-jogkivonatot hoz létre.

## PARAMETERS

### -Környezet
Egy Azure-tárterület környezetét határozza meg.
A parancsmagot a New-AzStorageContext hozhatja létre.
Amikor a tárterületkörnyezet OAuth-hitelesítésen alapul, létrehoz egy Felhasználói identitás tároló SAS-jogkivonatot.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Azt az időt adja meg, amikor a megosztott hozzáférés-aláírás érvénytelenné válik.
Ha a felhasználó beállítja a kezdési időt, de nem a lejárati időt, a lejárati idő a kezdési időpontra plusz egy órával van megállítva.
Ha sem a kezdési időpont, sem a lejárati idő nincs megadva, a lejárati idő az aktuális idő plusz egy óra lesz.
Ha a tárterület környezete OAuth-hitelesítésen alapul, a lejárati időnek a jelenlegi időponttól 7 napon belül kell lennie, és nem lehet korábbi a jelenlegi időpontnál.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
Azt jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási jogkivonatot adja vissza.

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

### -IPAddressOrRange
Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni (például 168.1.5.65 vagy 168.1.5.60-168.1.5.70).
A tartomány magában foglalja a teljes tartományt is.

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

### -Name
Egy Azure-tároló tárolónevet ad meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Engedély
Egy tároló engedélyeinek megadása.
Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Házirend
Egy Azure Tárolt hozzáférési házirendet ad meg.

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
A kéréshez engedélyezett protokollt adja meg.
A paraméter elfogadható értékei a következőek:
* HttpsOnly
* HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvényessé válik.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzStorageBlobSASToken](./New-AzStorageBlobSASToken.md)
