---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: d1e6b5b2b2e76c4ec807c27922f9ce577d94a7d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928937"
---
# <span data-ttu-id="b7d2a-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b7d2a-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="b7d2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d2a-103">Házirend-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="b7d2a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7d2a-104">SYNTAX</span></span>

### <span data-ttu-id="b7d2a-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7d2a-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7d2a-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7d2a-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7d2a-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7d2a-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7d2a-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7d2a-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7d2a-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7d2a-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7d2a-110">DESCRIPTION</span></span>
<span data-ttu-id="b7d2a-111">A **New-AzPolicyAssignment** parancsmag létrehoz egy házirend-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="b7d2a-112">Adjon meg egy házirendet és hatókört.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="b7d2a-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7d2a-113">EXAMPLES</span></span>

### <span data-ttu-id="b7d2a-114">1. példa: Házirend-hozzárendelés előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="b7d2a-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="b7d2a-115">Az első parancs egy Subscription01 nevű előfizetést kap a Get-AzSubscription parancsmag használatával, és tárolja azt a $Subscription változóban.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="b7d2a-116">A második parancs a virtualmachinePolicy nevű házirenddefiníciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b7d2a-117">Az utolsó parancs hozzárendeli a házirendet $Policy az előfizetés hatókörével azonosított szinten.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="b7d2a-118">2. példa: Házirend-hozzárendelés erőforráscsoport szintjén</span><span class="sxs-lookup"><span data-stu-id="b7d2a-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="b7d2a-119">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával, és tárolja azt a $ResourceGroup változóban.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b7d2a-120">A második parancs a virtualmachinePolicy nevű házirenddefiníciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b7d2a-121">Az utolsó parancs hozzárendeli a házirendet a $Policy erőforráscsoportnak  a házirend erőforrás-tulajdonsága által meghatározott $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="b7d2a-122">3. példa: Házirend-hozzárendelés erőforráscsoportszinten a házirend paraméterobjektumával</span><span class="sxs-lookup"><span data-stu-id="b7d2a-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="b7d2a-123">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="b7d2a-124">A parancs az objektumot a $ResourceGroup tárolja.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b7d2a-125">A második parancs az engedélyezett helyek beépített házirenddefinícióját kapja meg a Get-AzPolicyDefinition parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="b7d2a-126">A parancs az objektumot a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="b7d2a-127">A harmadik és a negyedik parancs egy olyan objektumot hoz létre, amely az összes Azure-régiót tartalmazza, és a nevében a "kelet" szó található.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="b7d2a-128">A parancsok az objektumot a $AllowedLocations tárolják.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="b7d2a-129">Az utolsó parancs hozzárendeli a házirendet $Policy egy erőforráscsoport szintjén, a házirend paraméterobjektumát használva a $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="b7d2a-130">A **$ResourceGroup ResourceId** tulajdonsága azonosítja az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="b7d2a-131">4. példa: Házirend-hozzárendelés erőforráscsoportszinten a házirend paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="b7d2a-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="b7d2a-132">Hozzon létre egyAllowedLocations.js _nevű_ fájlt a helyi munkakönyvtárban az alábbi tartalommal.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="b7d2a-133">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával, és tárolja azt a $ResourceGroup változóban.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b7d2a-134">A második parancs az engedélyezett helyek beépített házirenddefinícióját kapja meg a Get-AzPolicyDefinition parancsmag használatával, és tárolja azt a $Policy változóban.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b7d2a-135">A végleges parancs hozzárendeli a házirendet $Policy a $ResourceGroup **ResourceId** tulajdonságával azonosított erőforráscsoporthoz, és be van AllowedLocations.jsa helyi munkakönyvtárból.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="b7d2a-136">5. példa: Házirend-hozzárendelés felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="b7d2a-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="b7d2a-137">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával, és tárolja azt a $ResourceGroup változóban.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b7d2a-138">A második parancs a virtualmachinePolicy nevű házirenddefiníciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b7d2a-139">Az utolsó parancs hozzárendeli a házirendet $Policy erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="b7d2a-140">A rendszer automatikusan létrehoz egy felügyelt identitást, és hozzárendeli a házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="b7d2a-141">6. példa: Házirend-hozzárendelés kényszerítési mód tulajdonsággal</span><span class="sxs-lookup"><span data-stu-id="b7d2a-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="b7d2a-142">Az első parancs egy Subscription01 nevű előfizetést kap a Get-AzSubscription parancsmag használatával, és tárolja azt a $Subscription változóban.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="b7d2a-143">A második parancs a virtualmachinePolicy nevű házirenddefiníciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b7d2a-144">Az utolsó parancs hozzárendeli a házirendet $Policy az előfizetés hatókörével azonosított szinten.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="b7d2a-145">A hozzárendelés a _DoNotEnforce_ EnforcementMode értékével van beállítva, azaz a házirend-effektus nem lép érvénybe az erőforrás létrehozása vagy frissítése során.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="b7d2a-146">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7d2a-146">PARAMETERS</span></span>

### <span data-ttu-id="b7d2a-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b7d2a-147">-ApiVersion</span></span>
<span data-ttu-id="b7d2a-148">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b7d2a-149">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b7d2a-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b7d2a-150">-AssignIdentity</span></span>
<span data-ttu-id="b7d2a-151">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="b7d2a-152">Az identitást a "deployIfNotExists" házirendek telepítésének végrehajtásakor fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="b7d2a-153">Identitás hozzárendelésekor hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="b7d2a-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d2a-154">-DefaultProfile</span></span>
<span data-ttu-id="b7d2a-155">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b7d2a-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7d2a-156">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b7d2a-156">-Description</span></span>
<span data-ttu-id="b7d2a-157">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="b7d2a-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="b7d2a-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b7d2a-158">-DisplayName</span></span>
<span data-ttu-id="b7d2a-159">A házirend-hozzárendelés megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="b7d2a-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="b7d2a-160">-EnforcementMode</span></span>
<span data-ttu-id="b7d2a-161">A házirend-hozzárendelés kényszerítési módja.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="b7d2a-162">Jelenleg az érvényes értékek az Alapértelmezett, a DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-162">Currently, valid values are Default, DoNotEnforce.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d2a-163">-Location</span><span class="sxs-lookup"><span data-stu-id="b7d2a-163">-Location</span></span>
<span data-ttu-id="b7d2a-164">A házirend-hozzárendelés erőforrás-identitásának helye.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="b7d2a-165">Erre a -AssignIdentity kapcsoló használata esetén van szükség.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="b7d2a-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b7d2a-166">-Metadata</span></span>
<span data-ttu-id="b7d2a-167">Az új házirend-hozzárendelés metaadatai.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="b7d2a-168">Ez lehet egy olyan fájlnév elérési útja, amely tartalmazza a metaadatokat, vagy karakterláncként a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="b7d2a-169">-Name</span><span class="sxs-lookup"><span data-stu-id="b7d2a-169">-Name</span></span>
<span data-ttu-id="b7d2a-170">Megadja a házirend-hozzárendelés nevét.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="b7d2a-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="b7d2a-171">-NotScope</span></span>
<span data-ttu-id="b7d2a-172">A házirend-hozzárendelés hatóköre nem.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-172">The not scopes for policy assignment.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d2a-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b7d2a-173">-PolicyDefinition</span></span>
<span data-ttu-id="b7d2a-174">Egy házirendet ad meg a házirendszabályt tartalmazó **PsPolicyDefinition** objektumként.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d2a-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="b7d2a-175">-PolicyParameter</span></span>
<span data-ttu-id="b7d2a-176">A házirend paraméterének fájl elérési útja vagy a házirend paraméterének karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-176">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d2a-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="b7d2a-177">-PolicyParameterObject</span></span>
<span data-ttu-id="b7d2a-178">A házirend paraméterobjektuma.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-178">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d2a-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b7d2a-179">-PolicySetDefinition</span></span>
<span data-ttu-id="b7d2a-180">A házirendkészlet definíciós objektuma.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-180">The policy set definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d2a-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="b7d2a-181">-Pre</span></span>
<span data-ttu-id="b7d2a-182">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b7d2a-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="b7d2a-183">-Scope</span></span>
<span data-ttu-id="b7d2a-184">Megadja, hogy milyen hatókörben rendelje hozzá a házirendet.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="b7d2a-185">Ha például hozzá szeretne rendelni egy házirendet egy erőforráscsoporthoz, adja meg a következőt: `/subscriptions/` előfizetés-azonosító `/resourcegroups/` erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b7d2a-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="b7d2a-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d2a-186">CommonParameters</span></span>
<span data-ttu-id="b7d2a-187">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d2a-188">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d2a-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7d2a-189">INPUTS</span></span>

### <span data-ttu-id="b7d2a-190">System.String</span><span class="sxs-lookup"><span data-stu-id="b7d2a-190">System.String</span></span>

### <span data-ttu-id="b7d2a-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b7d2a-191">System.String[]</span></span>

### <span data-ttu-id="b7d2a-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b7d2a-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b7d2a-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7d2a-193">OUTPUTS</span></span>

### <span data-ttu-id="b7d2a-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b7d2a-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b7d2a-195">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7d2a-195">NOTES</span></span>

## <span data-ttu-id="b7d2a-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7d2a-196">RELATED LINKS</span></span>

[<span data-ttu-id="b7d2a-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b7d2a-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="b7d2a-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b7d2a-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="b7d2a-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b7d2a-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="b7d2a-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b7d2a-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


