---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207070"
---
# <span data-ttu-id="a8ac9-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="a8ac9-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="a8ac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ac9-103">A kapcsolat folytatása/újraszinkronizációja a célköteten.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="a8ac9-104">Ha a műveletet a forrásköteten futtatja, a művelet megfordítja a kapcsolatot, és a forrásból a célhelyre szinkronizálja.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="a8ac9-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8ac9-105">SYNTAX</span></span>

### <span data-ttu-id="a8ac9-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8ac9-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8ac9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8ac9-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ac9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8ac9-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ac9-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8ac9-109">DESCRIPTION</span></span>
<span data-ttu-id="a8ac9-110">A kapcsolat folytatása/újraszinkronizációja a célköteten</span><span class="sxs-lookup"><span data-stu-id="a8ac9-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="a8ac9-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8ac9-111">EXAMPLES</span></span>

### <span data-ttu-id="a8ac9-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="a8ac9-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="a8ac9-113">Ez a parancs folytatja az ANF-replikációs kapcsolatot a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="a8ac9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8ac9-114">PARAMETERS</span></span>

### <span data-ttu-id="a8ac9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a8ac9-115">-AccountName</span></span>
<span data-ttu-id="a8ac9-116">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="a8ac9-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="a8ac9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ac9-117">-DefaultProfile</span></span>
<span data-ttu-id="a8ac9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ac9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ac9-119">-InputObject</span></span>
<span data-ttu-id="a8ac9-120">Az ANF-replikációs célkötetobjektum újraszinkronizációja</span><span class="sxs-lookup"><span data-stu-id="a8ac9-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="a8ac9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a8ac9-121">-Name</span></span>
<span data-ttu-id="a8ac9-122">Az ANF-replikációs célkötet neve</span><span class="sxs-lookup"><span data-stu-id="a8ac9-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a8ac9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8ac9-123">-PassThru</span></span>
<span data-ttu-id="a8ac9-124">Visszaadja, hogy a megadott replikációs kötet újraszinkronizációja történt-e</span><span class="sxs-lookup"><span data-stu-id="a8ac9-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="a8ac9-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a8ac9-125">-PoolName</span></span>
<span data-ttu-id="a8ac9-126">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="a8ac9-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="a8ac9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ac9-127">-ResourceGroupName</span></span>
<span data-ttu-id="a8ac9-128">Az ANF-replikációs célkötet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="a8ac9-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a8ac9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8ac9-129">-ResourceId</span></span>
<span data-ttu-id="a8ac9-130">Az ANF-replikációs célkötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a8ac9-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a8ac9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8ac9-131">-Confirm</span></span>
<span data-ttu-id="a8ac9-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ac9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ac9-133">-WhatIf</span></span>
<span data-ttu-id="a8ac9-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ac9-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ac9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ac9-136">CommonParameters</span></span>
<span data-ttu-id="a8ac9-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ac9-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8ac9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ac9-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8ac9-139">INPUTS</span></span>

### <span data-ttu-id="a8ac9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a8ac9-140">System.String</span></span>

### <span data-ttu-id="a8ac9-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a8ac9-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a8ac9-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8ac9-142">OUTPUTS</span></span>

### <span data-ttu-id="a8ac9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a8ac9-143">System.Boolean</span></span>

## <span data-ttu-id="a8ac9-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8ac9-144">NOTES</span></span>

## <span data-ttu-id="a8ac9-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8ac9-145">RELATED LINKS</span></span>
