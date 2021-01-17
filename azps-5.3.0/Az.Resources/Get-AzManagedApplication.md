---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466534"
---
# <span data-ttu-id="8ed20-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="8ed20-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="8ed20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ed20-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed20-103">Felügyelt alkalmazások lekérte</span><span class="sxs-lookup"><span data-stu-id="8ed20-103">Gets managed applications</span></span>

## <span data-ttu-id="8ed20-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ed20-104">SYNTAX</span></span>

### <span data-ttu-id="8ed20-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ed20-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ed20-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8ed20-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ed20-107">GetById</span><span class="sxs-lookup"><span data-stu-id="8ed20-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ed20-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ed20-108">DESCRIPTION</span></span>
<span data-ttu-id="8ed20-109">A **Get-AzManagedApplication** parancsmag felügyelt alkalmazásokat kap</span><span class="sxs-lookup"><span data-stu-id="8ed20-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="8ed20-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ed20-110">EXAMPLES</span></span>

### <span data-ttu-id="8ed20-111">1. példa: Az összes felügyelt alkalmazás lekérte egy erőforráscsoportba</span><span class="sxs-lookup"><span data-stu-id="8ed20-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="8ed20-112">Ez a parancs a felügyelt alkalmazásokat a "MyRG" erőforráscsoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8ed20-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="8ed20-113">2. példa: Az összes felügyelt alkalmazás lekérte</span><span class="sxs-lookup"><span data-stu-id="8ed20-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="8ed20-114">Ez a parancs az aktuális előfizetés alatt lévő összes felügyelt alkalmazást lekérte</span><span class="sxs-lookup"><span data-stu-id="8ed20-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="8ed20-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ed20-115">PARAMETERS</span></span>

### <span data-ttu-id="8ed20-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8ed20-116">-ApiVersion</span></span>
<span data-ttu-id="8ed20-117">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="8ed20-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8ed20-118">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8ed20-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8ed20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed20-119">-DefaultProfile</span></span>
<span data-ttu-id="8ed20-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ed20-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ed20-121">-Id</span><span class="sxs-lookup"><span data-stu-id="8ed20-121">-Id</span></span>
<span data-ttu-id="8ed20-122">A teljesen minősített felügyelt alkalmazásazonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="8ed20-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="8ed20-123">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="8ed20-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="8ed20-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8ed20-124">-Name</span></span>
<span data-ttu-id="8ed20-125">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="8ed20-125">The managed application name.</span></span>

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

### <span data-ttu-id="8ed20-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="8ed20-126">-Pre</span></span>
<span data-ttu-id="8ed20-127">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8ed20-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8ed20-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ed20-128">-ResourceGroupName</span></span>
<span data-ttu-id="8ed20-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ed20-129">The resource group name.</span></span>

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

### <span data-ttu-id="8ed20-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed20-130">CommonParameters</span></span>
<span data-ttu-id="8ed20-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed20-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed20-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ed20-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed20-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ed20-133">INPUTS</span></span>

### <span data-ttu-id="8ed20-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8ed20-134">System.String</span></span>

## <span data-ttu-id="8ed20-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ed20-135">OUTPUTS</span></span>

### <span data-ttu-id="8ed20-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8ed20-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8ed20-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ed20-137">NOTES</span></span>

## <span data-ttu-id="8ed20-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ed20-138">RELATED LINKS</span></span>
