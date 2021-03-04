---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f53ca76da23620a37020a14877059aae4f4c9808
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926746"
---
# <span data-ttu-id="55ce5-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="55ce5-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="55ce5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="55ce5-103">Törli az Azure NetApp-fájlok (ANF) kötetét.</span><span class="sxs-lookup"><span data-stu-id="55ce5-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="55ce5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55ce5-104">SYNTAX</span></span>

### <span data-ttu-id="55ce5-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55ce5-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55ce5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55ce5-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55ce5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55ce5-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55ce5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55ce5-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55ce5-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55ce5-109">DESCRIPTION</span></span>
<span data-ttu-id="55ce5-110">A **Remove-AzNetAppFilesVolume** parancsmag törli az ANF-kötetet.</span><span class="sxs-lookup"><span data-stu-id="55ce5-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="55ce5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55ce5-111">EXAMPLES</span></span>

### <span data-ttu-id="55ce5-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="55ce5-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="55ce5-113">Ez a parancs törli a "MyAnfVolume" ANF-kötetet.</span><span class="sxs-lookup"><span data-stu-id="55ce5-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="55ce5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55ce5-114">PARAMETERS</span></span>

### <span data-ttu-id="55ce5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55ce5-115">-AccountName</span></span>
<span data-ttu-id="55ce5-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="55ce5-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="55ce5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ce5-117">-DefaultProfile</span></span>
<span data-ttu-id="55ce5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55ce5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55ce5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55ce5-119">-InputObject</span></span>
<span data-ttu-id="55ce5-120">Az eltávolítható kötetobjektum</span><span class="sxs-lookup"><span data-stu-id="55ce5-120">The volume object to remove</span></span>

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

### <span data-ttu-id="55ce5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="55ce5-121">-Name</span></span>
<span data-ttu-id="55ce5-122">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="55ce5-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ce5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55ce5-123">-PassThru</span></span>
<span data-ttu-id="55ce5-124">Visszaadja, hogy sikerült-e eltávolítani a megadott mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="55ce5-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="55ce5-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="55ce5-125">-PoolName</span></span>
<span data-ttu-id="55ce5-126">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="55ce5-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="55ce5-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="55ce5-127">-PoolObject</span></span>
<span data-ttu-id="55ce5-128">Az eltávolítható hangerőt tartalmazó készletobjektum</span><span class="sxs-lookup"><span data-stu-id="55ce5-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55ce5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ce5-129">-ResourceGroupName</span></span>
<span data-ttu-id="55ce5-130">Az ANF-mennyiség erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="55ce5-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="55ce5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55ce5-131">-ResourceId</span></span>
<span data-ttu-id="55ce5-132">Az ANF-mennyiség erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="55ce5-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="55ce5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55ce5-133">-Confirm</span></span>
<span data-ttu-id="55ce5-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="55ce5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55ce5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55ce5-135">-WhatIf</span></span>
<span data-ttu-id="55ce5-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="55ce5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55ce5-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55ce5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55ce5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ce5-138">CommonParameters</span></span>
<span data-ttu-id="55ce5-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55ce5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ce5-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55ce5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ce5-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55ce5-141">INPUTS</span></span>

### <span data-ttu-id="55ce5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="55ce5-142">System.String</span></span>

### <span data-ttu-id="55ce5-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="55ce5-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="55ce5-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="55ce5-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="55ce5-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55ce5-145">OUTPUTS</span></span>

### <span data-ttu-id="55ce5-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55ce5-146">System.Boolean</span></span>

## <span data-ttu-id="55ce5-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55ce5-147">NOTES</span></span>

## <span data-ttu-id="55ce5-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55ce5-148">RELATED LINKS</span></span>
