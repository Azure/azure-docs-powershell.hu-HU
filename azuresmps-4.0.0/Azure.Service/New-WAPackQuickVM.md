---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017400"
---
# New-WAPackQuickVM

## Áttekintés
Virtuális gépet hoz létre sablon alapján.

## SZINTAXISA

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ezek a témakörök elavultak, és a jövőben törlődnek.
Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.
A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .

A **New-WAPackQuickVM** parancsmag a virtuális gépet sablon alapján hozza létre.

## Példák

### Példa 1: virtuális gép létrehozása sablon alapján
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

Az első parancs létrehozza a **PSCredential** objektumot, majd a $credentials változóban tárolja.
A parancsmag a fiók és a jelszó megadását kéri.
További információért írja be a következőt: `Get-Help Get-Credential` .

A második parancs a **Get-WAPackVMTemplate** parancsmag segítségével kap sablont.
A parancs a sablon AZONOSÍTÓját adja meg.
A parancs a Template objektumot a $TemplateID változóban tárolja.

A végleges parancs egy VirtualMachine023 nevű virtuális gépet hoz létre.
A parancs a virtuális gépet az $TemplateId tárolt sablonon alapozza meg.

## PARAMÉTEREK

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
Sablon objektum beszerzéséhez használja a **Get-WAPackVMTemplate** parancsmagot.

```yaml
Type: VMTemplate
Parameter Sets: (All)
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
Parameter Sets: (All)
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

[Új – WAPackVM](./New-WAPackVM.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)


