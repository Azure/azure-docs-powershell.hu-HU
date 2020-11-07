---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: bec39b242de14da944496a4371fa661d95ce9c59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838920"
---
# <span data-ttu-id="1ad1c-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1ad1c-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="1ad1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ad1c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad1c-103">Házirend-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="1ad1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ad1c-104">SYNTAX</span></span>

### <span data-ttu-id="1ad1c-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ad1c-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ad1c-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad1c-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ad1c-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad1c-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ad1c-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad1c-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ad1c-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad1c-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ad1c-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ad1c-110">DESCRIPTION</span></span>
<span data-ttu-id="1ad1c-111">A **New-AzPolicyAssignment** parancsmag létrehoz egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="1ad1c-112">Adjon meg egy házirendet és egy hatókört.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="1ad1c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="1ad1c-113">EXAMPLES</span></span>

### <span data-ttu-id="1ad1c-114">1. példa: házirend-hozzárendelés az előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="1ad1c-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="1ad1c-115">Az első parancs a Subscription01 nevű előfizetést kapja meg az Get-AzSubscription parancsmag használatával, és a $Subscription változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="1ad1c-116">A második parancs a VirtualMachinePolicy nevű házirend-definíciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1ad1c-117">A végleges parancs a házirendet a $Policy az előfizetés hatóköre karakterlánc által azonosított előfizetéshez rendeli.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="1ad1c-118">2. példa: házirend-hozzárendelés az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="1ad1c-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="1ad1c-119">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1ad1c-120">A második parancs a VirtualMachinePolicy nevű házirend-definíciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1ad1c-121">A végleges parancs a házirendet a $ResourceGroup **ResourceId** tulajdonsága által azonosított erőforráscsoport szintjén rendeli $Policy.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="1ad1c-122">3. példa: házirend-hozzárendelés az erőforráscsoport szintjén a Policy paraméter-objektummal</span><span class="sxs-lookup"><span data-stu-id="1ad1c-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="1ad1c-123">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1ad1c-124">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1ad1c-125">A második parancs az engedélyezett helyek beépített házirend-definícióját az Get-AzPolicyDefinition parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="1ad1c-126">A parancs az objektumot a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="1ad1c-127">A harmadik és a negyedik parancs a nevében a "Kelet" nevű összes Azure-régiót tartalmazó objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="1ad1c-128">A parancsok az objektumot a $AllowedLocations változóban tárolják.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="1ad1c-129">A végleges parancs az $AllowedLocationsban a Policy paraméter objektummal az erőforráscsoport szintjén rendeli hozzá a házirendet a $Policyban.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="1ad1c-130">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="1ad1c-131">Példa 4: házirend-hozzárendelés az erőforráscsoport szintjén a házirend-paraméter fájllal</span><span class="sxs-lookup"><span data-stu-id="1ad1c-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="1ad1c-132">A következő tartalommal hozzon létre egy _AllowedLocations.js_ nevű fájlt a helyi munkakönyvtárban.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="1ad1c-133">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1ad1c-134">A második parancs beolvassa az engedélyezett helyek beépített házirend-definícióját az Get-AzPolicyDefinition parancsmag használatával, és a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1ad1c-135">A végleges parancs kiosztja a házirendet $Policy a $ResourceGroup **ResourceId** tulajdonság által meghatározott erőforráscsoport AllowedLocations.jsa helyi munkakönyvtárban a Policy paramétert tartalmazó fájllal.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="1ad1c-136">Példa 5: házirend-hozzárendelés felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="1ad1c-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="1ad1c-137">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1ad1c-138">A második parancs a VirtualMachinePolicy nevű házirend-definíciót a Get-AzPolicyDefinition parancsmag használatával kapja meg, és a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1ad1c-139">A végleges parancs a házirendet a $Policy az erőforráscsoport-csoportba rendeli.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="1ad1c-140">A rendszer automatikusan létrehoz egy felügyelt identitást, és hozzárendeli a házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="1ad1c-141">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ad1c-141">PARAMETERS</span></span>

### <span data-ttu-id="1ad1c-142">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1ad1c-142">-ApiVersion</span></span>
<span data-ttu-id="1ad1c-143">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-143">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1ad1c-144">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-144">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1ad1c-145">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1ad1c-145">-AssignIdentity</span></span>
<span data-ttu-id="1ad1c-146">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="1ad1c-146">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="1ad1c-147">Az identitás a "deployIfNotExists" házirendek telepítésének végrehajtásakor lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-147">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="1ad1c-148">Az identitás hozzárendelésekor a hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-148">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="1ad1c-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad1c-149">-DefaultProfile</span></span>
<span data-ttu-id="1ad1c-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1ad1c-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ad1c-151">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1ad1c-151">-Description</span></span>
<span data-ttu-id="1ad1c-152">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="1ad1c-152">The description for policy assignment</span></span>

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

### <span data-ttu-id="1ad1c-153">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1ad1c-153">-DisplayName</span></span>
<span data-ttu-id="1ad1c-154">A házirend-hozzárendelés megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-154">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="1ad1c-155">-Hely</span><span class="sxs-lookup"><span data-stu-id="1ad1c-155">-Location</span></span>
<span data-ttu-id="1ad1c-156">A házirend-hozzárendelés erőforrás-identitásának helye.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-156">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="1ad1c-157">Erre akkor van szükség, ha a-AssignIdentity kapcsolót használja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-157">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="1ad1c-158">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1ad1c-158">-Metadata</span></span>
<span data-ttu-id="1ad1c-159">Az új házirend-hozzárendelés metaadatai.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-159">The metadata for the new policy assignment.</span></span> <span data-ttu-id="1ad1c-160">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-160">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="1ad1c-161">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ad1c-161">-Name</span></span>
<span data-ttu-id="1ad1c-162">A házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-162">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="1ad1c-163">-NotScope</span><span class="sxs-lookup"><span data-stu-id="1ad1c-163">-NotScope</span></span>
<span data-ttu-id="1ad1c-164">A házirend-hozzárendeléshez nem tartozó hatókörök</span><span class="sxs-lookup"><span data-stu-id="1ad1c-164">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="1ad1c-165">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1ad1c-165">-PolicyDefinition</span></span>
<span data-ttu-id="1ad1c-166">A házirendet adja meg **PsPolicyDefinition** -objektumként, amely a házirend-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-166">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad1c-167">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="1ad1c-167">-PolicyParameter</span></span>
<span data-ttu-id="1ad1c-168">A házirend paraméterének fájlelérési útja vagy a házirend paraméterének karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-168">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="1ad1c-169">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="1ad1c-169">-PolicyParameterObject</span></span>
<span data-ttu-id="1ad1c-170">A Policy paraméter objektuma.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-170">The policy parameter object.</span></span>

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

### <span data-ttu-id="1ad1c-171">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1ad1c-171">-PolicySetDefinition</span></span>
<span data-ttu-id="1ad1c-172">A Policy set definition objektum.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-172">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad1c-173">-Pre</span><span class="sxs-lookup"><span data-stu-id="1ad1c-173">-Pre</span></span>
<span data-ttu-id="1ad1c-174">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-174">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1ad1c-175">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="1ad1c-175">-Scope</span></span>
<span data-ttu-id="1ad1c-176">A házirend hozzárendelésének hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-176">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="1ad1c-177">Ha például egy erőforrás-csoporthoz szeretne házirendet rendelni, adja meg a következőt: `/subscriptions/` előfizetés azonosítója `/resourcegroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="1ad1c-177">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="1ad1c-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad1c-178">CommonParameters</span></span>
<span data-ttu-id="1ad1c-179">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ad1c-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad1c-180">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-180">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad1c-181">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ad1c-181">INPUTS</span></span>

### <span data-ttu-id="1ad1c-182">System. String</span><span class="sxs-lookup"><span data-stu-id="1ad1c-182">System.String</span></span>

### <span data-ttu-id="1ad1c-183">System. string []</span><span class="sxs-lookup"><span data-stu-id="1ad1c-183">System.String[]</span></span>

### <span data-ttu-id="1ad1c-184">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1ad1c-184">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1ad1c-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ad1c-185">OUTPUTS</span></span>

### <span data-ttu-id="1ad1c-186">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1ad1c-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1ad1c-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ad1c-187">NOTES</span></span>

## <span data-ttu-id="1ad1c-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ad1c-188">RELATED LINKS</span></span>

[<span data-ttu-id="1ad1c-189">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1ad1c-189">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="1ad1c-190">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1ad1c-190">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="1ad1c-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1ad1c-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="1ad1c-192">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1ad1c-192">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


