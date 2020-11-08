---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016239"
---
# Move-AzureStorageAccount

## Áttekintés
Áttelepíti a tárolási fiókot az Azure Resource Manager-kötegbe.

## SZINTAXISA

### ValidateMigrationParameterSet
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### AbortMigrationParameterSet
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### CommitMigrationParameterSet
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PrepareMigrationParameterSet
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Move-AzureStorageAccount** parancsmag az Azure Resource Manager-kötegben lévő erőforrás-csoportba telepíti a tárolási fiókot.

## Példák

### 1. példa: a tárolási fiók áttelepítésének előkészítése
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

Ez a parancs a ContosoStorageName nevű tárolási fiókot készíti elő az Azure Resource Manager-kötegbe való áttelepítéshez.

### 2. példa: a tárolási fiók áttelepítésének megkezdése
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

Ez a parancs elindítja a ContosoStorageName nevű tárolási fiók áttelepítését az Azure Resource Manager-kötegbe.

### 3. példa: a tárolási fiók áttelepítésének ellenőrzése
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

Ez a parancs ellenőrzi a ContosoStorageName nevű tárolási fiók áttelepítését az Azure Resource Manager-kötegbe.

## PARAMÉTEREK

### -Megszakítás
Jelzi, hogy ez a parancsmag lemondja a tárolási fiók áttelepítését.

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Commit
Azt jelzi, hogy ez a parancsmag elindítja a tárolási fiók áttelepítését.

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Előkészületek
Jelzi, hogy ez a parancsmag előkészíti a tárolási fiókot az áttelepítéshez.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Annak a tároló fióknak a nevét adja meg, amelyre a parancsmag át van telepítve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Érvényesítés
Meghatározza, hogy ez a parancsmag ellenőrzi-e az áttelepítés tárolási fiókját.

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Move-AzureNetworkSecurityGroup](./Move-AzureNetworkSecurityGroup.md)

[Move-AzureReservedIP](./Move-AzureReservedIP.md)

[Move-AzureRouteTable](./Move-AzureRouteTable.md)

[Move-AzureService](./Move-AzureService.md)

[Move-AzureVirtualNetwork](./Move-AzureVirtualNetwork.md)


