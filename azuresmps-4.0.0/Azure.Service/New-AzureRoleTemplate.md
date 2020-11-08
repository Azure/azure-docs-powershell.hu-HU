---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015992"
---
# New-AzureRoleTemplate

## Áttekintés
A web-és a munkatársi szerepkör-sablonok létrehozása.

## SZINTAXISA

### Webszerepkör
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### WorkerRole
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **New-AzureRoleTemplate** parancsmag a webes és a munkavégző szerepkör-sablonokat hozza létre.

## Példák

### 1. példa: webszerepkör-sablon létrehozása
```
PS C:\> New-AzureRoleTemplate -Web
```

Ez a példa új webszerepkör-sablont hoz létre az aktuális könyvtár WebRoleTemplate nevű mappájában.

### 2. példa: munkatársi szerepkörű sablon létrehozása
```
PS C:\> New-AzureRoleTemplate -Worker
```

Ez a példa létrehoz egy új munkatársi szerepkör-sablont az aktuális könyvtár WebRoleTemplate nevű mappájában.

### 3. példa: szerepkör-sablon létrehozása egyéni címtárban
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

Ez a példa új webszerepkör-sablont hoz létre a MyWebRoleTemplate nevű címtárban az aktuális könyvtár helyett.

## PARAMÉTEREK

### -Output (kimenet)
A generált sablon kimeneti elérési útját adja meg.

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

### – Webes
Azt adja meg, hogy webszerepkör-sablont szeretne létrehozni.

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Munkás
Itt adhatja meg, hogy egy munkatársi szerepkör-sablont szeretne létrehozni.

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
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

[Add-AzureWebRole](./Add-AzureWebRole.md)

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)


