---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147203"
---
# <span data-ttu-id="d1267-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="d1267-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="d1267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1267-102">SYNOPSIS</span></span>
<span data-ttu-id="d1267-103">A replikációs kapcsolat eltávolítása/törlése a célköteten, és kiadás küldése a forrás replikációs szolgáltatásnak</span><span class="sxs-lookup"><span data-stu-id="d1267-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="d1267-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d1267-104">SYNTAX</span></span>

### <span data-ttu-id="d1267-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1267-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1267-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1267-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1267-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1267-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1267-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d1267-108">DESCRIPTION</span></span>
<span data-ttu-id="d1267-109">A replikációs kapcsolat eltávolítása/törlése a célköteten, és kiadás küldése a forrás replikációs szolgáltatásnak</span><span class="sxs-lookup"><span data-stu-id="d1267-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="d1267-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d1267-110">EXAMPLES</span></span>

### <span data-ttu-id="d1267-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d1267-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="d1267-112">Ez a parancs eltávolítja az ANF-replikációs kapcsolatot a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="d1267-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="d1267-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1267-113">PARAMETERS</span></span>

### <span data-ttu-id="d1267-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d1267-114">-AccountName</span></span>
<span data-ttu-id="d1267-115">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="d1267-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="d1267-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1267-116">-DefaultProfile</span></span>
<span data-ttu-id="d1267-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1267-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1267-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1267-118">-InputObject</span></span>
<span data-ttu-id="d1267-119">Az ANF-célkötet az eltávolítható replikációval</span><span class="sxs-lookup"><span data-stu-id="d1267-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="d1267-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d1267-120">-Name</span></span>
<span data-ttu-id="d1267-121">Az ANF-replikációs célkötet neve</span><span class="sxs-lookup"><span data-stu-id="d1267-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="d1267-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1267-122">-PassThru</span></span>
<span data-ttu-id="d1267-123">Annak visszaadása, hogy a megadott ANF-replikáció sikeresen el lett-e távolítva</span><span class="sxs-lookup"><span data-stu-id="d1267-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="d1267-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d1267-124">-PoolName</span></span>
<span data-ttu-id="d1267-125">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="d1267-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="d1267-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1267-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1267-127">Az ANF-replikációs célkötet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="d1267-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="d1267-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1267-128">-ResourceId</span></span>
<span data-ttu-id="d1267-129">Az ANF-replikációs célkötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d1267-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="d1267-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1267-130">-Confirm</span></span>
<span data-ttu-id="d1267-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d1267-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1267-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1267-132">-WhatIf</span></span>
<span data-ttu-id="d1267-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d1267-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1267-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1267-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1267-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1267-135">CommonParameters</span></span>
<span data-ttu-id="d1267-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1267-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1267-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1267-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1267-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1267-138">INPUTS</span></span>

### <span data-ttu-id="d1267-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d1267-139">System.String</span></span>

### <span data-ttu-id="d1267-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d1267-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d1267-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1267-141">OUTPUTS</span></span>

### <span data-ttu-id="d1267-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1267-142">System.Boolean</span></span>

## <span data-ttu-id="d1267-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d1267-143">NOTES</span></span>

## <span data-ttu-id="d1267-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1267-144">RELATED LINKS</span></span>
