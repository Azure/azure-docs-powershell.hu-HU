---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015511"
---
# New-AzureStorSimpleVirtualDevice

## Áttekintés
Virtuális StorSimple eszközt hoz létre.

## SZINTAXISA

### CreateNewStorageAccount
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UseExistingStorageAccount
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorSimpleVirtualDevice** parancsmag virtuális StorSimple eszközt hoz létre.
Adja meg az eszköz nevét.
Adja meg a virtuális hálózat virtuális hálózat-és alhálózati adatait ugyanazon előfizetésben.
A Geo-nek egyeznie kell azzal a GEO-val, amelybe a StorSimple erőforrás jön létre.
Ha a virtuális eszközhöz meglévő tárolási fiókot szeretne használni, adja meg a nevet.
Ha új tárolási fiókot szeretne létrehozni ehhez a virtuális eszközhöz, adja meg a *StorageAccountName* és a *CreateNewStorageAccount* paramétert is.

## Példák

### Példa 1: virtuális eszköz létrehozása új fiókkal és meglévő hálózattal
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

Ez a parancs létrehoz egy virtuális eszközt, amely egy új tárolási fiókot és egy meglévő virtuális hálózatot használ.

### 2. példa: virtuális eszköz létrehozása meglévő fiókkal és virtuális hálózattal
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

Ez a parancs létrehoz egy virtuális eszközt, amely egy meglévő tárterület-fiókot és egy meglévő virtuális hálózatot használ.

## PARAMÉTEREK

### -CreateNewStorageAccount
Jelzi, hogy ez a parancsmag új tárterület-fiókot hoz létre.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersistAzureVMOnFailrue
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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
A tárolási fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubNetName
A virtuális alhálózat nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualDeviceName
A virtuális eszköz nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkName
A virtuális hálózat nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Karakterlánc
Ez a parancsmag a virtuális eszközt létrehozó feladat AZONOSÍTÓját számítja ki.
Ezt az azonosítót használva követheti nyomon az eredményeket az Get-AzureStorSimpleJob parancsmag használatával.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)

[Set-AzureStorSimpleVirtualDevice](./Set-AzureStorSimpleVirtualDevice.md)


