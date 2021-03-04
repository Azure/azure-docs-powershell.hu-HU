---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932777"
---
# Add-AzLogProfile

## SYNOPSIS
Létrehoz egy új tevékenységnaplóprofilt. Ezzel a profillal archiválhatja a tevékenységnaplót egy Azure-tárfiókba, vagy adatfolyamként továbbíthatja egy Azure eseményközpontba ugyanabban az előfizetésben. 

## SZINTAXIS

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzLogProfile** parancsmag létrehoz egy naplóprofilt.
- **Tárfiók** – Csak a normál tárfiók (a prémium szintű tárfiók nem támogatott) támogatott. Típusának vagy ARM lehet. Ha egy tárfiókba van bejelentkezve, a tevékenységnapló tárolásának költségeit normál normál tárterületárak szerint számlázjuk. Előfizetésenként csak egy naplóprofil lehet, ezért előfizetésenként csak egy tárfiók használható a tevékenységnapló exportálására. 
- **Eseményközpont** – Előfizetésenként csak egy naplóprofil lehet, ezért előfizetésenként csak egy eseményközpont használható a tevékenységnapló exportálására. Ha a tevékenységnaplót egy eseményközpontba továbbítja, az eseményközpont szokásos ára lesz érvényben. A tevékenységnaplóban az események egy régióra vonatkoznak, vagy lehetnek "globálisak". Globálisan azt jelenti, hogy ezek az események régiódiagnosztikai események, és függetlenek a régiótól, valójában az események többsége ebbe a kategóriába tartozik. Ha a tevékenységnapló profilja a portálról van beállítva, az implicit módon hozzáadja a "Global" értéket a felhasználói felületen kijelölt többi régióval együtt. A parancsmag használata esetén a "Global" (Globális) helyet minden más régión kívül külön meg kell említeni. 
**Megjegyzés:-** Ha nem sikerül beállítani **a "Global" (Globális)** beállítását a helyeken, a tevékenységnapló nagy része nem lesz exportálva. Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.

## PÉLDÁK

### 1. példa: Új naplóprofil hozzáadása a helyfeltűnésnek megfelelő tevékenységnapló exportálása egy tárfiókba
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### 2. példa

Létrehoz egy új tevékenységnaplóprofilt. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMETERS

### -Category
A kategóriák listáját határozza meg.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Location
A naplóprofil helyét határozza meg.
Érvényes értékek: Futtassa a parancsmag alatt a helyek legújabb listáját. Get-AzLocation | Select DisplayName

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
A profil nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Az adatmegőrzési házirendet napokban adja meg. Ez az a napok száma, amikor a naplók megőrzve vannak a megadott tárfiókban. Az adatok megőrzéséhez állítsa ezt **0-ra.** Ha nincs megadva, akkor alapértelmezés szerint **0 lesz.** Az adatmegőrzésre normál normál tárterület- vagy eseményközponti számlázási díjak vonatkoznak.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
A Szolgáltatásbusz szabály azonosítója.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
A Tárfiók azonosítója. Az azonosító például a tárfiók teljes erőforrás-azonosítója  
/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## KIMENETEK

### Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


