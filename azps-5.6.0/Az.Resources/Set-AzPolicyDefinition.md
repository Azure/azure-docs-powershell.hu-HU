---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: ee3f1ffdb7e95e3c00b30238bf6d35833d99cea6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011749"
---
# <span data-ttu-id="5a4f6-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5a4f6-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="5a4f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4f6-103">Módosítja a házirenddefiníciót.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="5a4f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a4f6-104">SYNTAX</span></span>

### <span data-ttu-id="5a4f6-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a4f6-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a4f6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a4f6-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a4f6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a4f6-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a4f6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a4f6-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a4f6-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a4f6-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a4f6-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a4f6-110">DESCRIPTION</span></span>
<span data-ttu-id="5a4f6-111">A **Set-AzPolicyDefinition** parancsmag módosítja a házirenddefiníciót.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="5a4f6-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a4f6-112">EXAMPLES</span></span>

### <span data-ttu-id="5a4f6-113">1. példa: Házirenddefiníció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="5a4f6-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="5a4f6-114">Az első parancs egy VMPolicyDefinition nevű házirenddefiníciót kap a Get-AzPolicyDefinition parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="5a4f6-115">A parancs az objektumot a $PolicyDefinition tárolja.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="5a4f6-116">A második parancs frissíti a házirenddefiníció leírását, amelyet a rendszer **ResourceId** tulajdonsága $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="5a4f6-117">2. példa: Házirend-definíció módjának frissítése</span><span class="sxs-lookup"><span data-stu-id="5a4f6-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="5a4f6-118">Ez a parancs frissíti a VMPolicyDefinition nevű házirenddefiníciót úgy, hogy a Set-AzPolicyDefinition parancsmag használatával a módtulajdonságot "Mind" módra adja.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="5a4f6-119">3. példa: Házirend-definíció metaadatainak frissítése</span><span class="sxs-lookup"><span data-stu-id="5a4f6-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="5a4f6-120">Ez a parancs frissíti a VMPolicyDefinition nevű házirenddefiníció metaadatait, jelezve, hogy a kategória "Virtuális gép".</span><span class="sxs-lookup"><span data-stu-id="5a4f6-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="5a4f6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a4f6-121">PARAMETERS</span></span>

### <span data-ttu-id="5a4f6-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5a4f6-122">-ApiVersion</span></span>
<span data-ttu-id="5a4f6-123">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5a4f6-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5a4f6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4f6-125">-DefaultProfile</span></span>
<span data-ttu-id="5a4f6-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5a4f6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a4f6-127">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5a4f6-127">-Description</span></span>
<span data-ttu-id="5a4f6-128">A házirend-definíció új leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="5a4f6-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a4f6-129">-DisplayName</span></span>
<span data-ttu-id="5a4f6-130">A házirend-definíció új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="5a4f6-131">-Id</span><span class="sxs-lookup"><span data-stu-id="5a4f6-131">-Id</span></span>
<span data-ttu-id="5a4f6-132">A parancsmag által módosított házirenddefiníció teljes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5a4f6-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a4f6-133">-InputObject</span></span>
<span data-ttu-id="5a4f6-134">Az a házirend-definíciós objektum, amely egy másik parancsmagból lett kimenetként frissítve.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f6-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4f6-135">-ManagementGroupName</span></span>
<span data-ttu-id="5a4f6-136">A frissítenie kell a házirenddefiníció felügyeleti csoportjának nevét.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="5a4f6-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5a4f6-137">-Metadata</span></span>
<span data-ttu-id="5a4f6-138">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-138">The metadata for policy definition.</span></span> <span data-ttu-id="5a4f6-139">Ez lehet egy olyan fájlnév elérési útja, amely tartalmazza a metaadatokat, vagy karakterláncként a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="5a4f6-140">-Mód</span><span class="sxs-lookup"><span data-stu-id="5a4f6-140">-Mode</span></span>
<span data-ttu-id="5a4f6-141">Az új házirend-definíció módja.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="5a4f6-142">-Name</span><span class="sxs-lookup"><span data-stu-id="5a4f6-142">-Name</span></span>
<span data-ttu-id="5a4f6-143">A parancsmag által módosított házirenddefiníció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5a4f6-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="5a4f6-144">-Parameter</span></span>
<span data-ttu-id="5a4f6-145">A házirenddefiníció paramétereinek deklarációja.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="5a4f6-146">Ez lehet egy olyan fájlnév vagy uri elérési útja, amely a paraméterdeklarációt tartalmazza, vagy a paraméterek deklarációja karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="5a4f6-147">-Házirend</span><span class="sxs-lookup"><span data-stu-id="5a4f6-147">-Policy</span></span>
<span data-ttu-id="5a4f6-148">Új házirendszabályt ad meg a házirend-definícióhoz.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="5a4f6-149">Megadhatja egy .json fájl vagy egy olyan karakterlánc elérési útját, amely JavaScript objektum-notation (JSON) formátumban tartalmazza a házirendet.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="5a4f6-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="5a4f6-150">-Pre</span></span>
<span data-ttu-id="5a4f6-151">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5a4f6-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a4f6-152">-SubscriptionId</span></span>
<span data-ttu-id="5a4f6-153">A frissíteni szükséges házirend-definíció előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="5a4f6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4f6-154">CommonParameters</span></span>
<span data-ttu-id="5a4f6-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a4f6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4f6-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a4f6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4f6-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a4f6-157">INPUTS</span></span>

### <span data-ttu-id="5a4f6-158">System.String</span><span class="sxs-lookup"><span data-stu-id="5a4f6-158">System.String</span></span>

### <span data-ttu-id="5a4f6-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5a4f6-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5a4f6-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a4f6-160">OUTPUTS</span></span>

### <span data-ttu-id="5a4f6-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="5a4f6-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5a4f6-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a4f6-162">NOTES</span></span>

## <span data-ttu-id="5a4f6-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a4f6-163">RELATED LINKS</span></span>

[<span data-ttu-id="5a4f6-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5a4f6-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="5a4f6-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5a4f6-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="5a4f6-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5a4f6-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


