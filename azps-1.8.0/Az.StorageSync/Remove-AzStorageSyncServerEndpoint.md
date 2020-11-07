---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 328fd4c798380202b355974cc8d9150e1d138da5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668483"
---
# <span data-ttu-id="41b1b-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="41b1b-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="41b1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="41b1b-103">Ez a parancs törli a megadott kiszolgálói végpontot.</span><span class="sxs-lookup"><span data-stu-id="41b1b-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="41b1b-104">A szinkronizálás erre a helyre beállítás azonnal megszűnik.</span><span class="sxs-lookup"><span data-stu-id="41b1b-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="41b1b-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41b1b-105">SYNTAX</span></span>

### <span data-ttu-id="41b1b-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41b1b-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41b1b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41b1b-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41b1b-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41b1b-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41b1b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="41b1b-109">DESCRIPTION</span></span>
<span data-ttu-id="41b1b-110">A kiszolgáló végpontjának eltávolítása romboló művelet.</span><span class="sxs-lookup"><span data-stu-id="41b1b-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="41b1b-111">Ez a kiszolgálói hely megszünteti a szinkronizálást.</span><span class="sxs-lookup"><span data-stu-id="41b1b-111">This server location will stop syncing.</span></span> <span data-ttu-id="41b1b-112">Ezt a műveletet nem kell végrehajtani a szinkronizálási problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="41b1b-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="41b1b-113">Ha ez a kiszolgáló-hely (beleértve a fájlokat is) ismét hozzáadódik ugyanahhoz a szinkronizálási csoporthoz, mint a kiszolgáló végpontja, akkor az ütközési fájlok és más nem szándékolt következmények eléréséhez vezethet.</span><span class="sxs-lookup"><span data-stu-id="41b1b-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="41b1b-114">Ez a parancs csak a leszerelésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="41b1b-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="41b1b-115">Példák</span><span class="sxs-lookup"><span data-stu-id="41b1b-115">EXAMPLES</span></span>

### <span data-ttu-id="41b1b-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="41b1b-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="41b1b-117">Ez a parancs eltávolítja a kiszolgáló végpontját.</span><span class="sxs-lookup"><span data-stu-id="41b1b-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="41b1b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41b1b-118">PARAMETERS</span></span>

### <span data-ttu-id="41b1b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41b1b-119">-AsJob</span></span>
<span data-ttu-id="41b1b-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="41b1b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41b1b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b1b-121">-DefaultProfile</span></span>
<span data-ttu-id="41b1b-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41b1b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41b1b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="41b1b-123">-Force</span></span>
<span data-ttu-id="41b1b-124">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="41b1b-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="41b1b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41b1b-125">-InputObject</span></span>
<span data-ttu-id="41b1b-126">A ServerEndpoint bemeneti objektuma, normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="41b1b-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="41b1b-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41b1b-127">-Name</span></span>
<span data-ttu-id="41b1b-128">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="41b1b-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="41b1b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41b1b-129">-PassThru</span></span>
<span data-ttu-id="41b1b-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="41b1b-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="41b1b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b1b-131">-ResourceGroupName</span></span>
<span data-ttu-id="41b1b-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="41b1b-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="41b1b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41b1b-133">-ResourceId</span></span>
<span data-ttu-id="41b1b-134">ServerEndpoint erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="41b1b-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="41b1b-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="41b1b-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="41b1b-136">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="41b1b-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="41b1b-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="41b1b-137">-SyncGroupName</span></span>
<span data-ttu-id="41b1b-138">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="41b1b-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="41b1b-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41b1b-139">-Confirm</span></span>
<span data-ttu-id="41b1b-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41b1b-140">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41b1b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b1b-141">-WhatIf</span></span>
<span data-ttu-id="41b1b-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41b1b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41b1b-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41b1b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41b1b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b1b-144">CommonParameters</span></span>
<span data-ttu-id="41b1b-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41b1b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b1b-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b1b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b1b-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41b1b-147">INPUTS</span></span>

### <span data-ttu-id="41b1b-148">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="41b1b-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="41b1b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="41b1b-149">System.String</span></span>

## <span data-ttu-id="41b1b-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41b1b-150">OUTPUTS</span></span>

### <span data-ttu-id="41b1b-151">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="41b1b-151">System.Object</span></span>
## <span data-ttu-id="41b1b-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41b1b-152">NOTES</span></span>

## <span data-ttu-id="41b1b-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41b1b-153">RELATED LINKS</span></span>
