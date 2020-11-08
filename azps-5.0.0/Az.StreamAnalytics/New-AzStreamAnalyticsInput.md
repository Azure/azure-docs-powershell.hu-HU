---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195014"
---
# New-AzStreamAnalyticsInput

## Áttekintés
Projekthez tartozó bevitelt hoz létre vagy frissít.

## SZINTAXISA

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **New-AzStreamAnalyticsInput** parancsmag létrehoz egy bemenetet egy adatfolyam-elemzési munkafolyamaton belül, vagy egy meglévő bemenetet frissít.
A beviteli nevet a JSON-fájlban vagy a parancssorban lehet megadni.
Ha a két érték van megadva, a parancssorban lévő név egyeznie kell a fájl nevével.
Ha olyan bemenetet ad meg, amely már létezik, és nem adja meg az *erő* paramétert, akkor a parancsmag azt fogja megkérdezni, hogy lecseréli-e a meglévő bemenetet.
Ha az *erő* paramétert adja meg, és egy meglévő beviteli nevet ad meg, a program megerősítés nélkül lecseréli a bemenetet.

## Példák

### 1. példa: bevitt munka létrehozása egy definícióval egy fájlból
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

Ez a parancs a fájl Input.jsbeírását hozza létre.
Ha már definiált egy meglévő bemenetet a szövegbeviteli definíciós fájlban megadott névvel, a parancsmag megkérdezi, hogy a program lecseréli-e vagy sem.

### 2. példa: projekt bemenetének létrehozása
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

Ezzel a paranccsal új adatokat hozhat létre a EntryStream nevű feladathoz.
Ha már meg van határozva egy meglévő bemenet, akkor a parancsmag megkérdezi, hogy lecseréli-e vagy sem.

### 3. példa: a bevitt munka lecserélése egy definícióval egy fájlból
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

Ez a parancs felülírja a EntryStream nevű meglévő beviteli forrás definícióját a definíció fájlból megerősítés nélkül.

## PARAMÉTEREK

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

### -Fájl
Annak a JSON-fájlnak az elérési útját adja meg, amely az Azure stream Analytics által létrehozott bemenet JSON-beli képviseletét tartalmazza.

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

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -Feladatnév
Annak az Azure stream-elemzési projektnek a nevét adja meg, amely alatt az Azure stream Analytics-adatbevitel hozható létre.

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
A létrehozandó Azure stream Analytics-bemenet nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az Azure adatfolyam-bevitelt létre szeretné hozni.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. StreamAnalytics. models. PSInput

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStreamAnalyticsInput](./Get-AzStreamAnalyticsInput.md)

[Remove-AzStreamAnalyticsInput](./Remove-AzStreamAnalyticsInput.md)

[Teszt-AzStreamAnalyticsInput](./Test-AzStreamAnalyticsInput.md)


