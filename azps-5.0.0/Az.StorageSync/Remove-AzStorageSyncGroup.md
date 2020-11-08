---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186002"
---
# <span data-ttu-id="fd7e3-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fd7e3-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="fd7e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7e3-103">Ezzel a paranccsal törlődik a megadott szinkronizálási csoport.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="fd7e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd7e3-104">SYNTAX</span></span>

### <span data-ttu-id="fd7e3-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd7e3-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd7e3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd7e3-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7e3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd7e3-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd7e3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd7e3-108">DESCRIPTION</span></span>
<span data-ttu-id="fd7e3-109">Ezzel a paranccsal törlődik a megadott szinkronizálási csoport.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="fd7e3-110">A szinkronizálási csoportokat csak akkor lehet eltávolítani, ha az összes megadott végpont törlődik először.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="fd7e3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fd7e3-111">EXAMPLES</span></span>

### <span data-ttu-id="fd7e3-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fd7e3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="fd7e3-113">Ezzel a paranccsal törlődik a szinkronizálás csoport.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="fd7e3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd7e3-114">PARAMETERS</span></span>

### <span data-ttu-id="fd7e3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd7e3-115">-AsJob</span></span>
<span data-ttu-id="fd7e3-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fd7e3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd7e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7e3-117">-DefaultProfile</span></span>
<span data-ttu-id="fd7e3-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd7e3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fd7e3-119">-Force</span></span>
<span data-ttu-id="fd7e3-120">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd7e3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd7e3-121">-InputObject</span></span>
<span data-ttu-id="fd7e3-122">SyncGroup beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="fd7e3-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd7e3-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd7e3-123">-Name</span></span>
<span data-ttu-id="fd7e3-124">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd7e3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd7e3-125">-PassThru</span></span>
<span data-ttu-id="fd7e3-126">A normál végrehajtásban ez a parancsmag nem ad értéket a sikernek.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="fd7e3-127">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után a csővezetéknek ad értéket.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="fd7e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="fd7e3-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="fd7e3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd7e3-130">-ResourceId</span></span>
<span data-ttu-id="fd7e3-131">SyncGroup erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="fd7e3-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="fd7e3-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="fd7e3-133">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="fd7e3-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd7e3-134">-Confirm</span></span>
<span data-ttu-id="fd7e3-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7e3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7e3-136">-WhatIf</span></span>
<span data-ttu-id="fd7e3-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd7e3-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd7e3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7e3-139">CommonParameters</span></span>
<span data-ttu-id="fd7e3-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd7e3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7e3-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7e3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7e3-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd7e3-142">INPUTS</span></span>

### <span data-ttu-id="fd7e3-143">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fd7e3-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="fd7e3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fd7e3-144">System.String</span></span>

### <span data-ttu-id="fd7e3-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fd7e3-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fd7e3-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd7e3-146">OUTPUTS</span></span>

### <span data-ttu-id="fd7e3-147">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="fd7e3-147">System.Object</span></span>
## <span data-ttu-id="fd7e3-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd7e3-148">NOTES</span></span>

## <span data-ttu-id="fd7e3-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd7e3-149">RELATED LINKS</span></span>
