---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 148f7b22a9df77532f574457da453e9e4b07a846
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843241"
---
# <span data-ttu-id="a712f-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="a712f-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="a712f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a712f-102">SYNOPSIS</span></span>
<span data-ttu-id="a712f-103">Házirend-készlet definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a712f-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="a712f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a712f-104">SYNTAX</span></span>

### <span data-ttu-id="a712f-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a712f-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a712f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a712f-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a712f-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a712f-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a712f-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a712f-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a712f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a712f-109">DESCRIPTION</span></span>
<span data-ttu-id="a712f-110">A **Remove-AzPolicySetDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a712f-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="a712f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a712f-111">EXAMPLES</span></span>

### <span data-ttu-id="a712f-112">Példa 1: a házirend-készlet definíciójának eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="a712f-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="a712f-113">Az első parancs a Get-AzPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="a712f-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="a712f-114">A parancs a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a712f-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="a712f-115">A második parancs eltávolítja az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a712f-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="a712f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a712f-116">PARAMETERS</span></span>

### <span data-ttu-id="a712f-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a712f-117">-ApiVersion</span></span>
<span data-ttu-id="a712f-118">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a712f-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a712f-119">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a712f-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a712f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a712f-120">-DefaultProfile</span></span>
<span data-ttu-id="a712f-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a712f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a712f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a712f-122">-Force</span></span>
<span data-ttu-id="a712f-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a712f-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a712f-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a712f-124">-Id</span></span>
<span data-ttu-id="a712f-125">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="a712f-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="a712f-126">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="a712f-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a712f-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a712f-127">-ManagementGroupName</span></span>
<span data-ttu-id="a712f-128">A törölni kívánt Policy set Definition (felügyeleti csoport) neve.</span><span class="sxs-lookup"><span data-stu-id="a712f-128">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a712f-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a712f-129">-Name</span></span>
<span data-ttu-id="a712f-130">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="a712f-130">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a712f-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="a712f-131">-Pre</span></span>
<span data-ttu-id="a712f-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a712f-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a712f-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a712f-133">-SubscriptionId</span></span>
<span data-ttu-id="a712f-134">A törléshez a házirend-készlet definíciójának előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a712f-134">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a712f-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a712f-135">-Confirm</span></span>
<span data-ttu-id="a712f-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a712f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a712f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a712f-137">-WhatIf</span></span>
<span data-ttu-id="a712f-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a712f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a712f-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a712f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a712f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a712f-140">CommonParameters</span></span>
<span data-ttu-id="a712f-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a712f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a712f-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a712f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a712f-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a712f-143">INPUTS</span></span>

### <span data-ttu-id="a712f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a712f-144">System.String</span></span>

### <span data-ttu-id="a712f-145">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a712f-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a712f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a712f-146">OUTPUTS</span></span>

### <span data-ttu-id="a712f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a712f-147">System.Boolean</span></span>

## <span data-ttu-id="a712f-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a712f-148">NOTES</span></span>

## <span data-ttu-id="a712f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a712f-149">RELATED LINKS</span></span>
