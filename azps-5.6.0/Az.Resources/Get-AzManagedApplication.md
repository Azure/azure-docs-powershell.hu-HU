---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: c95fe4a977c70964cf8b4dab86985d79315d3141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008646"
---
# <span data-ttu-id="b2a30-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="b2a30-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="b2a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2a30-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a30-103">Felügyelt alkalmazások lekérte</span><span class="sxs-lookup"><span data-stu-id="b2a30-103">Gets managed applications</span></span>

## <span data-ttu-id="b2a30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2a30-104">SYNTAX</span></span>

### <span data-ttu-id="b2a30-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2a30-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2a30-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b2a30-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2a30-107">GetById</span><span class="sxs-lookup"><span data-stu-id="b2a30-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2a30-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2a30-108">DESCRIPTION</span></span>
<span data-ttu-id="b2a30-109">A **Get-AzManagedApplication** parancsmag felügyelt alkalmazásokat kap</span><span class="sxs-lookup"><span data-stu-id="b2a30-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="b2a30-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2a30-110">EXAMPLES</span></span>

### <span data-ttu-id="b2a30-111">1. példa: Az összes felügyelt alkalmazás lekérte egy erőforráscsoportba</span><span class="sxs-lookup"><span data-stu-id="b2a30-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="b2a30-112">Ez a parancs a felügyelt alkalmazásokat a "MyRG" erőforráscsoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b2a30-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="b2a30-113">2. példa: Az összes felügyelt alkalmazás lekérte</span><span class="sxs-lookup"><span data-stu-id="b2a30-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="b2a30-114">Ez a parancs az aktuális előfizetés alatt lévő összes felügyelt alkalmazást lekérte</span><span class="sxs-lookup"><span data-stu-id="b2a30-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="b2a30-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2a30-115">PARAMETERS</span></span>

### <span data-ttu-id="b2a30-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b2a30-116">-ApiVersion</span></span>
<span data-ttu-id="b2a30-117">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="b2a30-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b2a30-118">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b2a30-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b2a30-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a30-119">-DefaultProfile</span></span>
<span data-ttu-id="b2a30-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2a30-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2a30-121">-Id</span><span class="sxs-lookup"><span data-stu-id="b2a30-121">-Id</span></span>
<span data-ttu-id="b2a30-122">A teljesen minősített felügyelt alkalmazásazonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="b2a30-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="b2a30-123">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b2a30-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a30-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b2a30-124">-Name</span></span>
<span data-ttu-id="b2a30-125">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="b2a30-125">The managed application name.</span></span>

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

### <span data-ttu-id="b2a30-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="b2a30-126">-Pre</span></span>
<span data-ttu-id="b2a30-127">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b2a30-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b2a30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2a30-128">-ResourceGroupName</span></span>
<span data-ttu-id="b2a30-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b2a30-129">The resource group name.</span></span>

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

### <span data-ttu-id="b2a30-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a30-130">CommonParameters</span></span>
<span data-ttu-id="b2a30-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2a30-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a30-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2a30-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a30-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2a30-133">INPUTS</span></span>

### <span data-ttu-id="b2a30-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b2a30-134">System.String</span></span>

## <span data-ttu-id="b2a30-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2a30-135">OUTPUTS</span></span>

### <span data-ttu-id="b2a30-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b2a30-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b2a30-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2a30-137">NOTES</span></span>

## <span data-ttu-id="b2a30-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2a30-138">RELATED LINKS</span></span>
