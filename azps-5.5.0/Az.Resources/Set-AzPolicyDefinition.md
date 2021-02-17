---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159947"
---
# <span data-ttu-id="8dd89-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8dd89-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="8dd89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dd89-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd89-103">Módosítja a házirenddefiníciót.</span><span class="sxs-lookup"><span data-stu-id="8dd89-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="8dd89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8dd89-104">SYNTAX</span></span>

### <span data-ttu-id="8dd89-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8dd89-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd89-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd89-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd89-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd89-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd89-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd89-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd89-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd89-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dd89-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8dd89-110">DESCRIPTION</span></span>
<span data-ttu-id="8dd89-111">A **Set-AzPolicyDefinition** parancsmag módosítja a házirenddefiníciót.</span><span class="sxs-lookup"><span data-stu-id="8dd89-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="8dd89-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8dd89-112">EXAMPLES</span></span>

### <span data-ttu-id="8dd89-113">1. példa: Házirenddefiníció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="8dd89-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="8dd89-114">Az első parancs egy VMPolicyDefinition nevű házirend-definíciót kap a Get-AzPolicyDefinition parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8dd89-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="8dd89-115">A parancs az objektumot a $PolicyDefinition tárolja.</span><span class="sxs-lookup"><span data-stu-id="8dd89-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="8dd89-116">A második parancs frissíti a házirenddefiníció leírását, amelyet a rendszer **ResourceId** tulajdonsága $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="8dd89-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="8dd89-117">2. példa: Házirenddefiníció módjának frissítése</span><span class="sxs-lookup"><span data-stu-id="8dd89-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="8dd89-118">Ez a parancs frissíti a VMPolicyDefinition nevű házirenddefiníciót a Set-AzPolicyDefinition parancsmag használatával a módtulajdonság "Mind" beállítására.</span><span class="sxs-lookup"><span data-stu-id="8dd89-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="8dd89-119">3. példa: Házirend-definíció metaadatainak frissítése</span><span class="sxs-lookup"><span data-stu-id="8dd89-119">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="8dd89-120">Ez a parancs frissíti a VMPolicyDefinition nevű házirenddefiníció metaadatait, jelezve, hogy a kategória "Virtuális gép".</span><span class="sxs-lookup"><span data-stu-id="8dd89-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="8dd89-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dd89-121">PARAMETERS</span></span>

### <span data-ttu-id="8dd89-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8dd89-122">-ApiVersion</span></span>
<span data-ttu-id="8dd89-123">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8dd89-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8dd89-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8dd89-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8dd89-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd89-125">-DefaultProfile</span></span>
<span data-ttu-id="8dd89-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8dd89-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dd89-127">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8dd89-127">-Description</span></span>
<span data-ttu-id="8dd89-128">A házirend-definíció új leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8dd89-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="8dd89-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8dd89-129">-DisplayName</span></span>
<span data-ttu-id="8dd89-130">A házirend-definíció új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8dd89-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="8dd89-131">-Id</span><span class="sxs-lookup"><span data-stu-id="8dd89-131">-Id</span></span>
<span data-ttu-id="8dd89-132">A parancsmag által módosított házirenddefiníció teljes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8dd89-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8dd89-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dd89-133">-InputObject</span></span>
<span data-ttu-id="8dd89-134">Az a házirend-definíciós objektum, amely egy másik parancsmagból lett kimenetként frissítve.</span><span class="sxs-lookup"><span data-stu-id="8dd89-134">The policy definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="8dd89-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd89-135">-ManagementGroupName</span></span>
<span data-ttu-id="8dd89-136">A frissítenie kell a házirenddefiníció felügyeleti csoportjának nevét.</span><span class="sxs-lookup"><span data-stu-id="8dd89-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="8dd89-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8dd89-137">-Metadata</span></span>
<span data-ttu-id="8dd89-138">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="8dd89-138">The metadata for policy definition.</span></span> <span data-ttu-id="8dd89-139">Ez lehet egy olyan fájlnév elérési útja, amely tartalmazza a metaadatokat, vagy karakterláncként a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="8dd89-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="8dd89-140">-Mód</span><span class="sxs-lookup"><span data-stu-id="8dd89-140">-Mode</span></span>
<span data-ttu-id="8dd89-141">Az új házirenddefiníció módja.</span><span class="sxs-lookup"><span data-stu-id="8dd89-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="8dd89-142">-Name</span><span class="sxs-lookup"><span data-stu-id="8dd89-142">-Name</span></span>
<span data-ttu-id="8dd89-143">A parancsmag által módosított házirenddefiníció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8dd89-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8dd89-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8dd89-144">-Parameter</span></span>
<span data-ttu-id="8dd89-145">A házirenddefiníció paramétereinek deklarációja.</span><span class="sxs-lookup"><span data-stu-id="8dd89-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="8dd89-146">Ez lehet egy olyan fájlnév vagy uri elérési útja, amely a paraméterdeklarációt tartalmazza, vagy a paraméterek deklarációja karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="8dd89-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="8dd89-147">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8dd89-147">-Policy</span></span>
<span data-ttu-id="8dd89-148">Új házirendszabályt ad meg a házirend-definícióhoz.</span><span class="sxs-lookup"><span data-stu-id="8dd89-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="8dd89-149">Megadhatja egy .json fájl vagy egy olyan karakterlánc elérési útját, amely JavaScript objektum-notation (JSON) formátumban tartalmazza a házirendet.</span><span class="sxs-lookup"><span data-stu-id="8dd89-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="8dd89-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="8dd89-150">-Pre</span></span>
<span data-ttu-id="8dd89-151">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="8dd89-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8dd89-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8dd89-152">-SubscriptionId</span></span>
<span data-ttu-id="8dd89-153">A frissíteni szükséges házirend-definíció előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="8dd89-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="8dd89-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd89-154">CommonParameters</span></span>
<span data-ttu-id="8dd89-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd89-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd89-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dd89-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd89-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8dd89-157">INPUTS</span></span>

### <span data-ttu-id="8dd89-158">System.String</span><span class="sxs-lookup"><span data-stu-id="8dd89-158">System.String</span></span>

### <span data-ttu-id="8dd89-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8dd89-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8dd89-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8dd89-160">OUTPUTS</span></span>

### <span data-ttu-id="8dd89-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8dd89-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8dd89-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8dd89-162">NOTES</span></span>

## <span data-ttu-id="8dd89-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8dd89-163">RELATED LINKS</span></span>

[<span data-ttu-id="8dd89-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8dd89-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="8dd89-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8dd89-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="8dd89-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8dd89-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


