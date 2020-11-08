---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194174"
---
# Invoke-AzStorageAccountFailover

## Áttekintés
Meghívja a tárolási fiók feladatátvételét.

## SZINTAXISA

### AccountName (alapértelmezett)
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Meghívja a tárolási fiók feladatátvételét. A feladatátvételi kérést kikapcsolhatja a tárolási fiók esetében az elérhetőségi problémák esetén. A feladatátvétel a raktározási fiók elsődleges fürtjétől az RA-GRS-fiókok másodlagos fürtjébe kerül. A másodlagos fürt a feladatátvétel után az elsődleges lesz.
Kérjük, hogy az alábbi módon befolyásolja a tárterület-fiókját, mielőtt elindítja a feladatátvételt: 1,1. Kérjük, ellenőrizze a legutóbbi szinkronizálási időpontot a Paca szolgáltatás statisztikájának beszerzése ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) , a tábla szolgáltatás statisztikájának beszerzése ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) és a várólista-szolgáltatás statisztikájának beszerzése https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) ) segítségével Ezek az adatvesztést elveszítheti, ha elindítja a feladatátvételt.
2. a feladatátvételt követően a tárolási fiók típusát helyi redundáns tárterületre (LRS) konvertálja a rendszer. A fiókját a Geo-redundáns tárterület (GRS) használatára is átalakíthatja.
3. miután újra engedélyezte a GRS a tárterülete számára, a Microsoft az új másodlagos régióba fogja replikálni az adatait. A replikációs idő a replikálni kívánt adatmennyiségtől függ. Felhívjuk a figyelmét arra, hogy a betöltéshez sávszélesség terheli. https://azure.microsoft.com/en-us/pricing/details/bandwidth/

## Példák

### 1. példa: tárolási fiók feladatátvételének meghívása
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

Ez a parancs ellenőrzi a tárterület-fiók utolsó szinkronizálási időpontját, majd elindítja a feladatátvételt, a másodlagos fürt a feladatátvétel után válik elsődlegesnek. Mivel a feladatátvétel hosszú időt vesz igénybe, azt sugallja, hogy a backend with-Asjob paraméterrel futtatja, majd megvárja a feladat befejezését.

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
A fiók feladatátvételének kényszerítése

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Storage Account objektum

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Tárolási fiók neve.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
