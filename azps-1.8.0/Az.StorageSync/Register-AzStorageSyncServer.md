---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: edfeebf9781c40b44a5a06db407757a5e2f5d2a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668484"
---
# Register-AzStorageSyncServer

## Áttekintés
Ez a parancs a kiszolgálót egy olyan tárterület-szinkronizáló szolgáltatáshoz regisztrálja, amely bizalmi kapcsolatot hoz létre. Ezt követően a PowerShell vagy az Azure portál segítségével konfigurálhatja a szinkronizálást a kiszolgálón.

## SZINTAXISA

### ObjectParameterSet (alapértelmezett)
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StringParameterSet
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentStringParameterSet
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Ez a parancs a kiszolgálót egy tárterület-szinkronizáló szolgáltatáshoz, az Azure-fájlok szinkronizálásához szükséges legfelső szintű erőforráshoz regisztrálja. Létrejön egy bizalmi kapcsolat a kiszolgáló és a tárterület-szinkronizáló szolgáltatás között, amely biztosítja az adatátviteli és-kezelési csatornák biztonságát. A PowerShell vagy az Azure portál segítségével beállíthatja, hogy a kiszolgálón milyen szinkronizálások legyenek. A kiszolgálók csak egyetlen tárterület-szinkronizáló szolgáltatásban regisztrálhatók. Ha a kiszolgálókhoz ugyanazon fájlok szinkronizálásához is szüksége van, regisztrálja őket ugyanabba a tárterület-szinkronizálási szolgáltatásba.
A parancsot helyileg kell futtatni abban a kiszolgálón, amelyet regisztrálni kell, vagy közvetlenül vagy távoli PowerShell-munkameneten keresztül kell végrehajtani. A távoli számítógép-objektum nem fogadható el.

## Példák

### Példa 1
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

Ez a parancs rögzíti a helyi kiszolgálót, amelyre a parancs fut.

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben

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

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -ParentObject
StorageSyncService objektum, általában áthalad a paraméteren.

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentResourceId
A StorageSyncService szülő erőforrás-azonosítója

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageSyncServiceName
A StorageSyncService neve.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

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

### Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService

## KIMENETEK

### Microsoft. Azure. Command. StorageSync. models. PSRegisteredServer

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
