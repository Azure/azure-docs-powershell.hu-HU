---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010794"
---
# <span data-ttu-id="b435b-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="b435b-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="b435b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b435b-102">SYNOPSIS</span></span>
<span data-ttu-id="b435b-103">Felügyelt alkalmazás definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b435b-103">Removes a managed application definition</span></span>

## <span data-ttu-id="b435b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b435b-104">SYNTAX</span></span>

### <span data-ttu-id="b435b-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b435b-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b435b-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="b435b-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b435b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b435b-107">DESCRIPTION</span></span>
<span data-ttu-id="b435b-108">A **Remove-AzManagedApplicationDefinition** parancsmag eltávolít egy felügyelt alkalmazás-definíciót</span><span class="sxs-lookup"><span data-stu-id="b435b-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="b435b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b435b-109">EXAMPLES</span></span>

### <span data-ttu-id="b435b-110">Példa 1: a felügyelt alkalmazás definíciójának eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="b435b-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="b435b-111">Az első parancs az Get-AzManagedApplicationDefinition parancsmag használatával megkapja a myAppDef nevű felügyelt alkalmazás definícióját.</span><span class="sxs-lookup"><span data-stu-id="b435b-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="b435b-112">A parancs a $ApplicationDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b435b-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="b435b-113">A második parancs eltávolítja a felügyelt alkalmazás definícióját, amelyet az $ApplicationDefinition **ResourceId** tulajdonsága határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b435b-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="b435b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b435b-114">PARAMETERS</span></span>

### <span data-ttu-id="b435b-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b435b-115">-ApiVersion</span></span>
<span data-ttu-id="b435b-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b435b-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b435b-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b435b-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b435b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b435b-118">-DefaultProfile</span></span>
<span data-ttu-id="b435b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b435b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b435b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b435b-120">-Force</span></span>
<span data-ttu-id="b435b-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b435b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b435b-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b435b-122">-Id</span></span>
<span data-ttu-id="b435b-123">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="b435b-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="b435b-124">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b435b-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b435b-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b435b-125">-Name</span></span>
<span data-ttu-id="b435b-126">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="b435b-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="b435b-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="b435b-127">-Pre</span></span>
<span data-ttu-id="b435b-128">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b435b-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b435b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b435b-129">-ResourceGroupName</span></span>
<span data-ttu-id="b435b-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b435b-130">The resource group name.</span></span>

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

### <span data-ttu-id="b435b-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b435b-131">-Confirm</span></span>
<span data-ttu-id="b435b-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b435b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b435b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b435b-133">-WhatIf</span></span>
<span data-ttu-id="b435b-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b435b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b435b-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b435b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b435b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b435b-136">CommonParameters</span></span>
<span data-ttu-id="b435b-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b435b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b435b-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b435b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b435b-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b435b-139">INPUTS</span></span>

### <span data-ttu-id="b435b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b435b-140">System.String</span></span>

## <span data-ttu-id="b435b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b435b-141">OUTPUTS</span></span>

### <span data-ttu-id="b435b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b435b-142">System.Boolean</span></span>

## <span data-ttu-id="b435b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b435b-143">NOTES</span></span>

## <span data-ttu-id="b435b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b435b-144">RELATED LINKS</span></span>
