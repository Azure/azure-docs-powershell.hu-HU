---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: a09dae99d7a2b6e08dd255cc19b859aec89808f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496928"
---
# <span data-ttu-id="2e9c3-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="2e9c3-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="2e9c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e9c3-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9c3-103">Házirend-készlet definíciójának módosítása</span><span class="sxs-lookup"><span data-stu-id="2e9c3-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e9c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e9c3-104">SYNTAX</span></span>

### <span data-ttu-id="2e9c3-105">A Policy set definition Name paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="2e9c3-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="2e9c3-106">(Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e9c3-107">A házirend-definíciós azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-107">The policy set definition Id parameter set.</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e9c3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e9c3-108">DESCRIPTION</span></span>
<span data-ttu-id="2e9c3-109">A **set-AzureRmPolicySetDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-109">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="2e9c3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2e9c3-110">EXAMPLES</span></span>

### <span data-ttu-id="2e9c3-111">Példa 1: a házirend-készlet definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="2e9c3-111">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="2e9c3-112">Az első parancs a Get-AzureRmPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="2e9c3-113">A parancs az objektumot a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-113">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="2e9c3-114">A második parancs frissíti az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-114">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="2e9c3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e9c3-115">PARAMETERS</span></span>

### <span data-ttu-id="2e9c3-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2e9c3-116">-ApiVersion</span></span>
<span data-ttu-id="2e9c3-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2e9c3-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2e9c3-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="2e9c3-119">-Description</span></span>
<span data-ttu-id="2e9c3-120">A házirend-készlet definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-120">The description for policy set definition.</span></span>

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

### <span data-ttu-id="2e9c3-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2e9c3-121">-DisplayName</span></span>
<span data-ttu-id="2e9c3-122">A házirend-készlet definíciójának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-122">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="2e9c3-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="2e9c3-123">-Id</span></span>
<span data-ttu-id="2e9c3-124">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-124">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="2e9c3-125">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="2e9c3-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="2e9c3-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e9c3-126">-Name</span></span>
<span data-ttu-id="2e9c3-127">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-127">The policy set definition name.</span></span>

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

### <span data-ttu-id="2e9c3-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2e9c3-128">-PolicyDefinition</span></span>
<span data-ttu-id="2e9c3-129">A házirend-készlet definíciója.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-129">The policy set definition.</span></span> <span data-ttu-id="2e9c3-130">Ez lehet egy elérési út a házirend-definíciókat tartalmazó fájlnévhez vagy a házirend-definíció karakterláncként való beállításához.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="2e9c3-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="2e9c3-131">-Pre</span></span>
<span data-ttu-id="2e9c3-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2e9c3-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e9c3-133">-Confirm</span></span>
<span data-ttu-id="2e9c3-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e9c3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9c3-135">-DefaultProfile</span></span>
<span data-ttu-id="2e9c3-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e9c3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e9c3-137">-WhatIf</span></span>
<span data-ttu-id="2e9c3-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e9c3-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e9c3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e9c3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9c3-140">CommonParameters</span></span>
<span data-ttu-id="2e9c3-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e9c3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9c3-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e9c3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9c3-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e9c3-143">INPUTS</span></span>

### <span data-ttu-id="2e9c3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2e9c3-144">System.String</span></span>

## <span data-ttu-id="2e9c3-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e9c3-145">OUTPUTS</span></span>

### <span data-ttu-id="2e9c3-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2e9c3-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2e9c3-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e9c3-147">NOTES</span></span>

## <span data-ttu-id="2e9c3-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e9c3-148">RELATED LINKS</span></span>

