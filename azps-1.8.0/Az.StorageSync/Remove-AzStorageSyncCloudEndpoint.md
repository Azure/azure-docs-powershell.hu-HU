---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 2d9ad2417041f39ea43f48813310869f1ea7f353
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668482"
---
# <span data-ttu-id="47d00-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="47d00-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="47d00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47d00-102">SYNOPSIS</span></span>
<span data-ttu-id="47d00-103">Ez a parancs a megadott Felhőbeli végpontot fogja törölni egy szinkronizálási csoportból.</span><span class="sxs-lookup"><span data-stu-id="47d00-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="47d00-104">Ha nincs legalább egy felhő végpontja, a szinkronizálási csoportban nem lehet más kiszolgálói végpontokat szinkronizálni.</span><span class="sxs-lookup"><span data-stu-id="47d00-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="47d00-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47d00-105">SYNTAX</span></span>

### <span data-ttu-id="47d00-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47d00-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47d00-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47d00-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47d00-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47d00-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47d00-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="47d00-109">DESCRIPTION</span></span>
<span data-ttu-id="47d00-110">Ez a parancs a megadott Felhőbeli végpontot fogja törölni egy szinkronizálási csoportból.</span><span class="sxs-lookup"><span data-stu-id="47d00-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="47d00-111">Az Azure-fájl megosztásakor a Felhőbeli végpontokra mutató hivatkozások érintetlenül maradnak a folyamat során.</span><span class="sxs-lookup"><span data-stu-id="47d00-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="47d00-112">Ez a parancs csak a leszereléshez szolgál.</span><span class="sxs-lookup"><span data-stu-id="47d00-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="47d00-113">A Felhőbeli végpontok eltávolítása romboló művelet.</span><span class="sxs-lookup"><span data-stu-id="47d00-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="47d00-114">A kiszolgálói végpontok nem szinkronizálhatók legalább egy Felhőbeli végpont nélkül.</span><span class="sxs-lookup"><span data-stu-id="47d00-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="47d00-115">Ezt a műveletet nem kell végrehajtani a szinkronizálási problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="47d00-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="47d00-116">Ha az Azure-fájlmegosztás ismét megjelenik ugyanahhoz a szinkronizálási csoporthoz, Felhőbeli végpontként, az ütközési fájlokat és más nem szándékolt következményeket okozhat.</span><span class="sxs-lookup"><span data-stu-id="47d00-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="47d00-117">Példák</span><span class="sxs-lookup"><span data-stu-id="47d00-117">EXAMPLES</span></span>

### <span data-ttu-id="47d00-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="47d00-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="47d00-119">Ez a parancs eltávolítja a Felhőbeli végpontot.</span><span class="sxs-lookup"><span data-stu-id="47d00-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="47d00-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47d00-120">PARAMETERS</span></span>

### <span data-ttu-id="47d00-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47d00-121">-AsJob</span></span>
<span data-ttu-id="47d00-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="47d00-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47d00-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d00-123">-DefaultProfile</span></span>
<span data-ttu-id="47d00-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47d00-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d00-125">-Force</span><span class="sxs-lookup"><span data-stu-id="47d00-125">-Force</span></span>
<span data-ttu-id="47d00-126">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="47d00-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="47d00-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47d00-127">-InputObject</span></span>
<span data-ttu-id="47d00-128">A CloudEndpoint bemeneti objektuma, normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="47d00-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="47d00-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47d00-129">-Name</span></span>
<span data-ttu-id="47d00-130">A CloudEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="47d00-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="47d00-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47d00-131">-PassThru</span></span>
<span data-ttu-id="47d00-132">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="47d00-132">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="47d00-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d00-133">-ResourceGroupName</span></span>
<span data-ttu-id="47d00-134">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="47d00-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="47d00-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47d00-135">-ResourceId</span></span>
<span data-ttu-id="47d00-136">CloudEndpoint erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="47d00-136">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="47d00-137">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="47d00-137">-StorageSyncServiceName</span></span>
<span data-ttu-id="47d00-138">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="47d00-138">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="47d00-139">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="47d00-139">-SyncGroupName</span></span>
<span data-ttu-id="47d00-140">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="47d00-140">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="47d00-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47d00-141">-Confirm</span></span>
<span data-ttu-id="47d00-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47d00-142">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47d00-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47d00-143">-WhatIf</span></span>
<span data-ttu-id="47d00-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47d00-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47d00-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47d00-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47d00-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d00-146">CommonParameters</span></span>
<span data-ttu-id="47d00-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47d00-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d00-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47d00-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d00-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47d00-149">INPUTS</span></span>

### <span data-ttu-id="47d00-150">Microsoft. Azure. Command. StorageSync. models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="47d00-150">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="47d00-151">System. String</span><span class="sxs-lookup"><span data-stu-id="47d00-151">System.String</span></span>

## <span data-ttu-id="47d00-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47d00-152">OUTPUTS</span></span>

### <span data-ttu-id="47d00-153">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="47d00-153">System.Object</span></span>
## <span data-ttu-id="47d00-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47d00-154">NOTES</span></span>

## <span data-ttu-id="47d00-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47d00-155">RELATED LINKS</span></span>
