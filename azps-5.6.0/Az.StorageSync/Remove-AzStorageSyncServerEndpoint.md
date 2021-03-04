---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: ed0f21c7a3ad2105073cb81a8dff174d201f96ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929626"
---
# <span data-ttu-id="fea6c-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fea6c-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="fea6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fea6c-103">Ez a parancs törli a megadott kiszolgálói végpontot.</span><span class="sxs-lookup"><span data-stu-id="fea6c-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="fea6c-104">Az erre a helyre való szinkronizálás azonnal leáll.</span><span class="sxs-lookup"><span data-stu-id="fea6c-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="fea6c-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fea6c-105">SYNTAX</span></span>

### <span data-ttu-id="fea6c-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fea6c-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea6c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fea6c-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea6c-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fea6c-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea6c-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fea6c-109">DESCRIPTION</span></span>
<span data-ttu-id="fea6c-110">A kiszolgálóvégpont eltávolítása ártalmas művelet.</span><span class="sxs-lookup"><span data-stu-id="fea6c-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="fea6c-111">Ez a kiszolgálóhely leállítja a szinkronizálást.</span><span class="sxs-lookup"><span data-stu-id="fea6c-111">This server location will stop syncing.</span></span> <span data-ttu-id="fea6c-112">Ez a művelet nem végezhető el a szinkronizálási problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="fea6c-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="fea6c-113">Ha ezt a kiszolgálói helyet (incl. it's files) ismét hozzáadja ugyan ahhoz a szinkronizálási csoporthoz, mint egy kiszolgálói végpontot, az ütközési fájlokhoz és más nem szándékolt következményekhez vezethet.</span><span class="sxs-lookup"><span data-stu-id="fea6c-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="fea6c-114">Ez a parancs csak a leszerelésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="fea6c-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="fea6c-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fea6c-115">EXAMPLES</span></span>

### <span data-ttu-id="fea6c-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="fea6c-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="fea6c-117">Ez a parancs eltávolítja a kiszolgáló végpontját.</span><span class="sxs-lookup"><span data-stu-id="fea6c-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="fea6c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fea6c-118">PARAMETERS</span></span>

### <span data-ttu-id="fea6c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fea6c-119">-AsJob</span></span>
<span data-ttu-id="fea6c-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fea6c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fea6c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea6c-121">-DefaultProfile</span></span>
<span data-ttu-id="fea6c-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fea6c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea6c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fea6c-123">-Force</span></span>
<span data-ttu-id="fea6c-124">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="fea6c-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="fea6c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea6c-125">-InputObject</span></span>
<span data-ttu-id="fea6c-126">ServerEndpoint Input Object, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="fea6c-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fea6c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="fea6c-127">-Name</span></span>
<span data-ttu-id="fea6c-128">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="fea6c-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="fea6c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fea6c-129">-PassThru</span></span>
<span data-ttu-id="fea6c-130">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="fea6c-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="fea6c-131">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="fea6c-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="fea6c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea6c-132">-ResourceGroupName</span></span>
<span data-ttu-id="fea6c-133">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fea6c-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="fea6c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fea6c-134">-ResourceId</span></span>
<span data-ttu-id="fea6c-135">ServerEndpoint Resource Id</span><span class="sxs-lookup"><span data-stu-id="fea6c-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="fea6c-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fea6c-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="fea6c-137">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="fea6c-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="fea6c-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="fea6c-138">-SyncGroupName</span></span>
<span data-ttu-id="fea6c-139">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="fea6c-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="fea6c-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fea6c-140">-Confirm</span></span>
<span data-ttu-id="fea6c-141">A parancsmag futtatása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fea6c-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea6c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea6c-142">-WhatIf</span></span>
<span data-ttu-id="fea6c-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fea6c-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fea6c-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fea6c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea6c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea6c-145">CommonParameters</span></span>
<span data-ttu-id="fea6c-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea6c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea6c-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fea6c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea6c-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fea6c-148">INPUTS</span></span>

### <span data-ttu-id="fea6c-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fea6c-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="fea6c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="fea6c-150">System.String</span></span>

## <span data-ttu-id="fea6c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fea6c-151">OUTPUTS</span></span>

### <span data-ttu-id="fea6c-152">System.Object</span><span class="sxs-lookup"><span data-stu-id="fea6c-152">System.Object</span></span>
## <span data-ttu-id="fea6c-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fea6c-153">NOTES</span></span>

## <span data-ttu-id="fea6c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fea6c-154">RELATED LINKS</span></span>
