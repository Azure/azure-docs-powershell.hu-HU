---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015711"
---
# Add-AzureWebRole

## Áttekintés
Webes munkatársi szerepkör felvétele

## SZINTAXISA

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

Az **Add-AzureWebRole** parancsmag egy webes munkatársi szerepkört ad hozzá.

## Példák

### Példa 1: alapértelmezett szerepkör felvétele
```
PS C:\> Add-AzureWebRole
```

Ez a parancs olyan webszerepkört hoz létre, amely a Webrole1 alapértelmezett konfigurációjának neve és egyetlen példánya.

### 2. példa: szerepkör felvétele névvel
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

A parancs hozzáadja a MyWebRole nevű egyetlen webszerepkört az aktuális alkalmazáshoz.

### 3. példa: szerepkör felvétele név és előfordulási számmal
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

A parancs hozzáadja a MyWebRole nevű webszerepkört az aktuális alkalmazáshoz.
A parancsmagban a szerepkör-példányok száma 2.

### 4. példa: szerepkör felvétele névvel és sablonnal
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

A parancs hozzáadja a MyWebRole nevű egyetlen webszerepkört az aktuális alkalmazáshoz.
A parancs az állványzat sablonként a MyWebTemplateFolder nevű mappát adja meg.

## PARAMÉTEREK

### -Példányok
A példányok számát adja meg.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A webes szerepkör nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

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

### -TemplateFolder
A sablon mappáját adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)

[Új – AzureRoleTemplate](./New-AzureRoleTemplate.md)


