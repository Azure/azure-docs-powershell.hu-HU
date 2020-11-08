---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017411"
---
# Remove-WAPackVMRole

## Áttekintés
Eltávolítja a virtuálisgép-szerepkörök objektumait.

## SZINTAXISA

### FromVMRoleObject (alapértelmezett)
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FromCloudService
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Ezek a témakörök elavultak, és a jövőben törlődnek.
Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.
A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .

A **Remove-WAPackVMRole** parancsmag eltávolítja a virtuálisgép-szerepkörök objektumait.

## Példák

### 1. példa: a virtuálisgép-szerepkörök eltávolítása (amelyet a WAP-portál használatával hoztak létre)
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

Az első parancs megkapja a ContosoVMRole01 nevű virtuális gép szerepkört a **Get-WAPackVMRole** parancsmaggal, majd az objektumot a $VMRole változóban tárolja.

A második parancs eltávolítja a $VMRoleban tárolt virtuális gép szerepkört.
A parancs a megerősítést kéri. Feltételezve, hogy ez a virtuális gép szerepkör a WAP-portálon keresztül jött létre, nem kell megadnia a felhőalapú szolgáltatás nevét.

### 2. példa: a felhőalapú szolgáltatás kézi létrehozása után létrehozott virtuális gép szerepkör eltávolítása
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

Az első parancs a **Get-WAPackVMRole** parancsmaggal az "ContosoVMRole02" nevű virtuális gép szerepkört kapja, majd az objektumot a $VMRole változóban tárolja.

A második parancs eltávolítja a $VMRoleban tárolt virtuális gép szerepkört.
A parancs a megerősítést kéri.
Feltételezve, hogy ez a virtuális gép szerepkör nem a portál használatával jött létre, a felhasználónak meg kell adnia a felhő szolgáltatás nevét.
Ebben az esetben a "ContosoCloudService02" nevet kell elnevezni.

### 3. példa: virtuális gép szerepkörének eltávolítása megerősítés nélkül
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

Az első parancs a **Get-WAPackVMRole** parancsmaggal kapja meg a ContosoVMRole03 nevű felhőalapú szolgáltatást, majd a $VMRole változóban tárolja az objektumot.

A második parancs eltávolítja a $VMRoleban tárolt virtuális gép szerepkört.
Ez a parancs az *erő* paramétert tartalmazza.
A parancs nem kér megerősítést.

## PARAMÉTEREK

### -CloudServiceName
A virtuális gép szerepkör Felhőbeli szolgáltatásának nevét adja meg.

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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

### -VMRole
Virtuális gép szerepkört ad meg.
Virtuális gép szerepkör beszerzéséhez használja a **Get-WAPackVMRole** parancsmagot.

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[Új – WAPackVMRole](./New-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


