---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498848"
---
# <span data-ttu-id="71244-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="71244-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="71244-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71244-102">SYNOPSIS</span></span>
<span data-ttu-id="71244-103">Házirend-készlet definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="71244-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71244-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71244-104">SYNTAX</span></span>

### <span data-ttu-id="71244-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71244-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71244-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="71244-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71244-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="71244-107">DESCRIPTION</span></span>
<span data-ttu-id="71244-108">A **Remove-AzureRmPolicySetDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="71244-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="71244-109">Példák</span><span class="sxs-lookup"><span data-stu-id="71244-109">EXAMPLES</span></span>

### <span data-ttu-id="71244-110">Példa 1: a házirend-készlet definíciójának eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="71244-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="71244-111">Az első parancs a Get-AzureRmPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="71244-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="71244-112">A parancs a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="71244-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="71244-113">A második parancs eltávolítja az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="71244-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="71244-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71244-114">PARAMETERS</span></span>

### <span data-ttu-id="71244-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71244-115">-ApiVersion</span></span>
<span data-ttu-id="71244-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="71244-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="71244-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="71244-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71244-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71244-118">-DefaultProfile</span></span>
<span data-ttu-id="71244-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="71244-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71244-120">-Force</span><span class="sxs-lookup"><span data-stu-id="71244-120">-Force</span></span>
<span data-ttu-id="71244-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71244-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71244-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="71244-122">-Id</span></span>
<span data-ttu-id="71244-123">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="71244-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="71244-124">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="71244-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71244-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71244-125">-Name</span></span>
<span data-ttu-id="71244-126">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="71244-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71244-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="71244-127">-Pre</span></span>
<span data-ttu-id="71244-128">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="71244-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71244-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71244-129">-Confirm</span></span>
<span data-ttu-id="71244-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71244-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71244-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71244-131">-WhatIf</span></span>
<span data-ttu-id="71244-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71244-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71244-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71244-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71244-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71244-134">CommonParameters</span></span>
<span data-ttu-id="71244-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71244-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71244-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71244-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71244-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71244-137">INPUTS</span></span>

### <span data-ttu-id="71244-138">System. String</span><span class="sxs-lookup"><span data-stu-id="71244-138">System.String</span></span>

## <span data-ttu-id="71244-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71244-139">OUTPUTS</span></span>

### <span data-ttu-id="71244-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71244-140">System.Boolean</span></span>

## <span data-ttu-id="71244-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71244-141">NOTES</span></span>

## <span data-ttu-id="71244-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71244-142">RELATED LINKS</span></span>
