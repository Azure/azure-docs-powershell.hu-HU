---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017352"
---
# Get-WAPackVMOSDisk

## Áttekintés
A virtuális gépekhez az operációs rendszer Disk objektumait kapja.

## SZINTAXISA

### Üres (alapértelmezett)
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ezek a témakörök elavultak, és a jövőben törlődnek.
Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.
A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .

A **Get-WAPackVMOSDisk** parancsmag a virtuális gépek operációs rendszerbeli merevlemez-objektumait kapja.

## Példák

### 1. példa: operációs rendszer lemezének beszerzése név használatával
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

Ez a parancs a ContosoOSDisk nevű operációs rendszer lemezét kapja.

### 2. példa: operációs rendszer lemezének beszerzése azonosító használatával
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

Ez a parancs a megadott azonosítót tartalmazó operációs rendszer lemezét kapja meg.

### 3. példa: az összes operációs rendszer lemezének beszerzése
```
PS C:\> Get-WAPackVMOSDisk
```

Ez a parancs az operációs rendszer összes lemezét bekapja.

## PARAMÉTEREK

### -AZONOSÍTÓ
Az operációs rendszer lemezének egyedi AZONOSÍTÓját adja meg.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Egy operációs rendszer lemezének nevét adja meg.

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-WAPackVM](./Get-WAPackVM.md)


