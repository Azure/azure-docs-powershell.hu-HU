---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: c2dd4abcf9e917d4a34ed548cd356e02875971b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940745"
---
# <span data-ttu-id="feddc-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="feddc-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="feddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feddc-102">SYNOPSIS</span></span>
<span data-ttu-id="feddc-103">Egy tárfiók feladatátvételét hívja meg.</span><span class="sxs-lookup"><span data-stu-id="feddc-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="feddc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="feddc-104">SYNTAX</span></span>

### <span data-ttu-id="feddc-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="feddc-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feddc-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="feddc-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feddc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="feddc-107">DESCRIPTION</span></span>
<span data-ttu-id="feddc-108">Egy tárfiók feladatátvételét hívja meg.</span><span class="sxs-lookup"><span data-stu-id="feddc-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="feddc-109">A tárhelyfiókok esetében a feladatátvételi kérés az elérhetőségi problémák esetén indítható el.</span><span class="sxs-lookup"><span data-stu-id="feddc-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="feddc-110">A feladatátvétel a tárfiók elsődleges fürtjében, az RA-GRS-fiókok másodlagos fürtjében történik.</span><span class="sxs-lookup"><span data-stu-id="feddc-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="feddc-111">A másodlagos fürt a feladatátvétel után elsődlegessé válik.</span><span class="sxs-lookup"><span data-stu-id="feddc-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="feddc-112">A feladatátvétel kezdeményezése előtt értse meg, hogy milyen hatással van a tárfiókjára: 1.1.</span><span class="sxs-lookup"><span data-stu-id="feddc-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="feddc-113">Ellenőrizze az utolsó szinkronizálási időt a GET Blob Service Stats (, A táblaszolgáltatás statszáma ( és a VÁRÓLISTÁS szolgáltatás statisztika https://docs.microsoft.com/rest/api/storageservices/get-blob-service-stats) https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) ( a https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) fiókjában) használatával.</span><span class="sxs-lookup"><span data-stu-id="feddc-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="feddc-114">Ezek az adatok elveszhetnek, ha ön kezdeményezi a feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="feddc-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="feddc-115">2.A feladatátvétel után a tárfiók típusát helyileg redundáns tárterületre (LRS) konvertálja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="feddc-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="feddc-116">Fiókját átalakíthatja georedundáns tárterület(GRS) használatára.</span><span class="sxs-lookup"><span data-stu-id="feddc-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="feddc-117">3.Miután ismét engedélyezi a GRS-t a tárfiókban, a Microsoft replikálja az adatokat az új másodlagos régióba.</span><span class="sxs-lookup"><span data-stu-id="feddc-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="feddc-118">A replikációs idő a replikálni szükséges adatok mennyiségtől függ.</span><span class="sxs-lookup"><span data-stu-id="feddc-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="feddc-119">Felhívjuk a figyelmét arra, hogy a rendszerindításkor sávszélesség-díjakat kell fizetni.</span><span class="sxs-lookup"><span data-stu-id="feddc-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="feddc-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="feddc-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="feddc-121">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="feddc-121">EXAMPLES</span></span>

### <span data-ttu-id="feddc-122">1. példa: Tárfiók feladatátvételének meghívása</span><span class="sxs-lookup"><span data-stu-id="feddc-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="feddc-123">Ez a parancs ellenőrzi egy tárfiók utolsó szinkronizálási idejét, majd meghívja a feladatátvételt, a másodlagos fürt a feladatátvétel után elsődlegessé válik.</span><span class="sxs-lookup"><span data-stu-id="feddc-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="feddc-124">Mivel a feladatátvétel sokáig tart, javasoljuk, hogy futtassa a backendben -As job paraméterrel, majd várja meg, amíg a feladat befejeződik.</span><span class="sxs-lookup"><span data-stu-id="feddc-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="feddc-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feddc-125">PARAMETERS</span></span>

### <span data-ttu-id="feddc-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="feddc-126">-AsJob</span></span>
<span data-ttu-id="feddc-127">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="feddc-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="feddc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feddc-128">-DefaultProfile</span></span>
<span data-ttu-id="feddc-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="feddc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feddc-130">-Force</span><span class="sxs-lookup"><span data-stu-id="feddc-130">-Force</span></span>
<span data-ttu-id="feddc-131">A fiók feladatátvételének kényszerítve</span><span class="sxs-lookup"><span data-stu-id="feddc-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="feddc-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feddc-132">-InputObject</span></span>
<span data-ttu-id="feddc-133">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="feddc-133">Storage account object</span></span>

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

### <span data-ttu-id="feddc-134">-Name</span><span class="sxs-lookup"><span data-stu-id="feddc-134">-Name</span></span>
<span data-ttu-id="feddc-135">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="feddc-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="feddc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feddc-136">-ResourceGroupName</span></span>
<span data-ttu-id="feddc-137">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="feddc-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="feddc-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="feddc-138">-Confirm</span></span>
<span data-ttu-id="feddc-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="feddc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feddc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feddc-140">-WhatIf</span></span>
<span data-ttu-id="feddc-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="feddc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feddc-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="feddc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feddc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feddc-143">CommonParameters</span></span>
<span data-ttu-id="feddc-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feddc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feddc-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feddc-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feddc-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="feddc-146">INPUTS</span></span>

### <span data-ttu-id="feddc-147">System.String</span><span class="sxs-lookup"><span data-stu-id="feddc-147">System.String</span></span>

## <span data-ttu-id="feddc-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="feddc-148">OUTPUTS</span></span>

### <span data-ttu-id="feddc-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="feddc-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="feddc-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="feddc-150">NOTES</span></span>

## <span data-ttu-id="feddc-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="feddc-151">RELATED LINKS</span></span>
