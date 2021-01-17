---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359812"
---
# <span data-ttu-id="6564c-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="6564c-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="6564c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6564c-102">SYNOPSIS</span></span>
<span data-ttu-id="6564c-103">A replikációs kapcsolat eltávolítása/törlése a célköteten, és kiadás küldése a forrás replikációs szolgáltatásnak</span><span class="sxs-lookup"><span data-stu-id="6564c-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="6564c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6564c-104">SYNTAX</span></span>

### <span data-ttu-id="6564c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6564c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6564c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6564c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6564c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6564c-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6564c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6564c-108">DESCRIPTION</span></span>
<span data-ttu-id="6564c-109">A replikációs kapcsolat eltávolítása/törlése a célköteten, és kiadás küldése a forrás replikációs szolgáltatásnak</span><span class="sxs-lookup"><span data-stu-id="6564c-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="6564c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6564c-110">EXAMPLES</span></span>

### <span data-ttu-id="6564c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6564c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="6564c-112">Ez a parancs eltávolítja az ANF-replikációs kapcsolatot a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="6564c-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="6564c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6564c-113">PARAMETERS</span></span>

### <span data-ttu-id="6564c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6564c-114">-AccountName</span></span>
<span data-ttu-id="6564c-115">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="6564c-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="6564c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6564c-116">-DefaultProfile</span></span>
<span data-ttu-id="6564c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6564c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6564c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6564c-118">-InputObject</span></span>
<span data-ttu-id="6564c-119">Az ANF-célkötet eltávolítása a replikációval</span><span class="sxs-lookup"><span data-stu-id="6564c-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="6564c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6564c-120">-Name</span></span>
<span data-ttu-id="6564c-121">Az ANF-replikációs célkötet neve</span><span class="sxs-lookup"><span data-stu-id="6564c-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6564c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6564c-122">-PassThru</span></span>
<span data-ttu-id="6564c-123">Annak visszaadása, hogy a megadott ANF-replikáció sikeresen el lett-e távolítva</span><span class="sxs-lookup"><span data-stu-id="6564c-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="6564c-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6564c-124">-PoolName</span></span>
<span data-ttu-id="6564c-125">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="6564c-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="6564c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6564c-126">-ResourceGroupName</span></span>
<span data-ttu-id="6564c-127">Az ANF-replikációs célkötet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="6564c-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6564c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6564c-128">-ResourceId</span></span>
<span data-ttu-id="6564c-129">Az ANF-replikációs célkötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6564c-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6564c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6564c-130">-Confirm</span></span>
<span data-ttu-id="6564c-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6564c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6564c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6564c-132">-WhatIf</span></span>
<span data-ttu-id="6564c-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6564c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6564c-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6564c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6564c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6564c-135">CommonParameters</span></span>
<span data-ttu-id="6564c-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6564c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6564c-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6564c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6564c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6564c-138">INPUTS</span></span>

### <span data-ttu-id="6564c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6564c-139">System.String</span></span>

### <span data-ttu-id="6564c-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6564c-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6564c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6564c-141">OUTPUTS</span></span>

### <span data-ttu-id="6564c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6564c-142">System.Boolean</span></span>

## <span data-ttu-id="6564c-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6564c-143">NOTES</span></span>

## <span data-ttu-id="6564c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6564c-144">RELATED LINKS</span></span>
