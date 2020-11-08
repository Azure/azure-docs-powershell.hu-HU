---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016532"
---
# Get-AzureVMImage

## Áttekintés
A képtárházban egy operációs rendszer vagy egy virtuális gép tulajdonságainak egy vagy több elemét kapja.

## SZINTAXISA

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureVMImage** parancsmag egy vagy több operációs rendszer vagy egy virtuális gép egy vagy több, a képtárházban lévő képére vonatkozó tulajdonságot kap.
A parancsmag információt ad eredményül a tárházban lévő összes képhez, vagy ha a kép neve meg van határozva, akkor egy bizonyos képre.

## Példák

### Példa 1: adott képobjektum beszerzése az aktuális képtárházból.
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

Ez a parancs a Kép001 nevű kép objektumot az aktuális képtárházból kapja meg.

### 2. példa: az aktuális képtárház összes képének beolvasása
```
PS C:\> Get-AzureVMImage
```

A parancs a jelenlegi képtárházból olvassa be az összes képet.

### 3. példa: az előfizetés környezetének beállítása, majd az összes kép beolvasása
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

Ez a parancs beállítja az előfizetés környezetét, majd beolvassa az összes képet a képtárházból.

## PARAMÉTEREK

### -ImageName
Itt adhatja meg az operációs rendszer vagy a virtuális gép képét a képtárházban.
Ha nem adja meg ezt a paramétert, a program az összes képet visszaadja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Mentés-AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


