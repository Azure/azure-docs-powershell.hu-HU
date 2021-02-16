---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153562"
---
# <span data-ttu-id="9d652-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="9d652-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="9d652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d652-102">SYNOPSIS</span></span>
<span data-ttu-id="9d652-103">Felügyelt alkalmazás frissítései</span><span class="sxs-lookup"><span data-stu-id="9d652-103">Updates managed application</span></span>

## <span data-ttu-id="9d652-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9d652-104">SYNTAX</span></span>

### <span data-ttu-id="9d652-105">SetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d652-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d652-106">SetById</span><span class="sxs-lookup"><span data-stu-id="9d652-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d652-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9d652-107">DESCRIPTION</span></span>
<span data-ttu-id="9d652-108">A **Set-AzManagedApplication** parancsmag frissíti a felügyelt alkalmazásokat</span><span class="sxs-lookup"><span data-stu-id="9d652-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="9d652-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9d652-109">EXAMPLES</span></span>

### <span data-ttu-id="9d652-110">1. példa: Felügyelt alkalmazásdefiníció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="9d652-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="9d652-111">Ez a parancs frissíti a felügyelt alkalmazás leírását</span><span class="sxs-lookup"><span data-stu-id="9d652-111">This command updates the managed application description</span></span>

## <span data-ttu-id="9d652-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d652-112">PARAMETERS</span></span>

### <span data-ttu-id="9d652-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9d652-113">-ApiVersion</span></span>
<span data-ttu-id="9d652-114">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="9d652-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9d652-115">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="9d652-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d652-116">-DefaultProfile</span></span>
<span data-ttu-id="9d652-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d652-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d652-118">-Id</span><span class="sxs-lookup"><span data-stu-id="9d652-118">-Id</span></span>
<span data-ttu-id="9d652-119">A teljesen minősített felügyelt alkalmazásazonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="9d652-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="9d652-120">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d652-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="9d652-121">-Kind</span></span>
<span data-ttu-id="9d652-122">A felügyelt alkalmazás fajtája.</span><span class="sxs-lookup"><span data-stu-id="9d652-122">The managed application kind.</span></span>
<span data-ttu-id="9d652-123">Piactér vagy szolgáltatáscatalog</span><span class="sxs-lookup"><span data-stu-id="9d652-123">One of marketplace or servicecatalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="9d652-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="9d652-125">A felügyelt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d652-125">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d652-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="9d652-127">A felügyelt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d652-127">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9d652-128">-Name</span></span>
<span data-ttu-id="9d652-129">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="9d652-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9d652-130">-Parameter</span></span>
<span data-ttu-id="9d652-131">A felügyelt alkalmazás JSON formátumú paramétereinek karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="9d652-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="9d652-132">Ez lehet egy olyan fájlnév vagy uri elérési útja, amely tartalmazza a paramétereket, vagy karakterláncként a paramétereket.</span><span class="sxs-lookup"><span data-stu-id="9d652-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="9d652-133">-Plan</span></span>
<span data-ttu-id="9d652-134">A felügyelt alkalmazásterv tulajdonságait képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="9d652-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="9d652-135">-Pre</span></span>
<span data-ttu-id="9d652-136">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="9d652-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9d652-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d652-137">-ResourceGroupName</span></span>
<span data-ttu-id="9d652-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d652-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="9d652-139">-Tag</span></span>
<span data-ttu-id="9d652-140">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="9d652-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d652-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d652-141">-Confirm</span></span>
<span data-ttu-id="9d652-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9d652-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d652-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d652-143">-WhatIf</span></span>
<span data-ttu-id="9d652-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9d652-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d652-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d652-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d652-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d652-146">CommonParameters</span></span>
<span data-ttu-id="9d652-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d652-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d652-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d652-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d652-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d652-149">INPUTS</span></span>

### <span data-ttu-id="9d652-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9d652-150">System.String</span></span>

### <span data-ttu-id="9d652-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9d652-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9d652-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d652-152">OUTPUTS</span></span>

### <span data-ttu-id="9d652-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="9d652-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9d652-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9d652-154">NOTES</span></span>

## <span data-ttu-id="9d652-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d652-155">RELATED LINKS</span></span>
