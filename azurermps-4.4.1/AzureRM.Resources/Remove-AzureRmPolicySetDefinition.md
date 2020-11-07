---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d3b9d8af81f08786536abf0d26b3c4ba2f2d66bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679036"
---
# <span data-ttu-id="6876e-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6876e-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="6876e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6876e-102">SYNOPSIS</span></span>
<span data-ttu-id="6876e-103">Házirend-készlet definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6876e-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6876e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6876e-104">SYNTAX</span></span>

### <span data-ttu-id="6876e-105">A Policy set definition Name paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="6876e-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="6876e-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="6876e-106">(Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6876e-107">A házirend-definíciós azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="6876e-107">The policy set definition Id parameter set.</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6876e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6876e-108">DESCRIPTION</span></span>
<span data-ttu-id="6876e-109">A **Remove-AzureRmPolicySetDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="6876e-109">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="6876e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6876e-110">EXAMPLES</span></span>

### <span data-ttu-id="6876e-111">Példa 1: a házirend-készlet definíciójának eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="6876e-111">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="6876e-112">Az első parancs a Get-AzureRmPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="6876e-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="6876e-113">A parancs a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6876e-113">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="6876e-114">A második parancs eltávolítja az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="6876e-114">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="6876e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6876e-115">PARAMETERS</span></span>

### <span data-ttu-id="6876e-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6876e-116">-ApiVersion</span></span>
<span data-ttu-id="6876e-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6876e-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6876e-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6876e-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6876e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6876e-119">-Force</span></span>
<span data-ttu-id="6876e-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6876e-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6876e-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="6876e-121">-Id</span></span>
<span data-ttu-id="6876e-122">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="6876e-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="6876e-123">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6876e-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6876e-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6876e-124">-Name</span></span>
<span data-ttu-id="6876e-125">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="6876e-125">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6876e-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="6876e-126">-Pre</span></span>
<span data-ttu-id="6876e-127">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6876e-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6876e-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6876e-128">-Confirm</span></span>
<span data-ttu-id="6876e-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6876e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6876e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6876e-130">-WhatIf</span></span>
<span data-ttu-id="6876e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6876e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6876e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6876e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6876e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6876e-133">-DefaultProfile</span></span>
<span data-ttu-id="6876e-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6876e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6876e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6876e-135">CommonParameters</span></span>
<span data-ttu-id="6876e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6876e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6876e-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6876e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6876e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6876e-138">INPUTS</span></span>

### <span data-ttu-id="6876e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6876e-139">System.String</span></span>

## <span data-ttu-id="6876e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6876e-140">OUTPUTS</span></span>

### <span data-ttu-id="6876e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6876e-141">System.Boolean</span></span>

## <span data-ttu-id="6876e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6876e-142">NOTES</span></span>

## <span data-ttu-id="6876e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6876e-143">RELATED LINKS</span></span>

