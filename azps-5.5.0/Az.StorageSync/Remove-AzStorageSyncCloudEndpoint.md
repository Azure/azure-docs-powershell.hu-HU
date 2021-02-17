---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: ae3d75b90e6e095072b8e6e6543e2f122fe4cb50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164675"
---
# <span data-ttu-id="41ea8-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="41ea8-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="41ea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="41ea8-103">Ez a parancs törli a megadott felhőbeli végpontot egy szinkronizálási csoportból.</span><span class="sxs-lookup"><span data-stu-id="41ea8-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="41ea8-104">Legalább egy felhőbeli végpont nélkül a szinkronizálási csoport egyetlen másik kiszolgálói végpontja sem tud szinkronizálni.</span><span class="sxs-lookup"><span data-stu-id="41ea8-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="41ea8-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41ea8-105">SYNTAX</span></span>

### <span data-ttu-id="41ea8-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41ea8-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ea8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41ea8-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ea8-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41ea8-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41ea8-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41ea8-109">DESCRIPTION</span></span>
<span data-ttu-id="41ea8-110">Ez a parancs törli a megadott felhőbeli végpontot egy szinkronizálási csoportból.</span><span class="sxs-lookup"><span data-stu-id="41ea8-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="41ea8-111">Az Azure-fájl megosztásakor a felhőbeli végponthivatkozások érintetlenek maradnak a folyamat során.</span><span class="sxs-lookup"><span data-stu-id="41ea8-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="41ea8-112">Ez a parancs csak leszerelésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="41ea8-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="41ea8-113">A felhőbeli végpontok eltávolítása ártalmas művelet.</span><span class="sxs-lookup"><span data-stu-id="41ea8-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="41ea8-114">A kiszolgálói végpontok csak akkor szinkronizálódnak, ha legalább egy felhőbeli végpont jelen van.</span><span class="sxs-lookup"><span data-stu-id="41ea8-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="41ea8-115">Ez a művelet nem végezhető el a szinkronizálási problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="41ea8-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="41ea8-116">Ha ezt az Azure-fájlmegosztást ismét hozzáadják ugyanannak a szinkronizálási csoportnak , mint felhőbeli végpontnak, az ütközési fájlokhoz és más nem kívánt következményekhez vezethet.</span><span class="sxs-lookup"><span data-stu-id="41ea8-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="41ea8-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41ea8-117">EXAMPLES</span></span>

### <span data-ttu-id="41ea8-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="41ea8-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="41ea8-119">Ez a parancs eltávolítja a felhőbeli végpontot.</span><span class="sxs-lookup"><span data-stu-id="41ea8-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="41ea8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41ea8-120">PARAMETERS</span></span>

### <span data-ttu-id="41ea8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41ea8-121">-AsJob</span></span>
<span data-ttu-id="41ea8-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="41ea8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41ea8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ea8-123">-DefaultProfile</span></span>
<span data-ttu-id="41ea8-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41ea8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41ea8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="41ea8-125">-Force</span></span>
<span data-ttu-id="41ea8-126">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="41ea8-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="41ea8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41ea8-127">-InputObject</span></span>
<span data-ttu-id="41ea8-128">CloudEndpoint Input Object, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="41ea8-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41ea8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="41ea8-129">-Name</span></span>
<span data-ttu-id="41ea8-130">A CloudEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="41ea8-130">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ea8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41ea8-131">-PassThru</span></span>
<span data-ttu-id="41ea8-132">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="41ea8-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="41ea8-133">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="41ea8-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="41ea8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41ea8-134">-ResourceGroupName</span></span>
<span data-ttu-id="41ea8-135">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="41ea8-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="41ea8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41ea8-136">-ResourceId</span></span>
<span data-ttu-id="41ea8-137">CloudEndpoint Resource Id</span><span class="sxs-lookup"><span data-stu-id="41ea8-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="41ea8-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="41ea8-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="41ea8-139">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="41ea8-139">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ea8-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="41ea8-140">-SyncGroupName</span></span>
<span data-ttu-id="41ea8-141">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="41ea8-141">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ea8-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41ea8-142">-Confirm</span></span>
<span data-ttu-id="41ea8-143">A parancsmag futtatása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="41ea8-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41ea8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41ea8-144">-WhatIf</span></span>
<span data-ttu-id="41ea8-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="41ea8-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41ea8-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41ea8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41ea8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ea8-147">CommonParameters</span></span>
<span data-ttu-id="41ea8-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41ea8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ea8-149">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41ea8-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ea8-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41ea8-150">INPUTS</span></span>

### <span data-ttu-id="41ea8-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="41ea8-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="41ea8-152">System.String</span><span class="sxs-lookup"><span data-stu-id="41ea8-152">System.String</span></span>

## <span data-ttu-id="41ea8-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41ea8-153">OUTPUTS</span></span>

### <span data-ttu-id="41ea8-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="41ea8-154">System.Object</span></span>
## <span data-ttu-id="41ea8-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41ea8-155">NOTES</span></span>

## <span data-ttu-id="41ea8-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41ea8-156">RELATED LINKS</span></span>
