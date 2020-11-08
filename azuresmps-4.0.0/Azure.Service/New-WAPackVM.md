---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017398"
---
# New-WAPackVM

## Áttekintés
Virtuális gépet hoz létre.

## SZINTAXISA

### CreateVMFromTemplate (alapértelmezett)
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ezek a témakörök elavultak, és a jövőben törlődnek.
Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.
A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .

A **New-WAPackVM** parancsmag virtuális gépet hoz létre.

## Példák

### Példa 1: virtuális gép létrehozása Windows operációs rendszerhez sablon használatával
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

Az első parancs létrehozza a **PSCredential** objektumot, majd a $credentials változóban tárolja.
A parancsmag a fiók és a jelszó megadását kéri.
További információért írja be a következőt: `Get-Help Get-Credential` .

A második parancs a **Get-WAPackVMTemplate** parancsmag használatával kapja meg a ContosoTemplate04 nevű virtuálisgép-sablont, majd a $Template változóban tárolja.

A végleges parancs létrehoz egy ContosoV023 nevű virtuális gépet a $Template változóban tárolt sablon alapján.
A parancs a *Windows* paramétert adja meg, ezért a virtuális gépnek futnia kell a Windows operációs rendszer verziójától.

### 2. példa: virtuális gép létrehozása Linux operációs rendszerhez sablon használatával
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

Az első parancs létrehozza a **PSCredential** objektumot, majd a $credentials változóban tárolja.

A második parancs a **Get-WAPackVMTemplate** parancsmag használatával kapja meg a ContosoTemplate19 nevű virtuálisgép-sablont, majd a $Template változóban tárolja.

A végleges parancs létrehoz egy ContosoV028 nevű virtuális gépet a $Template változóban tárolt sablon alapján.
A parancs a *Linux* paramétert adja meg, ezért a virtuális gépnek a Linux operációs rendszer verzióját kell futtatnia.

### 3. példa: virtuális gép létrehozása operációs rendszerbeli lemezről és méretről
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

Az első parancs a **Get-WAPackVMOSDisk** parancsmaggal a ContosoDiskOS nevű operációs rendszer lemezét kapja, majd a $OSDisk változóban tárolja.

A második parancs a **Get-WAPackVMSizeProfile** parancsmaggal kapja meg a MediumSizeVM nevű méret profilt, majd a $SizeProfile változóban tárolja.

A végleges parancs létrehoz egy ContosoV073 nevű virtuális gépet az $OSDisk tárolt operációs rendszerről és a $SizeProfile tárolt méret profilról.

## PARAMÉTEREK

### -AdministratorSSHKey
A rendszergazdai fiók Secure Shell (SSH) kulcsát adja meg.

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Azt jelzi, hogy a parancsmag virtuális gépet hoz létre a Linux operációs rendszer futtatásához.

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A virtuális gép nevét adja meg.

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

### -OSDisk
Az operációs rendszer merevlemezét adja meg **VirtualHardDisk** -objektumként.
Operációs rendszer lemezének beszerzéséhez használja a **Get-WAPackVMOSDisk** parancsmagot.

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Termék
A termékkulcsot adja meg.
A termékkulcs egy 25 jegyből álló szám, amely azonosítja a termék licencét.
Termékkulcs használata egy olyan operációs rendszerhez, amelyet virtuális gépre vagy állomásra tervez telepíteni.

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
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

### -Sablon
Egy sablont ad meg.
A parancsmag a megadott sablonon alapuló virtuális gépet hoz létre.
A Template-objektum beolvasásához használja az Get-WAPackVMTemplate parancsmagot.

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
A helyi rendszergazdai fiók hitelesítő adatait adja meg.
Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.
További információért írja be a következőt: `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
A virtuális gép **HardwareProfile** -objektumként használt méret profilját adja meg.
Ha szeretné beolvasni a méretet, használja a **Get-WAPackVMSizeProfile** parancsmagot.

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
Virtuális hálózatot ad meg.
A parancsmag a virtuális gépet a megadott virtuális hálózathoz köti.
Virtuális hálózat beszerzéséhez használja a **Get-WAPackVNet** parancsmagot.

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
Azt jelzi, hogy a parancsmag virtuális gépet hoz létre a Windows operációs rendszer futtatásához.

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-WAPackVM](./Get-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Újraindítás – WAPackVM](./Restart-WAPackVM.md)

[Önéletrajz – WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Start-WAPackVM](./Start-WAPackVM.md)

[Stop-WAPackVM](./Stop-WAPackVM.md)

[Felfüggesztés – WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


