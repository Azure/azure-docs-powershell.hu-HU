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
# <span data-ttu-id="506e0-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="506e0-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="506e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="506e0-102">SYNOPSIS</span></span>
<span data-ttu-id="506e0-103">Meghívja a tárolási fiók feladatátvételét.</span><span class="sxs-lookup"><span data-stu-id="506e0-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="506e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="506e0-104">SYNTAX</span></span>

### <span data-ttu-id="506e0-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="506e0-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="506e0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="506e0-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="506e0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="506e0-107">DESCRIPTION</span></span>
<span data-ttu-id="506e0-108">Meghívja a tárolási fiók feladatátvételét.</span><span class="sxs-lookup"><span data-stu-id="506e0-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="506e0-109">A feladatátvételi kérést kikapcsolhatja a tárolási fiók esetében az elérhetőségi problémák esetén.</span><span class="sxs-lookup"><span data-stu-id="506e0-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="506e0-110">A feladatátvétel a raktározási fiók elsődleges fürtjétől az RA-GRS-fiókok másodlagos fürtjébe kerül.</span><span class="sxs-lookup"><span data-stu-id="506e0-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="506e0-111">A másodlagos fürt a feladatátvétel után az elsődleges lesz.</span><span class="sxs-lookup"><span data-stu-id="506e0-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="506e0-112">Kérjük, hogy az alábbi módon befolyásolja a tárterület-fiókját, mielőtt elindítja a feladatátvételt: 1,1.</span><span class="sxs-lookup"><span data-stu-id="506e0-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="506e0-113">Kérjük, ellenőrizze a legutóbbi szinkronizálási időpontot a Paca szolgáltatás statisztikájának beszerzése ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) , a tábla szolgáltatás statisztikájának beszerzése ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) és a várólista-szolgáltatás statisztikájának beszerzése https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) ) segítségével</span><span class="sxs-lookup"><span data-stu-id="506e0-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="506e0-114">Ezek az adatvesztést elveszítheti, ha elindítja a feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="506e0-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="506e0-115">2. a feladatátvételt követően a tárolási fiók típusát helyi redundáns tárterületre (LRS) konvertálja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="506e0-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="506e0-116">A fiókját a Geo-redundáns tárterület (GRS) használatára is átalakíthatja.</span><span class="sxs-lookup"><span data-stu-id="506e0-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="506e0-117">3. miután újra engedélyezte a GRS a tárterülete számára, a Microsoft az új másodlagos régióba fogja replikálni az adatait.</span><span class="sxs-lookup"><span data-stu-id="506e0-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="506e0-118">A replikációs idő a replikálni kívánt adatmennyiségtől függ.</span><span class="sxs-lookup"><span data-stu-id="506e0-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="506e0-119">Felhívjuk a figyelmét arra, hogy a betöltéshez sávszélesség terheli.</span><span class="sxs-lookup"><span data-stu-id="506e0-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="506e0-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="506e0-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="506e0-121">Példák</span><span class="sxs-lookup"><span data-stu-id="506e0-121">EXAMPLES</span></span>

### <span data-ttu-id="506e0-122">1. példa: tárolási fiók feladatátvételének meghívása</span><span class="sxs-lookup"><span data-stu-id="506e0-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="506e0-123">Ez a parancs ellenőrzi a tárterület-fiók utolsó szinkronizálási időpontját, majd elindítja a feladatátvételt, a másodlagos fürt a feladatátvétel után válik elsődlegesnek.</span><span class="sxs-lookup"><span data-stu-id="506e0-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="506e0-124">Mivel a feladatátvétel hosszú időt vesz igénybe, azt sugallja, hogy a backend with-Asjob paraméterrel futtatja, majd megvárja a feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="506e0-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="506e0-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="506e0-125">PARAMETERS</span></span>

### <span data-ttu-id="506e0-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="506e0-126">-AsJob</span></span>
<span data-ttu-id="506e0-127">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="506e0-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="506e0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506e0-128">-DefaultProfile</span></span>
<span data-ttu-id="506e0-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="506e0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="506e0-130">-Force</span><span class="sxs-lookup"><span data-stu-id="506e0-130">-Force</span></span>
<span data-ttu-id="506e0-131">A fiók feladatátvételének kényszerítése</span><span class="sxs-lookup"><span data-stu-id="506e0-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="506e0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="506e0-132">-InputObject</span></span>
<span data-ttu-id="506e0-133">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="506e0-133">Storage account object</span></span>

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

### <span data-ttu-id="506e0-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="506e0-134">-Name</span></span>
<span data-ttu-id="506e0-135">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="506e0-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="506e0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506e0-136">-ResourceGroupName</span></span>
<span data-ttu-id="506e0-137">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="506e0-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="506e0-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="506e0-138">-Confirm</span></span>
<span data-ttu-id="506e0-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="506e0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="506e0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="506e0-140">-WhatIf</span></span>
<span data-ttu-id="506e0-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="506e0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="506e0-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="506e0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="506e0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506e0-143">CommonParameters</span></span>
<span data-ttu-id="506e0-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="506e0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506e0-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="506e0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506e0-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="506e0-146">INPUTS</span></span>

### <span data-ttu-id="506e0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="506e0-147">System.String</span></span>

## <span data-ttu-id="506e0-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="506e0-148">OUTPUTS</span></span>

### <span data-ttu-id="506e0-149">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="506e0-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="506e0-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="506e0-150">NOTES</span></span>

## <span data-ttu-id="506e0-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="506e0-151">RELATED LINKS</span></span>
