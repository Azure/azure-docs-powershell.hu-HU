---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: b2c6d074f51f1ef2aa26e9d0c75fe6338a094419
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839884"
---
# <span data-ttu-id="5669a-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5669a-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="5669a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5669a-102">SYNOPSIS</span></span>
<span data-ttu-id="5669a-103">Ezzel a paranccsal törlődik a megadott szinkronizálási csoport.</span><span class="sxs-lookup"><span data-stu-id="5669a-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="5669a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5669a-104">SYNTAX</span></span>

### <span data-ttu-id="5669a-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5669a-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5669a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5669a-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5669a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5669a-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5669a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5669a-108">DESCRIPTION</span></span>
<span data-ttu-id="5669a-109">Ezzel a paranccsal törlődik a megadott szinkronizálási csoport.</span><span class="sxs-lookup"><span data-stu-id="5669a-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="5669a-110">A szinkronizálási csoportokat csak akkor lehet eltávolítani, ha az összes megadott végpont törlődik először.</span><span class="sxs-lookup"><span data-stu-id="5669a-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="5669a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5669a-111">EXAMPLES</span></span>

### <span data-ttu-id="5669a-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5669a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="5669a-113">Ezzel a paranccsal törlődik a szinkronizálás csoport.</span><span class="sxs-lookup"><span data-stu-id="5669a-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="5669a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5669a-114">PARAMETERS</span></span>

### <span data-ttu-id="5669a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5669a-115">-AsJob</span></span>
<span data-ttu-id="5669a-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5669a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5669a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5669a-117">-DefaultProfile</span></span>
<span data-ttu-id="5669a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5669a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5669a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5669a-119">-Force</span></span>
<span data-ttu-id="5669a-120">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="5669a-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="5669a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5669a-121">-InputObject</span></span>
<span data-ttu-id="5669a-122">SyncGroup beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="5669a-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="5669a-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5669a-123">-Name</span></span>
<span data-ttu-id="5669a-124">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="5669a-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="5669a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5669a-125">-PassThru</span></span>
<span data-ttu-id="5669a-126">A normál végrehajtásban ez a parancsmag nem ad értéket a sikernek.</span><span class="sxs-lookup"><span data-stu-id="5669a-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="5669a-127">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után a csővezetéknek ad értéket.</span><span class="sxs-lookup"><span data-stu-id="5669a-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="5669a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5669a-128">-ResourceGroupName</span></span>
<span data-ttu-id="5669a-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5669a-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="5669a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5669a-130">-ResourceId</span></span>
<span data-ttu-id="5669a-131">SyncGroup erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="5669a-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="5669a-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="5669a-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="5669a-133">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="5669a-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="5669a-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5669a-134">-Confirm</span></span>
<span data-ttu-id="5669a-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5669a-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5669a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5669a-136">-WhatIf</span></span>
<span data-ttu-id="5669a-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5669a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5669a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5669a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5669a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5669a-139">CommonParameters</span></span>
<span data-ttu-id="5669a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5669a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5669a-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5669a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5669a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5669a-142">INPUTS</span></span>

### <span data-ttu-id="5669a-143">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5669a-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="5669a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5669a-144">System.String</span></span>

### <span data-ttu-id="5669a-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5669a-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5669a-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5669a-146">OUTPUTS</span></span>

### <span data-ttu-id="5669a-147">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5669a-147">System.Object</span></span>
## <span data-ttu-id="5669a-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5669a-148">NOTES</span></span>

## <span data-ttu-id="5669a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5669a-149">RELATED LINKS</span></span>
