---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181422"
---
# <span data-ttu-id="4043b-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="4043b-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="4043b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4043b-102">SYNOPSIS</span></span>
<span data-ttu-id="4043b-103">Házirend-készlet definícióját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4043b-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="4043b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4043b-104">SYNTAX</span></span>

### <span data-ttu-id="4043b-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4043b-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4043b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4043b-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4043b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4043b-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4043b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4043b-108">DESCRIPTION</span></span>
<span data-ttu-id="4043b-109">A **New-AzPolicySetDefinition** parancsmag létrehoz egy házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="4043b-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="4043b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4043b-110">EXAMPLES</span></span>

### <span data-ttu-id="4043b-111">1. példa: házirend-készlet definíciójának létrehozása a metaadatokkal egy házirendfájl használatával</span><span class="sxs-lookup"><span data-stu-id="4043b-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="4043b-112">Ez a parancs létrehoz egy VMPolicySetDefinition nevű házirend-definíciós definíciót, amely azt jelzi, hogy a kategóriája a "virtuális gép", amely a C:\VMPolicy.jsban megadott házirend-definíciókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4043b-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="4043b-113">Példa: a fenti VMPolicy.jstartalma.</span><span class="sxs-lookup"><span data-stu-id="4043b-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="4043b-114">2. példa: paraméteres házirend-készlet definíciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="4043b-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="4043b-115">Ez a parancs létrehoz egy VMPolicySetDefinition nevű, paraméteres házirend-definíciós definíciót, amely a C:\VMPolicy.jsban megadott házirend-definíciókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4043b-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="4043b-116">Példa: a fenti VMPolicy.jstartalma.</span><span class="sxs-lookup"><span data-stu-id="4043b-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="4043b-117">3. példa: házirend-definíciós definíció létrehozása házirend-definíciós csoportokkal</span><span class="sxs-lookup"><span data-stu-id="4043b-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="4043b-118">Ez a parancs létrehoz egy VMPolicySetDefinition nevű házirend-definíciós definíciót, amelyben a C:\VMPolicy.jsbe van állítva a házirend-definíciók csoportja.</span><span class="sxs-lookup"><span data-stu-id="4043b-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="4043b-119">Példa: a fenti VMPolicy.jstartalma.</span><span class="sxs-lookup"><span data-stu-id="4043b-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="4043b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4043b-120">PARAMETERS</span></span>

### <span data-ttu-id="4043b-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4043b-121">-ApiVersion</span></span>
<span data-ttu-id="4043b-122">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4043b-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4043b-123">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4043b-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4043b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4043b-124">-DefaultProfile</span></span>
<span data-ttu-id="4043b-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4043b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4043b-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4043b-126">-Description</span></span>
<span data-ttu-id="4043b-127">A házirend-készlet definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="4043b-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="4043b-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4043b-128">-DisplayName</span></span>
<span data-ttu-id="4043b-129">A házirend-készlet definíciójának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="4043b-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="4043b-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="4043b-130">-GroupDefinition</span></span>
<span data-ttu-id="4043b-131">Az új házirendprofil definíciójának házirend-definíciós csoportjai.</span><span class="sxs-lookup"><span data-stu-id="4043b-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="4043b-132">Ez lehet a csoportokat tartalmazó fájl elérési útja, vagy a csoportok JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="4043b-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="4043b-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4043b-133">-ManagementGroupName</span></span>
<span data-ttu-id="4043b-134">Az új házirend-definíciós csoport felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="4043b-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="4043b-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4043b-135">-Metadata</span></span>
<span data-ttu-id="4043b-136">A házirend-készlet definíciójának metaadatai.</span><span class="sxs-lookup"><span data-stu-id="4043b-136">The metadata for policy set definition.</span></span> <span data-ttu-id="4043b-137">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok használata JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="4043b-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="4043b-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4043b-138">-Name</span></span>
<span data-ttu-id="4043b-139">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="4043b-139">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4043b-140">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="4043b-140">-Parameter</span></span>
<span data-ttu-id="4043b-141">A Parameters deklaráció a házirend-készlet definíciójában.</span><span class="sxs-lookup"><span data-stu-id="4043b-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="4043b-142">Ez lehet egy elérési út a Parameters deklarációt tartalmazó fájlnévhez vagy a Parameters deklaráció JSON-karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="4043b-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="4043b-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4043b-143">-PolicyDefinition</span></span>
<span data-ttu-id="4043b-144">A házirend-definíciók.</span><span class="sxs-lookup"><span data-stu-id="4043b-144">The policy definitions.</span></span> <span data-ttu-id="4043b-145">Ez lehet egy elérési út a házirend-definíciókat tartalmazó fájlnévhez vagy a házirend-definíciók JSON-karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="4043b-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4043b-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="4043b-146">-Pre</span></span>
<span data-ttu-id="4043b-147">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4043b-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4043b-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4043b-148">-SubscriptionId</span></span>
<span data-ttu-id="4043b-149">Az új házirend-készlet definíciójának előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4043b-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="4043b-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4043b-150">-Confirm</span></span>
<span data-ttu-id="4043b-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4043b-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4043b-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4043b-152">-WhatIf</span></span>
<span data-ttu-id="4043b-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4043b-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4043b-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4043b-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4043b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4043b-155">CommonParameters</span></span>
<span data-ttu-id="4043b-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4043b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4043b-157">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4043b-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4043b-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4043b-158">INPUTS</span></span>

### <span data-ttu-id="4043b-159">System. String</span><span class="sxs-lookup"><span data-stu-id="4043b-159">System.String</span></span>

### <span data-ttu-id="4043b-160">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4043b-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4043b-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4043b-161">OUTPUTS</span></span>

### <span data-ttu-id="4043b-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4043b-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4043b-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4043b-163">NOTES</span></span>

## <span data-ttu-id="4043b-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4043b-164">RELATED LINKS</span></span>
