---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015791"
---
# Set-AzureVMSize

## Áttekintés
Egy Azure virtuális gép méretének beállítását határozza meg.

## SZINTAXISA

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureVMSize** parancsmag frissíti a virtuális gép méretét.
Két paramétere van: *InstanceSize* , amely a virtuális gép új mérete, és a *VM* , amely a Virtual Machine objektum a **Get-AzureVM** parancsmag használatával.
A **set-AzureVMSize** eredménye a **Update-AzureVM** parancsmagra, illetve egy változóban későbbi használat céljából tárolható.
A **frissítési AzureVM** végrehajtása csak akkor történik meg, ha nincs tényleges módosítás.

Megjegyzés: Ez a parancsmag megköveteli a virtuális gép újralétesítését és új IP-cím megadását is.

## Példák

### Példa 1: virtuális gép méretének beállítása
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

A parancs frissíti a virtuális gépet a "kicsi" méretre.

## PARAMÉTEREK

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

### -InstanceSize
A virtuális gép méretét adja meg.

A paraméter elfogadható értékei a következők:

---ExtraSmall-------------------------------ExtraLarge

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

### -VM
Annak a virtuális számítógép-objektumnak a meghatározása, amelyre a parancsmag beállítja a méretet.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureVM](./Get-AzureVM.md)

[Update-AzureVM](./Update-AzureVM.md)


