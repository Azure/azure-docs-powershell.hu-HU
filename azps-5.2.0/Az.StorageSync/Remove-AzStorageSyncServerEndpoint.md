---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366573"
---
# <span data-ttu-id="ddf66-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ddf66-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="ddf66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddf66-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf66-103">Ez a parancs törli a megadott kiszolgálói végpontot.</span><span class="sxs-lookup"><span data-stu-id="ddf66-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="ddf66-104">Az erre a helyre való szinkronizálás azonnal leáll.</span><span class="sxs-lookup"><span data-stu-id="ddf66-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="ddf66-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ddf66-105">SYNTAX</span></span>

### <span data-ttu-id="ddf66-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ddf66-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddf66-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddf66-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddf66-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddf66-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddf66-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ddf66-109">DESCRIPTION</span></span>
<span data-ttu-id="ddf66-110">A kiszolgálóvégpont eltávolítása ártalmas művelet.</span><span class="sxs-lookup"><span data-stu-id="ddf66-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="ddf66-111">Ez a kiszolgálóhely leállítja a szinkronizálást.</span><span class="sxs-lookup"><span data-stu-id="ddf66-111">This server location will stop syncing.</span></span> <span data-ttu-id="ddf66-112">Ez a művelet nem végezhető el a szinkronizálási problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="ddf66-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="ddf66-113">Ha ezt a kiszolgálói helyet (incl. it's files) ismét hozzáadja ugyan ahhoz a szinkronizálási csoporthoz, mint egy kiszolgálói végpontot, az ütközési fájlokhoz és más nem szándékolt következményekhez vezethet.</span><span class="sxs-lookup"><span data-stu-id="ddf66-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="ddf66-114">Ez a parancs csak a leszerelésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="ddf66-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="ddf66-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ddf66-115">EXAMPLES</span></span>

### <span data-ttu-id="ddf66-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="ddf66-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="ddf66-117">Ez a parancs eltávolítja a kiszolgáló végpontját.</span><span class="sxs-lookup"><span data-stu-id="ddf66-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="ddf66-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddf66-118">PARAMETERS</span></span>

### <span data-ttu-id="ddf66-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddf66-119">-AsJob</span></span>
<span data-ttu-id="ddf66-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ddf66-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddf66-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf66-121">-DefaultProfile</span></span>
<span data-ttu-id="ddf66-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddf66-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddf66-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ddf66-123">-Force</span></span>
<span data-ttu-id="ddf66-124">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="ddf66-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="ddf66-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddf66-125">-InputObject</span></span>
<span data-ttu-id="ddf66-126">ServerEndpoint Input Object, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="ddf66-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ddf66-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ddf66-127">-Name</span></span>
<span data-ttu-id="ddf66-128">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="ddf66-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="ddf66-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddf66-129">-PassThru</span></span>
<span data-ttu-id="ddf66-130">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="ddf66-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="ddf66-131">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="ddf66-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="ddf66-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf66-132">-ResourceGroupName</span></span>
<span data-ttu-id="ddf66-133">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ddf66-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="ddf66-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddf66-134">-ResourceId</span></span>
<span data-ttu-id="ddf66-135">ServerEndpoint Resource Id</span><span class="sxs-lookup"><span data-stu-id="ddf66-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="ddf66-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ddf66-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="ddf66-137">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="ddf66-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ddf66-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf66-138">-SyncGroupName</span></span>
<span data-ttu-id="ddf66-139">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="ddf66-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ddf66-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddf66-140">-Confirm</span></span>
<span data-ttu-id="ddf66-141">A parancsmag futtatása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ddf66-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddf66-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddf66-142">-WhatIf</span></span>
<span data-ttu-id="ddf66-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ddf66-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddf66-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ddf66-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddf66-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf66-145">CommonParameters</span></span>
<span data-ttu-id="ddf66-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf66-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf66-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf66-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf66-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddf66-148">INPUTS</span></span>

### <span data-ttu-id="ddf66-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ddf66-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="ddf66-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ddf66-150">System.String</span></span>

## <span data-ttu-id="ddf66-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddf66-151">OUTPUTS</span></span>

### <span data-ttu-id="ddf66-152">System.Object</span><span class="sxs-lookup"><span data-stu-id="ddf66-152">System.Object</span></span>
## <span data-ttu-id="ddf66-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ddf66-153">NOTES</span></span>

## <span data-ttu-id="ddf66-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddf66-154">RELATED LINKS</span></span>
