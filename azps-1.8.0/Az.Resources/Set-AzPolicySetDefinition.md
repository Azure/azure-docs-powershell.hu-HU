---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: da4a08e46abce04b4a30726a419582a22b6e0b41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669312"
---
# <span data-ttu-id="78af8-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="78af8-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="78af8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78af8-102">SYNOPSIS</span></span>
<span data-ttu-id="78af8-103">Házirend-készlet definíciójának módosítása</span><span class="sxs-lookup"><span data-stu-id="78af8-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="78af8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78af8-104">SYNTAX</span></span>

### <span data-ttu-id="78af8-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78af8-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78af8-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78af8-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78af8-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78af8-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78af8-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78af8-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78af8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="78af8-109">DESCRIPTION</span></span>
<span data-ttu-id="78af8-110">A **set-AzPolicySetDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="78af8-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="78af8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="78af8-111">EXAMPLES</span></span>

### <span data-ttu-id="78af8-112">Példa 1: a házirend-készlet definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="78af8-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="78af8-113">Az első parancs a Get-AzPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="78af8-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="78af8-114">A parancs az objektumot a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="78af8-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="78af8-115">A második parancs frissíti az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="78af8-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="78af8-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78af8-116">PARAMETERS</span></span>

### <span data-ttu-id="78af8-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="78af8-117">-ApiVersion</span></span>
<span data-ttu-id="78af8-118">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="78af8-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="78af8-119">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="78af8-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="78af8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78af8-120">-DefaultProfile</span></span>
<span data-ttu-id="78af8-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="78af8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78af8-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="78af8-122">-Description</span></span>
<span data-ttu-id="78af8-123">A házirend-készlet definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="78af8-123">The description for policy set definition.</span></span>

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

### <span data-ttu-id="78af8-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="78af8-124">-DisplayName</span></span>
<span data-ttu-id="78af8-125">A házirend-készlet definíciójának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="78af8-125">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="78af8-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="78af8-126">-Id</span></span>
<span data-ttu-id="78af8-127">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="78af8-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="78af8-128">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="78af8-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="78af8-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="78af8-129">-ManagementGroupName</span></span>
<span data-ttu-id="78af8-130">A frissítéshez a Policy set definition Definition (felügyeleti csoport) neve.</span><span class="sxs-lookup"><span data-stu-id="78af8-130">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="78af8-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="78af8-131">-Metadata</span></span>
<span data-ttu-id="78af8-132">A frissített házirend-készlet definíciójának metaadatai.</span><span class="sxs-lookup"><span data-stu-id="78af8-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="78af8-133">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="78af8-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="78af8-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78af8-134">-Name</span></span>
<span data-ttu-id="78af8-135">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="78af8-135">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78af8-136">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="78af8-136">-Parameter</span></span>
<span data-ttu-id="78af8-137">A frissített házirend-definíció paramétereinek deklarációja.</span><span class="sxs-lookup"><span data-stu-id="78af8-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="78af8-138">Ez a paraméter a Parameters deklarációt vagy a Parameters deklarációt tartalmazó fájlnév vagy URI elérési útját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="78af8-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="78af8-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="78af8-139">-PolicyDefinition</span></span>
<span data-ttu-id="78af8-140">A házirend-készlet definíciója.</span><span class="sxs-lookup"><span data-stu-id="78af8-140">The policy set definition.</span></span> <span data-ttu-id="78af8-141">Ez lehet egy elérési út a házirend-definíciókat tartalmazó fájlnévhez vagy a házirend-definíció karakterláncként való beállításához.</span><span class="sxs-lookup"><span data-stu-id="78af8-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="78af8-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="78af8-142">-Pre</span></span>
<span data-ttu-id="78af8-143">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="78af8-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="78af8-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78af8-144">-SubscriptionId</span></span>
<span data-ttu-id="78af8-145">A házirend-készlet definíciójának előfizetés azonosítója a frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="78af8-145">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="78af8-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78af8-146">-Confirm</span></span>
<span data-ttu-id="78af8-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78af8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78af8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78af8-148">-WhatIf</span></span>
<span data-ttu-id="78af8-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78af8-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78af8-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78af8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78af8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78af8-151">CommonParameters</span></span>
<span data-ttu-id="78af8-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78af8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78af8-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78af8-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78af8-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78af8-154">INPUTS</span></span>

### <span data-ttu-id="78af8-155">System. String</span><span class="sxs-lookup"><span data-stu-id="78af8-155">System.String</span></span>

### <span data-ttu-id="78af8-156">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78af8-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="78af8-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78af8-157">OUTPUTS</span></span>

### <span data-ttu-id="78af8-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="78af8-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="78af8-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78af8-159">NOTES</span></span>

## <span data-ttu-id="78af8-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78af8-160">RELATED LINKS</span></span>
