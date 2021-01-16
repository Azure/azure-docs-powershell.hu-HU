---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354341"
---
# <span data-ttu-id="2deca-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="2deca-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="2deca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2deca-102">SYNOPSIS</span></span>
<span data-ttu-id="2deca-103">A kapcsolat folytatása/újraszinkronizációja a célköteten.</span><span class="sxs-lookup"><span data-stu-id="2deca-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="2deca-104">Ha a műveletet a forrásköteten futtatja, a művelet megfordítja a kapcsolatot, és a forrásból a célhelyre szinkronizálja.</span><span class="sxs-lookup"><span data-stu-id="2deca-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="2deca-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2deca-105">SYNTAX</span></span>

### <span data-ttu-id="2deca-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2deca-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2deca-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2deca-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2deca-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2deca-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2deca-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2deca-109">DESCRIPTION</span></span>
<span data-ttu-id="2deca-110">A kapcsolat folytatása/újraszinkronizációja a célköteten</span><span class="sxs-lookup"><span data-stu-id="2deca-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="2deca-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2deca-111">EXAMPLES</span></span>

### <span data-ttu-id="2deca-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="2deca-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="2deca-113">Ez a parancs folytatja az ANF-replikációs kapcsolatot a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="2deca-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="2deca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2deca-114">PARAMETERS</span></span>

### <span data-ttu-id="2deca-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2deca-115">-AccountName</span></span>
<span data-ttu-id="2deca-116">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="2deca-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="2deca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2deca-117">-DefaultProfile</span></span>
<span data-ttu-id="2deca-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2deca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2deca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2deca-119">-InputObject</span></span>
<span data-ttu-id="2deca-120">Az anf replikációs célkötetobjektum újraszinkronizációja</span><span class="sxs-lookup"><span data-stu-id="2deca-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="2deca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2deca-121">-Name</span></span>
<span data-ttu-id="2deca-122">Az ANF-replikációs célkötet neve</span><span class="sxs-lookup"><span data-stu-id="2deca-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2deca-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2deca-123">-PassThru</span></span>
<span data-ttu-id="2deca-124">Visszaadja, hogy a megadott replikációs kötet újraszinkronizációja történt-e</span><span class="sxs-lookup"><span data-stu-id="2deca-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="2deca-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2deca-125">-PoolName</span></span>
<span data-ttu-id="2deca-126">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="2deca-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="2deca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2deca-127">-ResourceGroupName</span></span>
<span data-ttu-id="2deca-128">Az ANF-replikációs célkötet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="2deca-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2deca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2deca-129">-ResourceId</span></span>
<span data-ttu-id="2deca-130">Az ANF-replikációs célkötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2deca-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2deca-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2deca-131">-Confirm</span></span>
<span data-ttu-id="2deca-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2deca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2deca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2deca-133">-WhatIf</span></span>
<span data-ttu-id="2deca-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2deca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2deca-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2deca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2deca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2deca-136">CommonParameters</span></span>
<span data-ttu-id="2deca-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2deca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2deca-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2deca-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2deca-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2deca-139">INPUTS</span></span>

### <span data-ttu-id="2deca-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2deca-140">System.String</span></span>

### <span data-ttu-id="2deca-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2deca-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2deca-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2deca-142">OUTPUTS</span></span>

### <span data-ttu-id="2deca-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2deca-143">System.Boolean</span></span>

## <span data-ttu-id="2deca-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2deca-144">NOTES</span></span>

## <span data-ttu-id="2deca-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2deca-145">RELATED LINKS</span></span>
