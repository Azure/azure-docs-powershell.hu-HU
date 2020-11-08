---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181943"
---
# <span data-ttu-id="1e9c3-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="1e9c3-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="1e9c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e9c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9c3-103">Felügyelt alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1e9c3-103">Removes a managed application</span></span>

## <span data-ttu-id="1e9c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e9c3-104">SYNTAX</span></span>

### <span data-ttu-id="1e9c3-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e9c3-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e9c3-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="1e9c3-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e9c3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e9c3-107">DESCRIPTION</span></span>
<span data-ttu-id="1e9c3-108">A **Remove-AzManagedApplication** parancsmag eltávolítja a felügyelt alkalmazást</span><span class="sxs-lookup"><span data-stu-id="1e9c3-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="1e9c3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1e9c3-109">EXAMPLES</span></span>

### <span data-ttu-id="1e9c3-110">1. példa: a felügyelt alkalmazások erőforrás-AZONOSÍTÓval való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1e9c3-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="1e9c3-111">Az első parancs az Get-AzManagedApplication parancsmag használatával megkapja a SajátPr nevű felügyelt alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="1e9c3-112">A parancs a $Application változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="1e9c3-113">A második parancs eltávolítja a felügyelt alkalmazást, amelyet a $Application **ResourceId** tulajdonsága azonosította.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="1e9c3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e9c3-114">PARAMETERS</span></span>

### <span data-ttu-id="1e9c3-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1e9c3-115">-ApiVersion</span></span>
<span data-ttu-id="1e9c3-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1e9c3-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1e9c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9c3-118">-DefaultProfile</span></span>
<span data-ttu-id="1e9c3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e9c3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1e9c3-120">-Force</span></span>
<span data-ttu-id="1e9c3-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1e9c3-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="1e9c3-122">-Id</span></span>
<span data-ttu-id="1e9c3-123">A teljes mértékben minősített felügyelt alkalmazásspecifikus azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="1e9c3-124">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1e9c3-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9c3-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e9c3-125">-Name</span></span>
<span data-ttu-id="1e9c3-126">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9c3-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="1e9c3-127">-Pre</span></span>
<span data-ttu-id="1e9c3-128">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1e9c3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9c3-129">-ResourceGroupName</span></span>
<span data-ttu-id="1e9c3-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9c3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e9c3-131">-Confirm</span></span>
<span data-ttu-id="1e9c3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9c3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9c3-133">-WhatIf</span></span>
<span data-ttu-id="1e9c3-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e9c3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9c3-136">CommonParameters</span></span>
<span data-ttu-id="1e9c3-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e9c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9c3-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9c3-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e9c3-139">INPUTS</span></span>

### <span data-ttu-id="1e9c3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1e9c3-140">System.String</span></span>

## <span data-ttu-id="1e9c3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e9c3-141">OUTPUTS</span></span>

### <span data-ttu-id="1e9c3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e9c3-142">System.Boolean</span></span>

## <span data-ttu-id="1e9c3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e9c3-143">NOTES</span></span>

## <span data-ttu-id="1e9c3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e9c3-144">RELATED LINKS</span></span>
