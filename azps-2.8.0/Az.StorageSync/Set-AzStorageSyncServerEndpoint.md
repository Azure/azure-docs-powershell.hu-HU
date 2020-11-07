---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 23aab4561e8127c67be4d9f751b250bc3fb6d1a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838239"
---
# <span data-ttu-id="4d5d2-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d5d2-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="4d5d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="4d5d2-103">Ez a parancs lehetővé teszi a kiszolgálói végpontok állítható paramétereinek módosítását.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="4d5d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d5d2-104">SYNTAX</span></span>

### <span data-ttu-id="4d5d2-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d5d2-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d5d2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d5d2-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d5d2-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d5d2-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d5d2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d5d2-108">DESCRIPTION</span></span>
<span data-ttu-id="4d5d2-109">Ez a parancs lehetővé teszi a kiszolgálói végpontok állítható paramétereinek módosítását.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="4d5d2-110">Előfordulhat, hogy a felhőalapú rétegekkel és a Felhőbeli rétegekkel kapcsolatos házirendek például bármikor módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="4d5d2-111">A kiszolgálói végpontok (például a helyi elérési út) számos jellemzője nem módosítható a kiszolgálói végpont létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="4d5d2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4d5d2-112">EXAMPLES</span></span>

### <span data-ttu-id="4d5d2-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4d5d2-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="4d5d2-114">Ez a példa két műveletet hajt végre, a megadott kiszolgálói végponton egy új felhőalapú adattípusi házirendet hoz létre, amely a kiszolgálót az elmúlt 30 napban nem elérhető fájlok kiválasztására irányítja, és letiltja az offline adatátviteli módot is, amelyet eredetileg a kiszolgáló végpontján engedélyeztek az adott kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="4d5d2-115">Az offline adatátvitelt a tömeges áttelepítési szolgáltatásokkal való együttműködés részeként használják, például Azure Data (például Azure Data box).</span><span class="sxs-lookup"><span data-stu-id="4d5d2-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="4d5d2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d5d2-116">PARAMETERS</span></span>

### <span data-ttu-id="4d5d2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d5d2-117">-AsJob</span></span>
<span data-ttu-id="4d5d2-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4d5d2-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d5d2-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="4d5d2-119">-CloudTiering</span></span>
<span data-ttu-id="4d5d2-120">Felhőbeli adatmeghatározás paraméter</span><span class="sxs-lookup"><span data-stu-id="4d5d2-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="4d5d2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d5d2-121">-DefaultProfile</span></span>
<span data-ttu-id="4d5d2-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d5d2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d5d2-123">-InputObject</span></span>
<span data-ttu-id="4d5d2-124">SyncGroup objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d2-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d5d2-125">-Name</span></span>
<span data-ttu-id="4d5d2-126">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d2-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="4d5d2-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="4d5d2-128">Felhőbe minősített adatérték paraméter</span><span class="sxs-lookup"><span data-stu-id="4d5d2-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="4d5d2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d5d2-129">-ResourceGroupName</span></span>
<span data-ttu-id="4d5d2-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d5d2-131">-ResourceId</span></span>
<span data-ttu-id="4d5d2-132">ServerEndpoint erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="4d5d2-132">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d2-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4d5d2-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="4d5d2-134">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-134">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d2-135">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4d5d2-135">-SyncGroupName</span></span>
<span data-ttu-id="4d5d2-136">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-136">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d2-137">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="4d5d2-137">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="4d5d2-138">A Days paraméternél régebbi fájlok</span><span class="sxs-lookup"><span data-stu-id="4d5d2-138">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d2-139">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="4d5d2-139">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="4d5d2-140">Mennyiségi szabad terület százalékos értéke</span><span class="sxs-lookup"><span data-stu-id="4d5d2-140">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d2-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d5d2-141">-Confirm</span></span>
<span data-ttu-id="4d5d2-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d5d2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d5d2-143">-WhatIf</span></span>
<span data-ttu-id="4d5d2-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d5d2-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d5d2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d5d2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d5d2-146">CommonParameters</span></span>
<span data-ttu-id="4d5d2-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d5d2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d5d2-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d5d2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d5d2-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d5d2-149">INPUTS</span></span>

### <span data-ttu-id="4d5d2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4d5d2-150">System.String</span></span>

### <span data-ttu-id="4d5d2-151">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d5d2-151">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4d5d2-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d5d2-152">OUTPUTS</span></span>

### <span data-ttu-id="4d5d2-153">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d5d2-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4d5d2-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d5d2-154">NOTES</span></span>

## <span data-ttu-id="4d5d2-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d5d2-155">RELATED LINKS</span></span>
