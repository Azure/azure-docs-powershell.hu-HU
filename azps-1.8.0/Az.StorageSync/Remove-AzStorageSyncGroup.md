---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: f7c1f129d9a5f6f6bdd117597a2943567fb4001d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668481"
---
# <span data-ttu-id="6e293-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6e293-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="6e293-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e293-102">SYNOPSIS</span></span>
<span data-ttu-id="6e293-103">Ezzel a paranccsal törlődik a megadott szinkronizálási csoport.</span><span class="sxs-lookup"><span data-stu-id="6e293-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="6e293-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e293-104">SYNTAX</span></span>

### <span data-ttu-id="6e293-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e293-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e293-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e293-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e293-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e293-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e293-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e293-108">DESCRIPTION</span></span>
<span data-ttu-id="6e293-109">Ezzel a paranccsal törlődik a megadott szinkronizálási csoport.</span><span class="sxs-lookup"><span data-stu-id="6e293-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="6e293-110">A szinkronizálási csoportokat csak akkor lehet eltávolítani, ha az összes megadott végpont törlődik először.</span><span class="sxs-lookup"><span data-stu-id="6e293-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="6e293-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6e293-111">EXAMPLES</span></span>

### <span data-ttu-id="6e293-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6e293-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="6e293-113">Ezzel a paranccsal törlődik a szinkronizálás csoport.</span><span class="sxs-lookup"><span data-stu-id="6e293-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="6e293-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e293-114">PARAMETERS</span></span>

### <span data-ttu-id="6e293-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e293-115">-AsJob</span></span>
<span data-ttu-id="6e293-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6e293-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e293-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e293-117">-DefaultProfile</span></span>
<span data-ttu-id="6e293-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e293-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e293-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6e293-119">-Force</span></span>
<span data-ttu-id="6e293-120">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="6e293-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="6e293-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e293-121">-InputObject</span></span>
<span data-ttu-id="6e293-122">SyncGroup beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="6e293-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="6e293-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e293-123">-Name</span></span>
<span data-ttu-id="6e293-124">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="6e293-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="6e293-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e293-125">-PassThru</span></span>
<span data-ttu-id="6e293-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6e293-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6e293-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e293-127">-ResourceGroupName</span></span>
<span data-ttu-id="6e293-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6e293-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="6e293-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e293-129">-ResourceId</span></span>
<span data-ttu-id="6e293-130">SyncGroup erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="6e293-130">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="6e293-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6e293-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="6e293-132">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="6e293-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6e293-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e293-133">-Confirm</span></span>
<span data-ttu-id="6e293-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e293-134">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e293-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e293-135">-WhatIf</span></span>
<span data-ttu-id="6e293-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e293-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e293-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e293-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e293-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e293-138">CommonParameters</span></span>
<span data-ttu-id="6e293-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e293-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e293-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e293-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e293-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e293-141">INPUTS</span></span>

### <span data-ttu-id="6e293-142">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6e293-142">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="6e293-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6e293-143">System.String</span></span>

### <span data-ttu-id="6e293-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6e293-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6e293-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e293-145">OUTPUTS</span></span>

### <span data-ttu-id="6e293-146">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="6e293-146">System.Object</span></span>
## <span data-ttu-id="6e293-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e293-147">NOTES</span></span>

## <span data-ttu-id="6e293-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e293-148">RELATED LINKS</span></span>
