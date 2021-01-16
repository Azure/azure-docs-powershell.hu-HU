---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380503"
---
# <span data-ttu-id="9b513-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="9b513-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="9b513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b513-102">SYNOPSIS</span></span>
<span data-ttu-id="9b513-103">A replikációs kapcsolat felfüggesztése/megszakadása a célköteten</span><span class="sxs-lookup"><span data-stu-id="9b513-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="9b513-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b513-104">SYNTAX</span></span>

### <span data-ttu-id="9b513-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b513-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b513-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b513-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b513-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b513-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b513-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b513-108">DESCRIPTION</span></span>
<span data-ttu-id="9b513-109">A replikációs kapcsolat felfüggesztése/megszakadása a célköteten</span><span class="sxs-lookup"><span data-stu-id="9b513-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="9b513-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b513-110">EXAMPLES</span></span>

### <span data-ttu-id="9b513-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9b513-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="9b513-112">Ez a parancs felfüggeszti az ANF-replikációs kapcsolatot a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="9b513-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="9b513-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b513-113">PARAMETERS</span></span>

### <span data-ttu-id="9b513-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9b513-114">-AccountName</span></span>
<span data-ttu-id="9b513-115">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="9b513-115">The name of the ANF account of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b513-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b513-116">-DefaultProfile</span></span>
<span data-ttu-id="9b513-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b513-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b513-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="9b513-118">-ForceBreak</span></span>
<span data-ttu-id="9b513-119">Ha a replikáció állapota átvitele közben meg szeretné szakítani a replikációt, állítsa igazra.</span><span class="sxs-lookup"><span data-stu-id="9b513-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b513-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b513-120">-InputObject</span></span>
<span data-ttu-id="9b513-121">AnF-célkötet-objektum a tördendő replikációval</span><span class="sxs-lookup"><span data-stu-id="9b513-121">The ANF destination volume object with the replication to break</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b513-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9b513-122">-Name</span></span>
<span data-ttu-id="9b513-123">Az ANF-replikációs célkötet neve</span><span class="sxs-lookup"><span data-stu-id="9b513-123">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b513-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b513-124">-PassThru</span></span>
<span data-ttu-id="9b513-125">Annak visszaadása, hogy történt-e a megadott mennyiségi replikációs törés</span><span class="sxs-lookup"><span data-stu-id="9b513-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="9b513-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9b513-126">-PoolName</span></span>
<span data-ttu-id="9b513-127">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="9b513-127">The name of the ANF pool of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b513-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b513-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b513-129">Az ANF-replikációs célkötet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="9b513-129">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b513-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b513-130">-ResourceId</span></span>
<span data-ttu-id="9b513-131">Az ANF-replikációs célkötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9b513-131">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b513-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b513-132">-Confirm</span></span>
<span data-ttu-id="9b513-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9b513-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b513-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b513-134">-WhatIf</span></span>
<span data-ttu-id="9b513-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9b513-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b513-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b513-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b513-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b513-137">CommonParameters</span></span>
<span data-ttu-id="9b513-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b513-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b513-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b513-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b513-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b513-140">INPUTS</span></span>

### <span data-ttu-id="9b513-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9b513-141">System.String</span></span>

### <span data-ttu-id="9b513-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9b513-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9b513-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b513-143">OUTPUTS</span></span>

### <span data-ttu-id="9b513-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b513-144">System.Boolean</span></span>

## <span data-ttu-id="9b513-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b513-145">NOTES</span></span>

## <span data-ttu-id="9b513-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b513-146">RELATED LINKS</span></span>
