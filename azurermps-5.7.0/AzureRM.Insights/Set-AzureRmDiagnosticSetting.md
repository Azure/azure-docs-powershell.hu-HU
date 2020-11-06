---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 086ca93f7b975f6c9b7f4de806dac0c7c99012b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493129"
---
# Set-AzureRmDiagnosticSetting

## Áttekintés
Az erőforrás naplók és metrikák beállításainak beállítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmDiagnosticSetting** parancsmag engedélyezi vagy letiltja az adott erőforráshoz tartozó minden gabona-és naplózási kategóriát.

A naplókat és a metrikákat a program a megadott tárterület-fiókban tárolja.

Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.

## Példák

### 1. példa: egy erőforrás összes metrikájának és naplójának engedélyezése
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

Ez a parancs a Resource01 minden elérhető metrikáját és naplóját engedélyezi.

### 2. példa: az összes metrikák és naplók letiltása
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

Ez a parancs letiltja az erőforrás-Resource01 elérhető összes metrikát és naplót.

### 3. példa: több kategória engedélyezése
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
Timegrain : PT1H
Logs
Enabled  : True
Category : Category1
Enabled  : True
Category : Category2
Enabled  : True
Category : Category3
Enabled  : False
Category : Category4
```

Ez a parancs lehetővé teszi a Category1 és a Category2.
Az összes timegrains és egyéb kategória változatlan marad.

### 4. példa: időgabona és több kategória engedélyezése
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

Ez a parancs csak a Category1, az Category2 és a Time Grain PT1M teszi lehetővé.
Minden más időgabona és kategória sem változik.

## PARAMÉTEREK

### -Kategóriák
Az engedélyezni vagy letiltani kívánt naplózási kategóriák listáját adja meg az *engedélyezett* érték szerint.
Ha nem ad meg egy kategóriát, az a parancs minden kategórián működik.

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

### -Engedélyezve
Azt jelzi, hogy engedélyezi-e a diagnosztika használatát.
Adja meg $True a diagnosztika engedélyezéséhez, vagy $False a diagnosztika letiltásához.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventHubAuthorizationRuleId
Az esemény hub szabálya

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az erőforrás AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionEnabled
Azt jelzi, hogy engedélyezve van-e a diagnosztikai adatok megőrzése.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
A napok szerinti adatmegőrzési házirendet adja meg.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
Annak a tárolási fióknak az AZONOSÍTÓját adja meg, amelybe az adatot menteni szeretné.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Timegrains
A metrikák engedélyezéséhez vagy letiltásához szükséges időmennyiséget adja meg az *engedélyezett* értéknek megfelelően.
Ha nem ad meg időgabonát, ez a parancs minden rendelkezésre álló időgabona esetén működik.

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

### -WorkspaceId
A munkaterület azonosítója

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. commands. OutputClasses. PSServiceDiagnosticSettings

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)


