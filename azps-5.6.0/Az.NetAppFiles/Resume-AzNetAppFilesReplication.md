---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 5f5dac2f2028de9b90941ef91c38361c4357fc8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926730"
---
# <span data-ttu-id="b0b85-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="b0b85-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="b0b85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b85-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b85-103">A kapcsolat folytatása/újraszinkronizációja a célköteten.</span><span class="sxs-lookup"><span data-stu-id="b0b85-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="b0b85-104">Ha a műveletet a forrásköteten futtatja, a művelet megfordítja a kapcsolatot, és a forrásból a célhelyre szinkronizálja.</span><span class="sxs-lookup"><span data-stu-id="b0b85-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="b0b85-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0b85-105">SYNTAX</span></span>

### <span data-ttu-id="b0b85-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0b85-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0b85-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0b85-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b85-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0b85-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b85-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0b85-109">DESCRIPTION</span></span>
<span data-ttu-id="b0b85-110">A kapcsolat folytatása/újraszinkronizációja a célköteten</span><span class="sxs-lookup"><span data-stu-id="b0b85-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="b0b85-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0b85-111">EXAMPLES</span></span>

### <span data-ttu-id="b0b85-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="b0b85-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="b0b85-113">Ez a parancs folytatja az ANF-replikációs kapcsolatot a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="b0b85-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="b0b85-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b85-114">PARAMETERS</span></span>

### <span data-ttu-id="b0b85-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0b85-115">-AccountName</span></span>
<span data-ttu-id="b0b85-116">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="b0b85-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="b0b85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b85-117">-DefaultProfile</span></span>
<span data-ttu-id="b0b85-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0b85-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b85-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b85-119">-InputObject</span></span>
<span data-ttu-id="b0b85-120">Az anf replikációs célkötetobjektum újraszinkronizációja</span><span class="sxs-lookup"><span data-stu-id="b0b85-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="b0b85-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b85-121">-Name</span></span>
<span data-ttu-id="b0b85-122">Az ANF-replikációs célkötet neve</span><span class="sxs-lookup"><span data-stu-id="b0b85-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b0b85-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0b85-123">-PassThru</span></span>
<span data-ttu-id="b0b85-124">Visszaadja, hogy a megadott replikációs kötet újraszinkronizációja történt-e</span><span class="sxs-lookup"><span data-stu-id="b0b85-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="b0b85-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b0b85-125">-PoolName</span></span>
<span data-ttu-id="b0b85-126">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="b0b85-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="b0b85-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b85-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0b85-128">Az ANF-replikációs célkötet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="b0b85-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b0b85-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b85-129">-ResourceId</span></span>
<span data-ttu-id="b0b85-130">Az ANF-replikációs célkötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b0b85-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b0b85-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0b85-131">-Confirm</span></span>
<span data-ttu-id="b0b85-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b0b85-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b85-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b85-133">-WhatIf</span></span>
<span data-ttu-id="b0b85-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b0b85-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b85-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0b85-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b85-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b85-136">CommonParameters</span></span>
<span data-ttu-id="b0b85-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b85-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b85-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0b85-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b85-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b85-139">INPUTS</span></span>

### <span data-ttu-id="b0b85-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b0b85-140">System.String</span></span>

### <span data-ttu-id="b0b85-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b0b85-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b0b85-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0b85-142">OUTPUTS</span></span>

### <span data-ttu-id="b0b85-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0b85-143">System.Boolean</span></span>

## <span data-ttu-id="b0b85-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0b85-144">NOTES</span></span>

## <span data-ttu-id="b0b85-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0b85-145">RELATED LINKS</span></span>
