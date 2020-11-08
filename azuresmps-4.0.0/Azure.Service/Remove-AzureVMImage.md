---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016454"
---
# Remove-AzureVMImage

## Áttekintés
Eltávolítja az operációs rendszer képét a képtárházból.

## SZINTAXISA

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureVMImage** parancsmag eltávolítja az operációs rendszer képét a képtárházból.
Ez a parancsmag alapértelmezés szerint nem törli a kapcsolódó fizikai képblobot a tárolási fiókból.
Ha törölni szeretné a kapcsolódó virtuális merevlemezt (VHD), használja a **DeleteVHD** paramétert.

## Példák

### 1. példa: kép eltávolítása a képtárházból
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

Ez a parancs eltávolítja a Kép001 nevű képet a képtárházból.

### 2. példa: képek eltávolítása a képtárházból és a VHD-ből
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

Ez a parancs eltávolítja a Kép001 nevű képet a képtárházból, és törli a fizikai VHD-képet a tároló fiókból.

### 3. példa: az előfizetés környezetének beállítása, majd az összes kép eltávolítása
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

Ez a parancs beállítja az előfizetés környezetét, majd eltávolítja az összes képet a képtárházból, amelynek a címkéje tartalmazza a béta nevet.

## PARAMÉTEREK

### -DeleteVHD
Azt jelzi, hogy ez a parancsmag törli a fizikai VHD-képblobot a tárolási fiókból.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
A képtárházból eltávolítandó operációs rendszert vagy virtuális gép képét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Mentés-AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


