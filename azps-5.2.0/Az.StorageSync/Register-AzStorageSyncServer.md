---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366602"
---
# Register-AzStorageSyncServer

## SYNOPSIS
Ez a parancs regisztrál egy kiszolgálót egy tárterület-szinkronizálási szolgáltatásban, amely megbízhatósági kapcsolatot hoz létre. Ezután a PowerShell vagy az Azure Portal segítségével konfigurálhatja a szinkronizálást ezen a kiszolgálón.

## SZINTAXIS

### StringParameterSet (alapértelmezett)
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ObjectParameterSet
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ParentStringParameterSet
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Ez a parancs regisztrál egy kiszolgálót egy tárterület-szinkronizálási szolgáltatásban, amely az Azure File Sync legfelső szintű erőforrása. Létrejön egy megbízhatósági kapcsolat a kiszolgáló és a tárterület-szinkronizálási szolgáltatás között, amely biztosítja a biztonságos adatátviteli és kezelési csatornákat. Ezután a PowerShell vagy az Azure Portal segítségével konfigurálhatja a kiszolgálón található szinkronizálásokat. Egy kiszolgáló csak egyetlen tárterület-szinkronizálási szolgáltatásba regisztrálható. Ha a kiszolgálóknak részt kell venniük ugyanazon fájlkészlet szinkronizálásában, regisztrálja őket ugyanannak a tárhelyszinkronizálási szolgáltatásnak.
A parancsot helyben kell futtatni a regisztrálandó kiszolgálón – vagy közvetlenül, vagy egy távoli PowerShell-munkameneten keresztül. Távoli számítógépes objektum nem fogadható el.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

Ez a parancs regisztrálja azt a helyi kiszolgálót, amelyen a parancs fut.

## PARAMETERS

### -AsJob
Parancsmag futtatása a háttérben

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

### -ParentObject
StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.

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
StorageSyncService szülőerőforrás-azonosító

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
Erőforráscsoport neve.

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

### Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService

## KIMENETEK

### Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
