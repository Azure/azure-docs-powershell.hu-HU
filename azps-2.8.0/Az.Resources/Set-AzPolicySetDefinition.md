---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 5b6d514fc41c909fdd48b6a13ba85ab5836a5668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838875"
---
# <span data-ttu-id="89485-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="89485-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="89485-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89485-102">SYNOPSIS</span></span>
<span data-ttu-id="89485-103">Házirend-készlet definíciójának módosítása</span><span class="sxs-lookup"><span data-stu-id="89485-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="89485-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89485-104">SYNTAX</span></span>

### <span data-ttu-id="89485-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89485-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89485-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="89485-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89485-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89485-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89485-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89485-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89485-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="89485-109">DESCRIPTION</span></span>
<span data-ttu-id="89485-110">A **set-AzPolicySetDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="89485-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="89485-111">Példák</span><span class="sxs-lookup"><span data-stu-id="89485-111">EXAMPLES</span></span>

### <span data-ttu-id="89485-112">Példa 1: a házirend-készlet definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="89485-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="89485-113">Az első parancs a Get-AzPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="89485-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="89485-114">A parancs az objektumot a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89485-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="89485-115">A második parancs frissíti az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="89485-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="89485-116">2. példa: egy házirend-definíciós definíció metaadatait frissíti</span><span class="sxs-lookup"><span data-stu-id="89485-116">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="89485-117">Ez a parancs frissíti a VMPolicySetDefinition nevű, a "virtuális gép" kategóriát tartalmazó irányelvmodul-definíció metaadatait.</span><span class="sxs-lookup"><span data-stu-id="89485-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="89485-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89485-118">PARAMETERS</span></span>

### <span data-ttu-id="89485-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="89485-119">-ApiVersion</span></span>
<span data-ttu-id="89485-120">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="89485-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="89485-121">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="89485-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="89485-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89485-122">-DefaultProfile</span></span>
<span data-ttu-id="89485-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="89485-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89485-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="89485-124">-Description</span></span>
<span data-ttu-id="89485-125">A házirend-készlet definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="89485-125">The description for policy set definition.</span></span>

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

### <span data-ttu-id="89485-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="89485-126">-DisplayName</span></span>
<span data-ttu-id="89485-127">A házirend-készlet definíciójának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="89485-127">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="89485-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="89485-128">-Id</span></span>
<span data-ttu-id="89485-129">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="89485-129">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="89485-130">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="89485-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="89485-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="89485-131">-ManagementGroupName</span></span>
<span data-ttu-id="89485-132">A frissítéshez a Policy set definition Definition (felügyeleti csoport) neve.</span><span class="sxs-lookup"><span data-stu-id="89485-132">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="89485-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="89485-133">-Metadata</span></span>
<span data-ttu-id="89485-134">A frissített házirend-készlet definíciójának metaadatai.</span><span class="sxs-lookup"><span data-stu-id="89485-134">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="89485-135">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="89485-135">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="89485-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89485-136">-Name</span></span>
<span data-ttu-id="89485-137">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="89485-137">The policy set definition name.</span></span>

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

### <span data-ttu-id="89485-138">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="89485-138">-Parameter</span></span>
<span data-ttu-id="89485-139">A frissített házirend-definíció paramétereinek deklarációja.</span><span class="sxs-lookup"><span data-stu-id="89485-139">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="89485-140">Ez a paraméter a Parameters deklarációt vagy a Parameters deklarációt tartalmazó fájlnév vagy URI elérési útját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="89485-140">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="89485-141">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89485-141">-PolicyDefinition</span></span>
<span data-ttu-id="89485-142">A házirend-definíciók.</span><span class="sxs-lookup"><span data-stu-id="89485-142">The policy definitions.</span></span> <span data-ttu-id="89485-143">Ez lehet a házirend-definíciókat tartalmazó fájlnév vagy a házirend-definíciók karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="89485-143">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="89485-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="89485-144">-Pre</span></span>
<span data-ttu-id="89485-145">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="89485-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="89485-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89485-146">-SubscriptionId</span></span>
<span data-ttu-id="89485-147">A házirend-készlet definíciójának előfizetés azonosítója a frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="89485-147">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="89485-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89485-148">-Confirm</span></span>
<span data-ttu-id="89485-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89485-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89485-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89485-150">-WhatIf</span></span>
<span data-ttu-id="89485-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89485-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89485-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89485-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89485-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89485-153">CommonParameters</span></span>
<span data-ttu-id="89485-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89485-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89485-155">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89485-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89485-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89485-156">INPUTS</span></span>

### <span data-ttu-id="89485-157">System. String</span><span class="sxs-lookup"><span data-stu-id="89485-157">System.String</span></span>

### <span data-ttu-id="89485-158">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="89485-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="89485-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89485-159">OUTPUTS</span></span>

### <span data-ttu-id="89485-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="89485-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="89485-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89485-161">NOTES</span></span>

## <span data-ttu-id="89485-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89485-162">RELATED LINKS</span></span>
