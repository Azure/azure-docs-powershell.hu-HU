---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016448"
---
# Remove-AzureVMCustomScriptExtension

## Áttekintés
Eltávolítja az egyéni parancsfájl-kiterjesztést egy virtuális gépről.

## SZINTAXISA

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureVMCustomScriptExtension** parancsmag eltávolítja az egyéni parancsfájl-kiterjesztést egy virtuális gépről.

## Példák

### Példa 1: a virtuális gép egyéni parancsfájl-bővítményének eltávolítása
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

Ez a parancs eltávolítja az Azure Virtual Machine egyéni parancsfájl-bővítményét a megadott virtuális gépről a változó $VM tárolva.

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
Az állandó virtuálisgép-objektumot adja meg.

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

[Get-AzureVMCustomScriptExtension](./Get-AzureVMCustomScriptExtension.md)

[Set-AzureVMCustomScriptExtension](./Set-AzureVMCustomScriptExtension.md)


