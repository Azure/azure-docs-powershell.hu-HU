---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016512"
---
# Get-AzureWebHostingPlan

## Áttekintés
Azure web hosting csomagok beolvasása az aktuális előfizetésben.

## SZINTAXISA

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **Get-AzureWebHostingPlan** parancsmag az Azure web hosting csomagokat az aktuális előfizetésben kapja meg.

A **Get-AzureWebHostingPlan** alapértelmezés szerint az aktuális előfizetésben minden Azure-fogadási csomagot megkapja, és egy olyan objektumot ad eredményül, amely alapvető információkat nyújt a tervekről.
A *tárhely* és a *név* paraméter használatakor a **Get-AzureWebHostingPlan** egy adott üzemeltetési terv objektumát adja eredményül.

Az aktuális előfizetés megkereséséhez használja a **Get-AzureSubscription** parancsmag *aktuális* paraméterét.
Az aktuális előfizetés módosításához használja a **Select-AzureSubscription** parancsmagot.

## Példák

### Példa 1: az összes Webtárhely-csomag beszerzése előfizetésben
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

Ez a parancs beilleszti az összes Azure web hosting csomagot a jelenlegi előfizetésbe.

### 2. példa: speciális Webtárhely-csomag beszerzése előfizetésben
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

Ez a parancs beolvassa a Default0 nevű webtárhely csomagot a jelenlegi előfizetésben a westeuropewebspace nevű webtárhelyen.

## PARAMÉTEREK

### -Name (név)
Az előfizetésben szereplő terv nevét adja meg.
Ez a parancsmag alapértelmezés szerint a jelenlegi előfizetéshez tartozó összes csomagot beilleszti.
Ez a paraméter nem támogatja a helyettesítő karaktereket.

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

### -WebSpaceName
Az előfizetésben lévő tárhely nevét adja meg.
Ez a parancsmag alapértelmezés szerint a megadott webtárhely összes webhelyét kapja.
Ez a paraméter nem támogatja a helyettesítő karaktereket.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

###  
A parancsmagot név szerint, de nem érték szerint is továbbíthatja.

## KIMENETEK

### Microsoft. WindowsAzure. Command. Utilities. websites. Services. webentitások. WebHostingPlan
Alapértelmezés szerint a **Get-AzureWebHostingPlan** a **WebHostingPlan** -objektumok tömbjét számítja ki.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

