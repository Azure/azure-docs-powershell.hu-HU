---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016505"
---
# Get-AzureWinRMUri

## Áttekintés
Megkapja az URI-t a WinRM HTTPS-figyelőhöz egy virtuális géphez vagy egy hosztolt szolgáltatásban lévő virtuális gépek listájával.

## SZINTAXISA

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureWinRMUri** parancsmag a Windows távfelügyelet (WinRM) https-figyelésének URI-jét egy virtuális gépre vagy egy hosztolt szolgáltatás virtuális gépei listájára kapja.

## Példák

### Példa 1: a WinRM HTTPS-figyelő URI-ja beszerzése virtuális gépre
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

Ez a parancs a WinRM HTTPS-figyelő UIR a virtuális gépre.

### 2. példa: a WinRM HTTPS-figyelő URI-azonosítójának beszerzése egy adott szolgáltatás virtuális géphez
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

Ez a parancs a WinRM HTTPS-figyelő UIR a virtuális gépre.

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

### -Name (név)
Annak a virtuális gépnek a neve, amelyhez a WinRM-URI jön létre.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### -Szolgáltatásnév
Annak a Microsoft Azure-szolgáltatásnak a neve, amely a virtuális gépet tárolja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[Új – AzureVM](./New-AzureVM.md)

[Új – AzureQuickVM](./New-AzureQuickVM.md)


