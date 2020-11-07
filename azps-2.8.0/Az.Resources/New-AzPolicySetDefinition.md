---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 838fe6f4ed7ff1e69a6bdf99a8816f00fc0ab019
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838918"
---
# <span data-ttu-id="87635-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="87635-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="87635-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87635-102">SYNOPSIS</span></span>
<span data-ttu-id="87635-103">Házirend-készlet definícióját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="87635-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="87635-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87635-104">SYNTAX</span></span>

### <span data-ttu-id="87635-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87635-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87635-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="87635-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87635-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87635-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87635-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="87635-108">DESCRIPTION</span></span>
<span data-ttu-id="87635-109">A **New-AzPolicySetDefinition** parancsmag létrehoz egy házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="87635-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="87635-110">Példák</span><span class="sxs-lookup"><span data-stu-id="87635-110">EXAMPLES</span></span>

### <span data-ttu-id="87635-111">1. példa: házirend-készlet definíciójának létrehozása a metaadatokkal egy házirendfájl használatával</span><span class="sxs-lookup"><span data-stu-id="87635-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="87635-112">Ez a parancs létrehoz egy VMPolicySetDefinition nevű házirend-definíciós definíciót, amely azt jelzi, hogy a kategóriája a "virtuális gép", amely a C:\VMPolicy.jsban megadott házirend-definíciókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="87635-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="87635-113">Példa: a fenti VMPolicy.jstartalma.</span><span class="sxs-lookup"><span data-stu-id="87635-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="87635-114">2. példa: paraméteres házirend-készlet definíciójának létrehozása</span><span class="sxs-lookup"><span data-stu-id="87635-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="87635-115">Ez a parancs létrehoz egy VMPolicySetDefinition nevű, paraméteres házirend-definíciós definíciót, amely a C:\VMPolicy.jsban megadott házirend-definíciókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="87635-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="87635-116">Példa: a fenti VMPolicy.jstartalma.</span><span class="sxs-lookup"><span data-stu-id="87635-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="87635-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87635-117">PARAMETERS</span></span>

### <span data-ttu-id="87635-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="87635-118">-ApiVersion</span></span>
<span data-ttu-id="87635-119">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="87635-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="87635-120">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="87635-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="87635-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87635-121">-DefaultProfile</span></span>
<span data-ttu-id="87635-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="87635-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87635-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="87635-123">-Description</span></span>
<span data-ttu-id="87635-124">A házirend-készlet definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="87635-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="87635-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="87635-125">-DisplayName</span></span>
<span data-ttu-id="87635-126">A házirend-készlet definíciójának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="87635-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="87635-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="87635-127">-ManagementGroupName</span></span>
<span data-ttu-id="87635-128">Az új házirend-definíciós csoport felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="87635-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="87635-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="87635-129">-Metadata</span></span>
<span data-ttu-id="87635-130">A házirend-készlet definíciójának metaadatai.</span><span class="sxs-lookup"><span data-stu-id="87635-130">The metadata for policy set definition.</span></span> <span data-ttu-id="87635-131">Ez lehet a metaadatot tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="87635-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="87635-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87635-132">-Name</span></span>
<span data-ttu-id="87635-133">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="87635-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="87635-134">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="87635-134">-Parameter</span></span>
<span data-ttu-id="87635-135">A Parameters deklaráció a házirend-készlet definíciójában.</span><span class="sxs-lookup"><span data-stu-id="87635-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="87635-136">Ez lehet a Parameters deklarációt vagy a Parameters deklarációt karakterláncként tartalmazó fájlnév elérési útja.</span><span class="sxs-lookup"><span data-stu-id="87635-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="87635-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="87635-137">-PolicyDefinition</span></span>
<span data-ttu-id="87635-138">A házirend-definíciók.</span><span class="sxs-lookup"><span data-stu-id="87635-138">The policy definitions.</span></span> <span data-ttu-id="87635-139">Ez lehet a házirend-definíciókat tartalmazó fájlnév vagy a házirend-definíciók karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="87635-139">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="87635-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="87635-140">-Pre</span></span>
<span data-ttu-id="87635-141">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="87635-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="87635-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87635-142">-SubscriptionId</span></span>
<span data-ttu-id="87635-143">Az új házirend-készlet definíciójának előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87635-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="87635-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87635-144">-Confirm</span></span>
<span data-ttu-id="87635-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87635-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87635-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87635-146">-WhatIf</span></span>
<span data-ttu-id="87635-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87635-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87635-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87635-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87635-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87635-149">CommonParameters</span></span>
<span data-ttu-id="87635-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87635-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87635-151">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="87635-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87635-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87635-152">INPUTS</span></span>

### <span data-ttu-id="87635-153">System. String</span><span class="sxs-lookup"><span data-stu-id="87635-153">System.String</span></span>

### <span data-ttu-id="87635-154">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="87635-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="87635-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87635-155">OUTPUTS</span></span>

### <span data-ttu-id="87635-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="87635-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="87635-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87635-157">NOTES</span></span>

## <span data-ttu-id="87635-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87635-158">RELATED LINKS</span></span>
