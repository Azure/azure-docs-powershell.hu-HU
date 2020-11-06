---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492188"
---
# <span data-ttu-id="b69bd-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b69bd-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b69bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b69bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b69bd-103">Házirend-készlet definíciójának módosítása</span><span class="sxs-lookup"><span data-stu-id="b69bd-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b69bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b69bd-104">SYNTAX</span></span>

### <span data-ttu-id="b69bd-105">SetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b69bd-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b69bd-106">SetById</span><span class="sxs-lookup"><span data-stu-id="b69bd-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b69bd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b69bd-107">DESCRIPTION</span></span>
<span data-ttu-id="b69bd-108">A **set-AzureRmPolicySetDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="b69bd-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="b69bd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b69bd-109">EXAMPLES</span></span>

### <span data-ttu-id="b69bd-110">Példa 1: a házirend-készlet definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b69bd-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="b69bd-111">Az első parancs a Get-AzureRmPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="b69bd-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b69bd-112">A parancs az objektumot a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b69bd-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="b69bd-113">A második parancs frissíti az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="b69bd-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="b69bd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b69bd-114">PARAMETERS</span></span>

### <span data-ttu-id="b69bd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b69bd-115">-ApiVersion</span></span>
<span data-ttu-id="b69bd-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b69bd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b69bd-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b69bd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b69bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b69bd-118">-DefaultProfile</span></span>
<span data-ttu-id="b69bd-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b69bd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b69bd-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b69bd-120">-Description</span></span>
<span data-ttu-id="b69bd-121">A házirend-készlet definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="b69bd-121">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b69bd-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b69bd-122">-DisplayName</span></span>
<span data-ttu-id="b69bd-123">A házirend-készlet definíciójának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="b69bd-123">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b69bd-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b69bd-124">-Id</span></span>
<span data-ttu-id="b69bd-125">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="b69bd-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="b69bd-126">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b69bd-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b69bd-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b69bd-127">-Name</span></span>
<span data-ttu-id="b69bd-128">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="b69bd-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b69bd-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b69bd-129">-PolicyDefinition</span></span>
<span data-ttu-id="b69bd-130">A házirend-készlet definíciója.</span><span class="sxs-lookup"><span data-stu-id="b69bd-130">The policy set definition.</span></span> <span data-ttu-id="b69bd-131">Ez lehet egy elérési út a házirend-definíciókat tartalmazó fájlnévhez vagy a házirend-definíció karakterláncként való beállításához.</span><span class="sxs-lookup"><span data-stu-id="b69bd-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b69bd-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="b69bd-132">-Pre</span></span>
<span data-ttu-id="b69bd-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b69bd-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b69bd-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b69bd-134">-Confirm</span></span>
<span data-ttu-id="b69bd-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b69bd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b69bd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b69bd-136">-WhatIf</span></span>
<span data-ttu-id="b69bd-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b69bd-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b69bd-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b69bd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b69bd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b69bd-139">CommonParameters</span></span>
<span data-ttu-id="b69bd-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b69bd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b69bd-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b69bd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b69bd-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b69bd-142">INPUTS</span></span>

### <span data-ttu-id="b69bd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b69bd-143">System.String</span></span>

## <span data-ttu-id="b69bd-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b69bd-144">OUTPUTS</span></span>

### <span data-ttu-id="b69bd-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b69bd-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b69bd-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b69bd-146">NOTES</span></span>

## <span data-ttu-id="b69bd-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b69bd-147">RELATED LINKS</span></span>
