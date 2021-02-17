---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208462"
---
# <span data-ttu-id="e5976-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e5976-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="e5976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5976-102">SYNOPSIS</span></span>
<span data-ttu-id="e5976-103">Házirend-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e5976-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="e5976-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5976-104">SYNTAX</span></span>

### <span data-ttu-id="e5976-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5976-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5976-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5976-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5976-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5976-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5976-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5976-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5976-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5976-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5976-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5976-110">DESCRIPTION</span></span>
<span data-ttu-id="e5976-111">A **New-AzPolicyAssignment** parancsmag létrehoz egy házirend-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="e5976-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="e5976-112">Adjon meg egy házirendet és hatókört.</span><span class="sxs-lookup"><span data-stu-id="e5976-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="e5976-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5976-113">EXAMPLES</span></span>

### <span data-ttu-id="e5976-114">1. példa: Házirend-hozzárendelés előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="e5976-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="e5976-115">Az első parancs egy Subscription01 nevű előfizetést kap a Get-AzSubscription parancsmag használatával, és azt a $Subscription változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5976-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="e5976-116">A második parancs a VirtualMachinePolicy nevű házirenddefiníciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5976-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="e5976-117">Az utolsó parancs hozzárendeli a házirendet $Policy az előfizetés hatókörével azonosított szinten.</span><span class="sxs-lookup"><span data-stu-id="e5976-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="e5976-118">2. példa: Házirend-hozzárendelés erőforráscsoport szintjén</span><span class="sxs-lookup"><span data-stu-id="e5976-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="e5976-119">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával, és tárolja azt a $ResourceGroup változóban.</span><span class="sxs-lookup"><span data-stu-id="e5976-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e5976-120">A második parancs a VirtualMachinePolicy nevű házirenddefiníciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5976-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="e5976-121">Az utolsó parancs hozzárendeli a házirendet a $Policy erőforráscsoportnak  a házirend Erőforrásazonosító tulajdonsága által meghatározott $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e5976-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="e5976-122">3. példa: Házirend-hozzárendelés erőforráscsoportszinten a házirend paraméterobjektumával</span><span class="sxs-lookup"><span data-stu-id="e5976-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="e5976-123">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e5976-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e5976-124">A parancs az objektumot a $ResourceGroup tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5976-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e5976-125">A második parancs az engedélyezett helyek beépített házirenddefinícióját kapja meg a Get-AzPolicyDefinition parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e5976-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="e5976-126">A parancs az objektumot a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5976-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="e5976-127">A harmadik és a negyedik parancs egy olyan objektumot hoz létre, amely az összes Azure-régiót tartalmazza, és a nevében a "kelet" szó található.</span><span class="sxs-lookup"><span data-stu-id="e5976-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="e5976-128">A parancsok az objektumot a $AllowedLocations tárolják.</span><span class="sxs-lookup"><span data-stu-id="e5976-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="e5976-129">Az utolsó parancs hozzárendeli a házirendet $Policy egy erőforráscsoport szintjén, a házirend paraméterobjektumát használva a $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="e5976-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="e5976-130">A **$ResourceGroup ResourceId** tulajdonsága azonosítja az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="e5976-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="e5976-131">4. példa: Házirend-hozzárendelés erőforráscsoportszinten a házirend paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="e5976-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="e5976-132">Hozzon létre egy _AllowedLocations.jsnevű fájlt_ a helyi munkakönyvtárban az alábbi tartalommal.</span><span class="sxs-lookup"><span data-stu-id="e5976-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="e5976-133">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával, és tárolja azt a $ResourceGroup változóban.</span><span class="sxs-lookup"><span data-stu-id="e5976-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e5976-134">A második parancs az engedélyezett helyek beépített házirenddefinícióját kapja meg a Get-AzPolicyDefinition parancsmag használatával, és tárolja azt a $Policy változóban.</span><span class="sxs-lookup"><span data-stu-id="e5976-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="e5976-135">Az utolsó parancs hozzárendeli a házirendet $Policy a $ResourceGroup **ResourceId** tulajdonságával azonosított erőforráscsoporthoz, és be van AllowedLocations.jsa helyi munkakönyvtárból.</span><span class="sxs-lookup"><span data-stu-id="e5976-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="e5976-136">5. példa: Házirend-hozzárendelés felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="e5976-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="e5976-137">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával, és tárolja azt a $ResourceGroup változóban.</span><span class="sxs-lookup"><span data-stu-id="e5976-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e5976-138">A második parancs a VirtualMachinePolicy nevű házirenddefiníciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5976-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="e5976-139">Az utolsó parancs hozzárendeli a házirendet $Policy erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e5976-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="e5976-140">A rendszer automatikusan létrehoz egy felügyelt identitást, és hozzárendeli a házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="e5976-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="e5976-141">6. példa: Házirend-hozzárendelés kényszerítési mód tulajdonsággal</span><span class="sxs-lookup"><span data-stu-id="e5976-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="e5976-142">Az első parancs egy Subscription01 nevű előfizetést kap a Get-AzSubscription parancsmag használatával, és azt a $Subscription változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5976-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="e5976-143">A második parancs a VirtualMachinePolicy nevű házirenddefiníciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5976-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="e5976-144">Az utolsó parancs hozzárendeli a házirendet $Policy az előfizetés hatókörével azonosított szinten.</span><span class="sxs-lookup"><span data-stu-id="e5976-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="e5976-145">A hozzárendelés a _DoNotEnforce_ EnforcementMode értékével van beállítva, azaz a házirend-effektus nincs kényszerítve az erőforrás létrehozása vagy frissítése során.</span><span class="sxs-lookup"><span data-stu-id="e5976-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="e5976-146">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5976-146">PARAMETERS</span></span>

### <span data-ttu-id="e5976-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5976-147">-ApiVersion</span></span>
<span data-ttu-id="e5976-148">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5976-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e5976-149">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e5976-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e5976-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e5976-150">-AssignIdentity</span></span>
<span data-ttu-id="e5976-151">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="e5976-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="e5976-152">Az identitást a "deployIfNotExists" házirendek telepítésének végrehajtásakor fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="e5976-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="e5976-153">Identitás hozzárendelésekor hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="e5976-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="e5976-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5976-154">-DefaultProfile</span></span>
<span data-ttu-id="e5976-155">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5976-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5976-156">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e5976-156">-Description</span></span>
<span data-ttu-id="e5976-157">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="e5976-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="e5976-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5976-158">-DisplayName</span></span>
<span data-ttu-id="e5976-159">A házirend-hozzárendelés megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5976-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="e5976-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="e5976-160">-EnforcementMode</span></span>
<span data-ttu-id="e5976-161">A házirend-hozzárendelés kényszerítési módja.</span><span class="sxs-lookup"><span data-stu-id="e5976-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="e5976-162">Jelenleg az érvényes értékek az Alapértelmezett, a DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="e5976-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="e5976-163">-Location</span><span class="sxs-lookup"><span data-stu-id="e5976-163">-Location</span></span>
<span data-ttu-id="e5976-164">A házirend-hozzárendelés erőforrás-identitásának helye.</span><span class="sxs-lookup"><span data-stu-id="e5976-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="e5976-165">Erre a -AssignIdentity kapcsoló használata esetén van szükség.</span><span class="sxs-lookup"><span data-stu-id="e5976-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="e5976-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e5976-166">-Metadata</span></span>
<span data-ttu-id="e5976-167">Az új házirend-hozzárendelés metaadatai.</span><span class="sxs-lookup"><span data-stu-id="e5976-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="e5976-168">Ez lehet egy olyan fájlnév elérési útja, amely tartalmazza a metaadatokat, vagy karakterláncként a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="e5976-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="e5976-169">-Name</span><span class="sxs-lookup"><span data-stu-id="e5976-169">-Name</span></span>
<span data-ttu-id="e5976-170">Megadja a házirend-hozzárendelés nevét.</span><span class="sxs-lookup"><span data-stu-id="e5976-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="e5976-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="e5976-171">-NotScope</span></span>
<span data-ttu-id="e5976-172">A házirend-hozzárendelés hatóköre nem.</span><span class="sxs-lookup"><span data-stu-id="e5976-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="e5976-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5976-173">-PolicyDefinition</span></span>
<span data-ttu-id="e5976-174">Egy házirendet ad meg a házirendszabályt tartalmazó **PsPolicyDefinition** objektumként.</span><span class="sxs-lookup"><span data-stu-id="e5976-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="e5976-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="e5976-175">-PolicyParameter</span></span>
<span data-ttu-id="e5976-176">A házirend paraméterének fájl elérési útja vagy a házirend paraméterének karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="e5976-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="e5976-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5976-177">-PolicyParameterObject</span></span>
<span data-ttu-id="e5976-178">A házirend paraméterobjektuma.</span><span class="sxs-lookup"><span data-stu-id="e5976-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="e5976-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e5976-179">-PolicySetDefinition</span></span>
<span data-ttu-id="e5976-180">A házirendkészlet definíciós objektuma.</span><span class="sxs-lookup"><span data-stu-id="e5976-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="e5976-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="e5976-181">-Pre</span></span>
<span data-ttu-id="e5976-182">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="e5976-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e5976-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="e5976-183">-Scope</span></span>
<span data-ttu-id="e5976-184">Megadja, hogy milyen hatókörben rendelje hozzá a házirendet.</span><span class="sxs-lookup"><span data-stu-id="e5976-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="e5976-185">Ha például hozzá szeretne rendelni egy házirendet egy erőforráscsoporthoz, adja meg a következőt: `/subscriptions/` előfizetés-azonosító `/resourcegroups/` erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e5976-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="e5976-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5976-186">CommonParameters</span></span>
<span data-ttu-id="e5976-187">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5976-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5976-188">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5976-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5976-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5976-189">INPUTS</span></span>

### <span data-ttu-id="e5976-190">System.String</span><span class="sxs-lookup"><span data-stu-id="e5976-190">System.String</span></span>

### <span data-ttu-id="e5976-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e5976-191">System.String[]</span></span>

### <span data-ttu-id="e5976-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e5976-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e5976-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5976-193">OUTPUTS</span></span>

### <span data-ttu-id="e5976-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e5976-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e5976-195">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5976-195">NOTES</span></span>

## <span data-ttu-id="e5976-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5976-196">RELATED LINKS</span></span>

[<span data-ttu-id="e5976-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5976-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="e5976-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e5976-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="e5976-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e5976-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="e5976-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e5976-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


