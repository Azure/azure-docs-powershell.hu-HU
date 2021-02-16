---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153651"
---
# <span data-ttu-id="80ae0-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="80ae0-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="80ae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="80ae0-103">Azure által felügyelt alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="80ae0-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="80ae0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80ae0-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80ae0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80ae0-105">DESCRIPTION</span></span>
<span data-ttu-id="80ae0-106">A **New-AzManagedApplication** parancsmag létrehoz egy Azure Felügyelt alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="80ae0-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="80ae0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80ae0-107">EXAMPLES</span></span>

### <span data-ttu-id="80ae0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="80ae0-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="80ae0-109">Ez a parancs felügyelt alkalmazást hoz létre</span><span class="sxs-lookup"><span data-stu-id="80ae0-109">This command creates a managed application</span></span>

## <span data-ttu-id="80ae0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80ae0-110">PARAMETERS</span></span>

### <span data-ttu-id="80ae0-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="80ae0-111">-ApiVersion</span></span>
<span data-ttu-id="80ae0-112">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="80ae0-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="80ae0-113">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="80ae0-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="80ae0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ae0-114">-DefaultProfile</span></span>
<span data-ttu-id="80ae0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80ae0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80ae0-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="80ae0-116">-Kind</span></span>
<span data-ttu-id="80ae0-117">A felügyelt alkalmazás fajtája.</span><span class="sxs-lookup"><span data-stu-id="80ae0-117">The managed application kind.</span></span>
<span data-ttu-id="80ae0-118">Piactér vagy servicecatalog</span><span class="sxs-lookup"><span data-stu-id="80ae0-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ae0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="80ae0-119">-Location</span></span>
<span data-ttu-id="80ae0-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="80ae0-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ae0-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="80ae0-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="80ae0-122">A felügyelt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="80ae0-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="80ae0-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ae0-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="80ae0-124">A felügyelt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="80ae0-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ae0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="80ae0-125">-Name</span></span>
<span data-ttu-id="80ae0-126">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="80ae0-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ae0-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="80ae0-127">-Parameter</span></span>
<span data-ttu-id="80ae0-128">A felügyelt alkalmazás JSON formátumú paramétereinek karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="80ae0-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="80ae0-129">Ez lehet egy olyan fájlnév vagy uri elérési útja, amely tartalmazza a paramétereket, vagy karakterláncként a paramétereket.</span><span class="sxs-lookup"><span data-stu-id="80ae0-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="80ae0-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="80ae0-130">-Plan</span></span>
<span data-ttu-id="80ae0-131">A felügyelt alkalmazásterv tulajdonságait képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="80ae0-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="80ae0-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="80ae0-132">-Pre</span></span>
<span data-ttu-id="80ae0-133">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="80ae0-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="80ae0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ae0-134">-ResourceGroupName</span></span>
<span data-ttu-id="80ae0-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="80ae0-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ae0-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="80ae0-136">-Tag</span></span>
<span data-ttu-id="80ae0-137">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="80ae0-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="80ae0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80ae0-138">-Confirm</span></span>
<span data-ttu-id="80ae0-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="80ae0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80ae0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80ae0-140">-WhatIf</span></span>
<span data-ttu-id="80ae0-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="80ae0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80ae0-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="80ae0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80ae0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ae0-143">CommonParameters</span></span>
<span data-ttu-id="80ae0-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80ae0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ae0-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80ae0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ae0-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80ae0-146">INPUTS</span></span>

### <span data-ttu-id="80ae0-147">System.String</span><span class="sxs-lookup"><span data-stu-id="80ae0-147">System.String</span></span>

### <span data-ttu-id="80ae0-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="80ae0-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="80ae0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80ae0-149">OUTPUTS</span></span>

### <span data-ttu-id="80ae0-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="80ae0-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="80ae0-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80ae0-151">NOTES</span></span>

## <span data-ttu-id="80ae0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80ae0-152">RELATED LINKS</span></span>
