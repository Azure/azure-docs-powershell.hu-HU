---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466844"
---
# <span data-ttu-id="c1aee-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1aee-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="c1aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1aee-102">SYNOPSIS</span></span>
<span data-ttu-id="c1aee-103">Ez a parancs lehetővé teszi a kiszolgáló végpontjának módosítható paramétereinek módosításait.</span><span class="sxs-lookup"><span data-stu-id="c1aee-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="c1aee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1aee-104">SYNTAX</span></span>

### <span data-ttu-id="c1aee-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1aee-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1aee-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1aee-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1aee-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1aee-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1aee-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1aee-108">DESCRIPTION</span></span>
<span data-ttu-id="c1aee-109">Ez a parancs lehetővé teszi a kiszolgáló végpontjának módosítható paramétereinek módosításait.</span><span class="sxs-lookup"><span data-stu-id="c1aee-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="c1aee-110">A felhőréteg-ezés és a felhőszintű rétegezésre vonatkozó házirendek például bármikor módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="c1aee-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="c1aee-111">A kiszolgálói végpont számos aspektusa, például a helyi elérési út, nem módosítható a kiszolgáló végpontjának létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="c1aee-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="c1aee-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1aee-112">EXAMPLES</span></span>

### <span data-ttu-id="c1aee-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="c1aee-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="c1aee-114">Ez a példa két műveletet hajt végre, egy új felhőszintű rétegezés házirendet állít be a megadott kiszolgálói végponton, amely arra irányítja a kiszolgálót, hogy az összes olyan fájlt rétegesítse, amelyekhez az elmúlt 30 napban nem fértek hozzá, valamint letiltja az offline adatátviteli módot is, amelyet eredetileg ezen a kiszolgálói végponton engedélyeztek a létrehozása során.</span><span class="sxs-lookup"><span data-stu-id="c1aee-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="c1aee-115">Az offline adatátvitel a tömeges áttelepítési szolgáltatásokkal, például az Azure Data Box-zal való együttműködés részeként használatos.</span><span class="sxs-lookup"><span data-stu-id="c1aee-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="c1aee-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1aee-116">PARAMETERS</span></span>

### <span data-ttu-id="c1aee-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1aee-117">-AsJob</span></span>
<span data-ttu-id="c1aee-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c1aee-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1aee-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="c1aee-119">-CloudTiering</span></span>
<span data-ttu-id="c1aee-120">Felhőszintű rétegezés paramétere</span><span class="sxs-lookup"><span data-stu-id="c1aee-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="c1aee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1aee-121">-DefaultProfile</span></span>
<span data-ttu-id="c1aee-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1aee-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1aee-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1aee-123">-InputObject</span></span>
<span data-ttu-id="c1aee-124">SyncGroup-objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="c1aee-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c1aee-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c1aee-125">-Name</span></span>
<span data-ttu-id="c1aee-126">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="c1aee-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="c1aee-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="c1aee-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="c1aee-128">Cloud Seeded Data Parameter</span><span class="sxs-lookup"><span data-stu-id="c1aee-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="c1aee-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="c1aee-129">-localCacheMode</span></span>
<span data-ttu-id="c1aee-130">Local cache mode Parameter</span><span class="sxs-lookup"><span data-stu-id="c1aee-130">Local cache mode Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1aee-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1aee-131">-ResourceGroupName</span></span>
<span data-ttu-id="c1aee-132">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c1aee-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="c1aee-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1aee-133">-ResourceId</span></span>
<span data-ttu-id="c1aee-134">ServerEndpoint Resource Id</span><span class="sxs-lookup"><span data-stu-id="c1aee-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="c1aee-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c1aee-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="c1aee-136">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="c1aee-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c1aee-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c1aee-137">-SyncGroupName</span></span>
<span data-ttu-id="c1aee-138">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="c1aee-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="c1aee-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="c1aee-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="c1aee-140">A napnál régebbi tier fájlok paramétere</span><span class="sxs-lookup"><span data-stu-id="c1aee-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="c1aee-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="c1aee-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="c1aee-142">Volume Free Space Percent Parameter</span><span class="sxs-lookup"><span data-stu-id="c1aee-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="c1aee-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1aee-143">-Confirm</span></span>
<span data-ttu-id="c1aee-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c1aee-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1aee-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1aee-145">-WhatIf</span></span>
<span data-ttu-id="c1aee-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c1aee-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1aee-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1aee-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1aee-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1aee-148">CommonParameters</span></span>
<span data-ttu-id="c1aee-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1aee-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1aee-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1aee-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1aee-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1aee-151">INPUTS</span></span>

### <span data-ttu-id="c1aee-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c1aee-152">System.String</span></span>

### <span data-ttu-id="c1aee-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1aee-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="c1aee-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1aee-154">OUTPUTS</span></span>

### <span data-ttu-id="c1aee-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1aee-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="c1aee-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1aee-156">NOTES</span></span>

## <span data-ttu-id="c1aee-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1aee-157">RELATED LINKS</span></span>
