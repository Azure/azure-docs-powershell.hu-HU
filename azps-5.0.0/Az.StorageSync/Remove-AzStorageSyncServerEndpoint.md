---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186329"
---
# <span data-ttu-id="fa727-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa727-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="fa727-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa727-102">SYNOPSIS</span></span>
<span data-ttu-id="fa727-103">Ez a parancs törli a megadott kiszolgálói végpontot.</span><span class="sxs-lookup"><span data-stu-id="fa727-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="fa727-104">A szinkronizálás erre a helyre beállítás azonnal megszűnik.</span><span class="sxs-lookup"><span data-stu-id="fa727-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="fa727-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa727-105">SYNTAX</span></span>

### <span data-ttu-id="fa727-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa727-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa727-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa727-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa727-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa727-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa727-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa727-109">DESCRIPTION</span></span>
<span data-ttu-id="fa727-110">A kiszolgáló végpontjának eltávolítása romboló művelet.</span><span class="sxs-lookup"><span data-stu-id="fa727-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="fa727-111">Ez a kiszolgálói hely megszünteti a szinkronizálást.</span><span class="sxs-lookup"><span data-stu-id="fa727-111">This server location will stop syncing.</span></span> <span data-ttu-id="fa727-112">Ezt a műveletet nem kell végrehajtani a szinkronizálási problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="fa727-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="fa727-113">Ha ez a kiszolgáló-hely (beleértve a fájlokat is) ismét hozzáadódik ugyanahhoz a szinkronizálási csoporthoz, mint a kiszolgáló végpontja, akkor az ütközési fájlok és más nem szándékolt következmények eléréséhez vezethet.</span><span class="sxs-lookup"><span data-stu-id="fa727-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="fa727-114">Ez a parancs csak a leszerelésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="fa727-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="fa727-115">Példák</span><span class="sxs-lookup"><span data-stu-id="fa727-115">EXAMPLES</span></span>

### <span data-ttu-id="fa727-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fa727-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="fa727-117">Ez a parancs eltávolítja a kiszolgáló végpontját.</span><span class="sxs-lookup"><span data-stu-id="fa727-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="fa727-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa727-118">PARAMETERS</span></span>

### <span data-ttu-id="fa727-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa727-119">-AsJob</span></span>
<span data-ttu-id="fa727-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fa727-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa727-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa727-121">-DefaultProfile</span></span>
<span data-ttu-id="fa727-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa727-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa727-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fa727-123">-Force</span></span>
<span data-ttu-id="fa727-124">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="fa727-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="fa727-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa727-125">-InputObject</span></span>
<span data-ttu-id="fa727-126">A ServerEndpoint bemeneti objektuma, normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="fa727-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="fa727-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa727-127">-Name</span></span>
<span data-ttu-id="fa727-128">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="fa727-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="fa727-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa727-129">-PassThru</span></span>
<span data-ttu-id="fa727-130">A normál végrehajtásban ez a parancsmag nem ad értéket a sikernek.</span><span class="sxs-lookup"><span data-stu-id="fa727-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="fa727-131">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után a csővezetéknek ad értéket.</span><span class="sxs-lookup"><span data-stu-id="fa727-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="fa727-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa727-132">-ResourceGroupName</span></span>
<span data-ttu-id="fa727-133">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fa727-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="fa727-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa727-134">-ResourceId</span></span>
<span data-ttu-id="fa727-135">ServerEndpoint erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="fa727-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="fa727-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fa727-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="fa727-137">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="fa727-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="fa727-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="fa727-138">-SyncGroupName</span></span>
<span data-ttu-id="fa727-139">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="fa727-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="fa727-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa727-140">-Confirm</span></span>
<span data-ttu-id="fa727-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa727-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa727-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa727-142">-WhatIf</span></span>
<span data-ttu-id="fa727-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa727-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa727-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa727-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa727-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa727-145">CommonParameters</span></span>
<span data-ttu-id="fa727-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa727-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa727-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa727-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa727-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa727-148">INPUTS</span></span>

### <span data-ttu-id="fa727-149">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa727-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="fa727-150">System. String</span><span class="sxs-lookup"><span data-stu-id="fa727-150">System.String</span></span>

## <span data-ttu-id="fa727-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa727-151">OUTPUTS</span></span>

### <span data-ttu-id="fa727-152">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="fa727-152">System.Object</span></span>
## <span data-ttu-id="fa727-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa727-153">NOTES</span></span>

## <span data-ttu-id="fa727-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa727-154">RELATED LINKS</span></span>