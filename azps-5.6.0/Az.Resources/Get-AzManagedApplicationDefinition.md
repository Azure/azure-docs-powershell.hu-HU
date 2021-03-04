---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: f1f71d188a6b25146103fe3fe5d91b8ba53eaaf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935522"
---
# <span data-ttu-id="beefb-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="beefb-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="beefb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beefb-102">SYNOPSIS</span></span>
<span data-ttu-id="beefb-103">Felügyelt alkalmazásdefiníciók lekérte</span><span class="sxs-lookup"><span data-stu-id="beefb-103">Gets managed application definitions</span></span>

## <span data-ttu-id="beefb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="beefb-104">SYNTAX</span></span>

### <span data-ttu-id="beefb-105">GetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="beefb-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="beefb-106">GetById</span><span class="sxs-lookup"><span data-stu-id="beefb-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beefb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="beefb-107">DESCRIPTION</span></span>
<span data-ttu-id="beefb-108">A **Get-AzManagedApplicationDefinition parancsmag** felügyelt alkalmazásdefiníciókat kap</span><span class="sxs-lookup"><span data-stu-id="beefb-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="beefb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="beefb-109">EXAMPLES</span></span>

### <span data-ttu-id="beefb-110">1. példa: Az összes felügyelt alkalmazásdefiníció lekérte egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="beefb-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="beefb-111">Ez a parancs a felügyelt alkalmazásdefiníciókat a "MyRG" erőforráscsoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="beefb-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="beefb-112">2. példa: Felügyelt alkalmazásdefiníció lekérte</span><span class="sxs-lookup"><span data-stu-id="beefb-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="beefb-113">Ez a parancs a "MyRG" erőforráscsoportban a "myManagedAppDef" felügyelt alkalmazásdefiníciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="beefb-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="beefb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="beefb-114">PARAMETERS</span></span>

### <span data-ttu-id="beefb-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="beefb-115">-ApiVersion</span></span>
<span data-ttu-id="beefb-116">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="beefb-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="beefb-117">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="beefb-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="beefb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beefb-118">-DefaultProfile</span></span>
<span data-ttu-id="beefb-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="beefb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beefb-120">-Id</span><span class="sxs-lookup"><span data-stu-id="beefb-120">-Id</span></span>
<span data-ttu-id="beefb-121">A teljesen minősített felügyelt alkalmazásdefiníciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="beefb-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="beefb-122">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="beefb-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beefb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="beefb-123">-Name</span></span>
<span data-ttu-id="beefb-124">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="beefb-124">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beefb-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="beefb-125">-Pre</span></span>
<span data-ttu-id="beefb-126">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="beefb-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="beefb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beefb-127">-ResourceGroupName</span></span>
<span data-ttu-id="beefb-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="beefb-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beefb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beefb-129">CommonParameters</span></span>
<span data-ttu-id="beefb-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beefb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beefb-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="beefb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beefb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="beefb-132">INPUTS</span></span>

### <span data-ttu-id="beefb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="beefb-133">System.String</span></span>

## <span data-ttu-id="beefb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="beefb-134">OUTPUTS</span></span>

### <span data-ttu-id="beefb-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="beefb-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="beefb-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="beefb-136">NOTES</span></span>

## <span data-ttu-id="beefb-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="beefb-137">RELATED LINKS</span></span>
