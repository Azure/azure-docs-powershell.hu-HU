---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015952"
---
# Set-AzureServiceProjectRole

## Áttekintés
Megadja a szerepkör példányainak vagy futásidejű verziójának számát.

## SZINTAXISA

### Példányok
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Futtatókörnyezet
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### VMSize
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **set-AzureServiceProjectRole** parancsmag a megadott szerepkörhöz tartozó szerepkör-példányok számát határozza meg.

## Példák

### Példa 1: webes szerepkör példányainak beállítása
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

A MyWebRole1 nevű webszerepkör példányainak számát határozza meg.

### 2. példa: a munkatársi szerepkör példányainak beállítása
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

A WorkerRole1 és a 2 nevű munkatársi szerepkör szerepkör-példányának számát állítja be.

### 3. példa: egy szerepkör-szolgáltatás futásidejű verziójának beállítása
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

A 0.6.20 szerepkör-MyRole1 a node.exe futtatókörnyezet-verziót állítja be.

## PARAMÉTEREK

### -Példányok
A megadott webes vagy munkatársi szerepkörhöz tartozó szerepkör-példányok számát adja meg.

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -RoleName
A módosítani kívánt webes vagy munkatársi szerepkör nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Futtatókörnyezet
A megadott szerepkörhöz hozzáadni kívánt futtatókörnyezetet adja meg.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzió
Itt adhatja meg a szerepkörhöz hozzáadni kívánt futásidejű verziót.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
A szerepkör virtuális gép méretét adja meg.

```yaml
Type: String
Parameter Sets: VMSize
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

###  
A virtuális gép méretét adja meg.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


