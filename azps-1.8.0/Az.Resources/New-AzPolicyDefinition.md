---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 07882064fae3cfc4a24899b6106480551f3681a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669387"
---
# <span data-ttu-id="c7e72-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7e72-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="c7e72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7e72-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e72-103">Házirend-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c7e72-103">Creates a policy definition.</span></span>

## <span data-ttu-id="c7e72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7e72-104">SYNTAX</span></span>

### <span data-ttu-id="c7e72-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7e72-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7e72-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7e72-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7e72-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7e72-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7e72-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7e72-108">DESCRIPTION</span></span>
<span data-ttu-id="c7e72-109">A **New-AzPolicyDefinition** parancsmag olyan házirend-definíciót hoz létre, amely egy JavaScript-objektum formátumú (JSON) formátumú házirend-szabályt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="c7e72-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="c7e72-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c7e72-110">EXAMPLES</span></span>

### <span data-ttu-id="c7e72-111">Példa 1: házirend-definíció létrehozása házirendfájl használatával</span><span class="sxs-lookup"><span data-stu-id="c7e72-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="c7e72-112">Ez a parancs létrehoz egy LocationDefinition nevű házirend-definíciót, amely a C:\LocationPolicy.jsban megadott házirend-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c7e72-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="c7e72-113">A fenti LocationPolicy.jspéldául a fájlhoz tartozó tartalmakat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7e72-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="c7e72-114">2. példa: paraméteres házirend-definíció létrehozása szövegközi paraméterek használatával</span><span class="sxs-lookup"><span data-stu-id="c7e72-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="c7e72-115">Ez a parancs létrehoz egy LocationDefinition nevű házirend-definíciót, amely a C:\LocationPolicy.jsban megadott házirend-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c7e72-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="c7e72-116">A házirend-szabály paraméter-definíciója szövegközi módon van megadva.</span><span class="sxs-lookup"><span data-stu-id="c7e72-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="c7e72-117">3. példa: házirend-definíció létrehozása egy felügyeleti csoportban</span><span class="sxs-lookup"><span data-stu-id="c7e72-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="c7e72-118">Ez a parancs létrehoz egy VMPolicyDefinition nevű házirend-definíciót a felügyeleti csoport Dept42.</span><span class="sxs-lookup"><span data-stu-id="c7e72-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="c7e72-119">A parancs érvényes JSON formátumú karakterláncként adja meg a házirendet.</span><span class="sxs-lookup"><span data-stu-id="c7e72-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="c7e72-120">Példa 4: házirend-definíció létrehozása a metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="c7e72-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="c7e72-121">Ez a parancs létrehoz egy VMPolicyDefinition nevű házirend-definíciót, amelyben a kategóriája "virtuális gép".</span><span class="sxs-lookup"><span data-stu-id="c7e72-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="c7e72-122">A parancs érvényes JSON formátumú karakterláncként adja meg a házirendet.</span><span class="sxs-lookup"><span data-stu-id="c7e72-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="c7e72-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7e72-123">PARAMETERS</span></span>

### <span data-ttu-id="c7e72-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c7e72-124">-ApiVersion</span></span>
<span data-ttu-id="c7e72-125">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7e72-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c7e72-126">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c7e72-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c7e72-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e72-127">-DefaultProfile</span></span>
<span data-ttu-id="c7e72-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c7e72-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7e72-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c7e72-129">-Description</span></span>
<span data-ttu-id="c7e72-130">A házirend definíciójának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7e72-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="c7e72-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7e72-131">-DisplayName</span></span>
<span data-ttu-id="c7e72-132">A házirend-definíció megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7e72-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="c7e72-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c7e72-133">-ManagementGroupName</span></span>
<span data-ttu-id="c7e72-134">Az új házirend-definíció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="c7e72-134">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="c7e72-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c7e72-135">-Metadata</span></span>
<span data-ttu-id="c7e72-136">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="c7e72-136">The metadata for policy definition.</span></span> <span data-ttu-id="c7e72-137">Ez lehet a metaadatot tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c7e72-137">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="c7e72-138">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="c7e72-138">-Mode</span></span>
<span data-ttu-id="c7e72-139">A házirend-definíció módja</span><span class="sxs-lookup"><span data-stu-id="c7e72-139">The mode of the policy definition</span></span>

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

### <span data-ttu-id="c7e72-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7e72-140">-Name</span></span>
<span data-ttu-id="c7e72-141">A házirend-definíció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7e72-141">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="c7e72-142">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="c7e72-142">-Parameter</span></span>
<span data-ttu-id="c7e72-143">A Parameters deklaráció a házirend-definícióban.</span><span class="sxs-lookup"><span data-stu-id="c7e72-143">The parameters declaration for policy definition.</span></span> <span data-ttu-id="c7e72-144">Ez lehet a Parameters deklarációt vagy a Parameters deklarációt karakterláncként tartalmazó fájlnév elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c7e72-144">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="c7e72-145">-Házirend</span><span class="sxs-lookup"><span data-stu-id="c7e72-145">-Policy</span></span>
<span data-ttu-id="c7e72-146">A házirend-definíció szabályait adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7e72-146">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="c7e72-147">Megadhatja a. JSON fájlok elérési útját vagy a JSON formátumú házirendet tartalmazó karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="c7e72-147">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="c7e72-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="c7e72-148">-Pre</span></span>
<span data-ttu-id="c7e72-149">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c7e72-149">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c7e72-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7e72-150">-SubscriptionId</span></span>
<span data-ttu-id="c7e72-151">Az új házirend-definíció előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7e72-151">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="c7e72-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e72-152">CommonParameters</span></span>
<span data-ttu-id="c7e72-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7e72-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e72-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e72-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e72-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7e72-155">INPUTS</span></span>

### <span data-ttu-id="c7e72-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c7e72-156">System.String</span></span>

### <span data-ttu-id="c7e72-157">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c7e72-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c7e72-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7e72-158">OUTPUTS</span></span>

### <span data-ttu-id="c7e72-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c7e72-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c7e72-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7e72-160">NOTES</span></span>

## <span data-ttu-id="c7e72-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7e72-161">RELATED LINKS</span></span>

[<span data-ttu-id="c7e72-162">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7e72-162">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="c7e72-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7e72-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="c7e72-164">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7e72-164">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


