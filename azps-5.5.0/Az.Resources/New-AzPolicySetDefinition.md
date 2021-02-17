---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159978"
---
# <span data-ttu-id="08685-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="08685-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="08685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08685-102">SYNOPSIS</span></span>
<span data-ttu-id="08685-103">Házirendkészlet-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="08685-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="08685-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="08685-104">SYNTAX</span></span>

### <span data-ttu-id="08685-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08685-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08685-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08685-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08685-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08685-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08685-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="08685-108">DESCRIPTION</span></span>
<span data-ttu-id="08685-109">A **New-AzPolicySetDefinition parancsmag** létrehoz egy házirendkészlet-definíciót.</span><span class="sxs-lookup"><span data-stu-id="08685-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="08685-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="08685-110">EXAMPLES</span></span>

### <span data-ttu-id="08685-111">1. példa: Házirendkészlet-definíció létrehozása metaadatokkal egy házirendkészletfájl használatával</span><span class="sxs-lookup"><span data-stu-id="08685-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="08685-112">Ez a parancs létrehoz egy VMPolicySetDefinition nevű házirendkészlet-definíciót, metaadatokkal jelezve, hogy a kategória "Virtuális gép", amely a C:\VMPolicy.jsmegadott házirenddefiníciókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="08685-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="08685-113">A fenti példában VMPolicy.jsa be van téve.</span><span class="sxs-lookup"><span data-stu-id="08685-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="08685-114">2. példa: Paraméteres házirendkészlet-definíció létrehozása</span><span class="sxs-lookup"><span data-stu-id="08685-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="08685-115">Ez a parancs létrehoz egy VMPolicySetDefinition nevű paraméteres házirendkészlet-definíciót, amely tartalmazza a C:\VMPolicy.jsházirenddefiníciókat.</span><span class="sxs-lookup"><span data-stu-id="08685-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="08685-116">A fenti példában VMPolicy.jsa be van téve.</span><span class="sxs-lookup"><span data-stu-id="08685-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="08685-117">3. példa: Házirendkészlet-definíció létrehozása házirenddefiníciós csoportokkal</span><span class="sxs-lookup"><span data-stu-id="08685-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="08685-118">Ez a parancs létrehoz egy VMPolicySetDefinition nevű házirendkészlet-definíciót, amely a be van állítva a C:\VMPolicy.jscsoportosításával.</span><span class="sxs-lookup"><span data-stu-id="08685-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="08685-119">A fenti példában VMPolicy.jsa be van téve.</span><span class="sxs-lookup"><span data-stu-id="08685-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="08685-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08685-120">PARAMETERS</span></span>

### <span data-ttu-id="08685-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="08685-121">-ApiVersion</span></span>
<span data-ttu-id="08685-122">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="08685-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="08685-123">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="08685-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="08685-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08685-124">-DefaultProfile</span></span>
<span data-ttu-id="08685-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="08685-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08685-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="08685-126">-Description</span></span>
<span data-ttu-id="08685-127">A házirendkészlet-definíció leírása.</span><span class="sxs-lookup"><span data-stu-id="08685-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="08685-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="08685-128">-DisplayName</span></span>
<span data-ttu-id="08685-129">A házirendkészlet-definíció megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="08685-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="08685-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="08685-130">-GroupDefinition</span></span>
<span data-ttu-id="08685-131">Az új házirendkészlet-definíció házirenddefiníciós csoportjai.</span><span class="sxs-lookup"><span data-stu-id="08685-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="08685-132">Ez lehet egy olyan fájl elérési útja, amely a csoportokat tartalmazza, vagy a csoportokat JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="08685-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="08685-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="08685-133">-ManagementGroupName</span></span>
<span data-ttu-id="08685-134">Az új házirendkészlet-definíció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="08685-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="08685-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="08685-135">-Metadata</span></span>
<span data-ttu-id="08685-136">A házirendkészlet-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="08685-136">The metadata for policy set definition.</span></span> <span data-ttu-id="08685-137">Ez lehet egy olyan fájlnév elérési útja, amely tartalmazza a metaadatokat vagy a metaadatokat JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="08685-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="08685-138">-Name</span><span class="sxs-lookup"><span data-stu-id="08685-138">-Name</span></span>
<span data-ttu-id="08685-139">A házirendkészlet definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="08685-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="08685-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="08685-140">-Parameter</span></span>
<span data-ttu-id="08685-141">A házirendkészlet-definíció paramétereinek deklarációja.</span><span class="sxs-lookup"><span data-stu-id="08685-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="08685-142">Ez lehet egy olyan fájlnév elérési útja, amely a paraméterdeklarációt tartalmazza, vagy a paraméterek deklarációja JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="08685-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="08685-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="08685-143">-PolicyDefinition</span></span>
<span data-ttu-id="08685-144">A házirend-definíciók.</span><span class="sxs-lookup"><span data-stu-id="08685-144">The policy definitions.</span></span> <span data-ttu-id="08685-145">Ez lehet egy olyan fájlnév elérési útja, amely tartalmazza a házirenddefiníciókat, vagy a házirenddefiníciókat JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="08685-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="08685-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="08685-146">-Pre</span></span>
<span data-ttu-id="08685-147">Ha be van állítva, az azt jelenti, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="08685-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="08685-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08685-148">-SubscriptionId</span></span>
<span data-ttu-id="08685-149">Az új házirendkészlet-definíció előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="08685-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="08685-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08685-150">-Confirm</span></span>
<span data-ttu-id="08685-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="08685-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08685-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08685-152">-WhatIf</span></span>
<span data-ttu-id="08685-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="08685-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08685-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08685-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08685-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08685-155">CommonParameters</span></span>
<span data-ttu-id="08685-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08685-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08685-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08685-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08685-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08685-158">INPUTS</span></span>

### <span data-ttu-id="08685-159">System.String</span><span class="sxs-lookup"><span data-stu-id="08685-159">System.String</span></span>

### <span data-ttu-id="08685-160">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08685-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="08685-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08685-161">OUTPUTS</span></span>

### <span data-ttu-id="08685-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="08685-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="08685-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="08685-163">NOTES</span></span>

## <span data-ttu-id="08685-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08685-164">RELATED LINKS</span></span>
