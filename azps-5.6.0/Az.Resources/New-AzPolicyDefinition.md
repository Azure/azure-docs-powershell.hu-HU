---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 259b0abd120fb27eee1ca80da61266f4c890423f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928913"
---
# <span data-ttu-id="19279-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19279-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="19279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19279-102">SYNOPSIS</span></span>
<span data-ttu-id="19279-103">Házirenddefiníciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="19279-103">Creates a policy definition.</span></span>

## <span data-ttu-id="19279-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19279-104">SYNTAX</span></span>

### <span data-ttu-id="19279-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19279-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19279-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19279-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19279-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19279-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19279-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19279-108">DESCRIPTION</span></span>
<span data-ttu-id="19279-109">A **New-AzPolicyDefinition** parancsmag létrehoz egy olyan házirend-definíciót, amely tartalmaz egy házirendszabályt JavaScript objektum-notation (JSON) formátumban.</span><span class="sxs-lookup"><span data-stu-id="19279-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="19279-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19279-110">EXAMPLES</span></span>

### <span data-ttu-id="19279-111">1. példa: Házirenddefiníció létrehozása házirendfájl használatával</span><span class="sxs-lookup"><span data-stu-id="19279-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="19279-112">Ez a parancs létrehoz egy LocationDefinition nevű házirend-definíciót, amely tartalmazza a C:\LocationPolicy.jsházirendszabályt.</span><span class="sxs-lookup"><span data-stu-id="19279-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="19279-113">A fájlon LocationPolicy.jstartalom a fenti.</span><span class="sxs-lookup"><span data-stu-id="19279-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="19279-114">2. példa: Paraméteres házirenddefiníció létrehozása beágyazott paraméterek használatával</span><span class="sxs-lookup"><span data-stu-id="19279-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="19279-115">Ez a parancs létrehoz egy LocationDefinition nevű házirend-definíciót, amely tartalmazza a C:\LocationPolicy.jsházirendszabályt.</span><span class="sxs-lookup"><span data-stu-id="19279-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="19279-116">A házirendszabály paraméterdefiníciója beágyazott.</span><span class="sxs-lookup"><span data-stu-id="19279-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="19279-117">3. példa: Házirenddefiníció létrehozása egy felügyeleti csoportban beágyazottan</span><span class="sxs-lookup"><span data-stu-id="19279-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="19279-118">Ez a parancs létrehoz egy VMPolicyDefinition nevű házirend-definíciót a Dept42 felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="19279-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="19279-119">A parancs érvényes JSON formátumú karakterláncként adja meg a házirendet.</span><span class="sxs-lookup"><span data-stu-id="19279-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="19279-120">4. példa: Házirenddefiníció létrehozása metaadatokkal egy vonalban</span><span class="sxs-lookup"><span data-stu-id="19279-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="19279-121">Ez a parancs létrehoz egy VMPolicyDefinition nevű házirenddefiníciót metaadatokkal, jelezve, hogy a kategória "Virtuális gép".</span><span class="sxs-lookup"><span data-stu-id="19279-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="19279-122">A parancs érvényes JSON formátumú karakterláncként adja meg a házirendet.</span><span class="sxs-lookup"><span data-stu-id="19279-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="19279-123">5. példa: Házirenddefiníció létrehozása a móddal egy vonalban</span><span class="sxs-lookup"><span data-stu-id="19279-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="19279-124">Ez a parancs létrehoz egy TagsPolicyDefinition nevű házirenddefiníciót "Indexelt" módban, jelezve, hogy a házirendet csak a címkéket és a helyet támogató erőforrástípusok esetén kell kiértékelni.</span><span class="sxs-lookup"><span data-stu-id="19279-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="19279-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19279-125">PARAMETERS</span></span>

### <span data-ttu-id="19279-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="19279-126">-ApiVersion</span></span>
<span data-ttu-id="19279-127">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19279-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="19279-128">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="19279-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="19279-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19279-129">-DefaultProfile</span></span>
<span data-ttu-id="19279-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19279-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19279-131">-Leírás</span><span class="sxs-lookup"><span data-stu-id="19279-131">-Description</span></span>
<span data-ttu-id="19279-132">Megadja a házirenddefiníció leírását.</span><span class="sxs-lookup"><span data-stu-id="19279-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="19279-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="19279-133">-DisplayName</span></span>
<span data-ttu-id="19279-134">A házirend-definíció megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19279-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="19279-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="19279-135">-ManagementGroupName</span></span>
<span data-ttu-id="19279-136">Az új házirend-definíció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="19279-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="19279-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="19279-137">-Metadata</span></span>
<span data-ttu-id="19279-138">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="19279-138">The metadata for policy definition.</span></span> <span data-ttu-id="19279-139">Ez lehet egy olyan fájlnév elérési útja, amely a metaadatokat tartalmazza, vagy a metaadatok karakterláncként</span><span class="sxs-lookup"><span data-stu-id="19279-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="19279-140">-Mód</span><span class="sxs-lookup"><span data-stu-id="19279-140">-Mode</span></span>
<span data-ttu-id="19279-141">A házirenddefiníció módja</span><span class="sxs-lookup"><span data-stu-id="19279-141">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19279-142">-Name</span><span class="sxs-lookup"><span data-stu-id="19279-142">-Name</span></span>
<span data-ttu-id="19279-143">Megadja a házirenddefiníció nevét.</span><span class="sxs-lookup"><span data-stu-id="19279-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="19279-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="19279-144">-Parameter</span></span>
<span data-ttu-id="19279-145">A házirenddefiníció paramétereinek deklarációja.</span><span class="sxs-lookup"><span data-stu-id="19279-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="19279-146">Ez lehet egy olyan fájlnév elérési útja, amely a paraméterdeklarációt tartalmazza, vagy a paraméterek deklarációja karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="19279-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="19279-147">-Házirend</span><span class="sxs-lookup"><span data-stu-id="19279-147">-Policy</span></span>
<span data-ttu-id="19279-148">Házirendszabályt ad meg a házirend-definícióhoz.</span><span class="sxs-lookup"><span data-stu-id="19279-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="19279-149">Megadhatja a házirendet JSON formátumban tartalmazó .json fájl vagy karakterlánc elérési útját.</span><span class="sxs-lookup"><span data-stu-id="19279-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="19279-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="19279-150">-Pre</span></span>
<span data-ttu-id="19279-151">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="19279-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="19279-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19279-152">-SubscriptionId</span></span>
<span data-ttu-id="19279-153">Az új házirend-definíció előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="19279-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="19279-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19279-154">CommonParameters</span></span>
<span data-ttu-id="19279-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19279-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19279-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19279-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19279-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19279-157">INPUTS</span></span>

### <span data-ttu-id="19279-158">System.String</span><span class="sxs-lookup"><span data-stu-id="19279-158">System.String</span></span>

### <span data-ttu-id="19279-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="19279-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="19279-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19279-160">OUTPUTS</span></span>

### <span data-ttu-id="19279-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="19279-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="19279-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19279-162">NOTES</span></span>

## <span data-ttu-id="19279-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19279-163">RELATED LINKS</span></span>

[<span data-ttu-id="19279-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19279-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="19279-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19279-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="19279-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19279-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


