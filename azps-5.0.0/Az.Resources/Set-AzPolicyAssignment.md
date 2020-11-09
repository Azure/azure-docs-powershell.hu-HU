---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300983"
---
# <span data-ttu-id="33414-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="33414-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="33414-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33414-102">SYNOPSIS</span></span>
<span data-ttu-id="33414-103">Házirend-hozzárendelés módosítása</span><span class="sxs-lookup"><span data-stu-id="33414-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="33414-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33414-104">SYNTAX</span></span>

### <span data-ttu-id="33414-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33414-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33414-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33414-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33414-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="33414-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33414-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33414-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33414-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33414-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33414-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="33414-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33414-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33414-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33414-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="33414-112">DESCRIPTION</span></span>
<span data-ttu-id="33414-113">A **set-AzPolicyAssignment** parancsmag módosította egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="33414-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="33414-114">Adjon meg egy hozzárendelést azonosító alapján vagy név és hatókör szerint.</span><span class="sxs-lookup"><span data-stu-id="33414-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="33414-115">Példák</span><span class="sxs-lookup"><span data-stu-id="33414-115">EXAMPLES</span></span>

### <span data-ttu-id="33414-116">Példa 1: a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="33414-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="33414-117">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="33414-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="33414-118">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="33414-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="33414-119">A második parancs az Get-AzPolicyAssignment parancsmag használatával kapja meg a PolicyAssignment nevű házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="33414-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="33414-120">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="33414-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="33414-121">A végleges parancs frissíti a megjelenítendő nevet az $ResourceGroup **ResourceId** tulajdonsága által azonosított erőforráscsoport házirend-hozzárendelésében.</span><span class="sxs-lookup"><span data-stu-id="33414-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="33414-122">2. példa: felügyelt identitás hozzáadása a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="33414-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="33414-123">Az első parancs a PolicyAssignment nevű házirend-hozzárendelést az aktuális előfizetésből az Get-AzPolicyAssignment parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="33414-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="33414-124">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="33414-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="33414-125">A végleges parancs a felügyelt identitást a házirend-hozzárendeléshez rendeli.</span><span class="sxs-lookup"><span data-stu-id="33414-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="33414-126">3. példa: házirend-hozzárendelési paraméterek frissítése új házirend-paraméteres objektummal</span><span class="sxs-lookup"><span data-stu-id="33414-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="33414-127">Az első és a második parancs az összes Azure-régiót tartalmazó objektumot hoz létre, amelynek a nevei a "Franciaország" vagy az "Egyesült Királyság" betűvel kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="33414-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="33414-128">A második parancs az objektumot a $AllowedLocations változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="33414-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="33414-129">A harmadik parancs a "PolicyAssignment" nevű házirend-hozzárendelést kapja meg, a parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="33414-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="33414-130">A végleges parancs frissíti a PolicyAssignment nevű házirend-hozzárendelés paramétereinek értékeit.</span><span class="sxs-lookup"><span data-stu-id="33414-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="33414-131">Példa 4: házirend-hozzárendelési paraméterek frissítése házirend-paraméteres fájllal</span><span class="sxs-lookup"><span data-stu-id="33414-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="33414-132">A következő tartalommal hozzon létre egy _AllowedLocations.js_ nevű fájlt a helyi munkakönyvtárban.</span><span class="sxs-lookup"><span data-stu-id="33414-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="33414-133">A parancs frissíti a "PolicyAssignment" nevű házirend-hozzárendelést a helyi munkakönyvtárból AllowedLocations.jsházirend-paraméter fájljában.</span><span class="sxs-lookup"><span data-stu-id="33414-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="33414-134">Példa 5: enforcementMode frissítése</span><span class="sxs-lookup"><span data-stu-id="33414-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="33414-135">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="33414-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="33414-136">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="33414-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="33414-137">A második parancs az Get-AzPolicyAssignment parancsmag használatával kapja meg a PolicyAssignment nevű házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="33414-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="33414-138">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="33414-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="33414-139">A végleges parancs frissíti a enforcementMode tulajdonságot az $ResourceGroup **ResourceId** tulajdonsága által azonosított erőforráscsoport házirend-hozzárendeléseiben.</span><span class="sxs-lookup"><span data-stu-id="33414-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="33414-140">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33414-140">PARAMETERS</span></span>

### <span data-ttu-id="33414-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="33414-141">-ApiVersion</span></span>
<span data-ttu-id="33414-142">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="33414-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="33414-143">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="33414-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="33414-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="33414-144">-AssignIdentity</span></span>
<span data-ttu-id="33414-145">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="33414-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="33414-146">Az identitás a "deployIfNotExists" házirendek telepítésének végrehajtásakor lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="33414-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="33414-147">Az identitás hozzárendelésekor a hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="33414-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="33414-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33414-148">-DefaultProfile</span></span>
<span data-ttu-id="33414-149">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="33414-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33414-150">-Leírás</span><span class="sxs-lookup"><span data-stu-id="33414-150">-Description</span></span>
<span data-ttu-id="33414-151">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="33414-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="33414-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="33414-152">-DisplayName</span></span>
<span data-ttu-id="33414-153">A házirend-hozzárendelés új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33414-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="33414-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="33414-154">-EnforcementMode</span></span>
<span data-ttu-id="33414-155">A házirend-hozzárendelés kényszerítési módja.</span><span class="sxs-lookup"><span data-stu-id="33414-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="33414-156">Jelenleg az érvényes értékek az alapértelmezettek, a DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="33414-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="33414-157">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="33414-157">-Id</span></span>
<span data-ttu-id="33414-158">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="33414-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33414-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33414-159">-InputObject</span></span>
<span data-ttu-id="33414-160">Az a házirend-hozzárendelési objektum, amely egy másik parancsmagból származó kimenetet frissít.</span><span class="sxs-lookup"><span data-stu-id="33414-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33414-161">-Hely</span><span class="sxs-lookup"><span data-stu-id="33414-161">-Location</span></span>
<span data-ttu-id="33414-162">A házirend-hozzárendelés erőforrás-identitásának helye.</span><span class="sxs-lookup"><span data-stu-id="33414-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="33414-163">Erre akkor van szükség, ha a-AssignIdentity kapcsolót használja.</span><span class="sxs-lookup"><span data-stu-id="33414-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="33414-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="33414-164">-Metadata</span></span>
<span data-ttu-id="33414-165">A házirend-hozzárendelés frissített metaadatai.</span><span class="sxs-lookup"><span data-stu-id="33414-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="33414-166">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="33414-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="33414-167">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="33414-167">-Name</span></span>
<span data-ttu-id="33414-168">Annak a házirend-hozzárendelésnek a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="33414-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33414-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="33414-169">-NotScope</span></span>
<span data-ttu-id="33414-170">A házirend-hozzárendelés nem hatókörök.</span><span class="sxs-lookup"><span data-stu-id="33414-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="33414-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="33414-171">-PolicyParameter</span></span>
<span data-ttu-id="33414-172">A házirend-hozzárendelés új házirend-paraméterei fájlelérési útja vagy karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="33414-172">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33414-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="33414-173">-PolicyParameterObject</span></span>
<span data-ttu-id="33414-174">A házirend-hozzárendelés új házirend-paraméterei objektuma.</span><span class="sxs-lookup"><span data-stu-id="33414-174">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33414-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="33414-175">-Pre</span></span>
<span data-ttu-id="33414-176">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="33414-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="33414-177">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="33414-177">-Scope</span></span>
<span data-ttu-id="33414-178">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="33414-178">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33414-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33414-179">CommonParameters</span></span>
<span data-ttu-id="33414-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33414-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33414-181">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="33414-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33414-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33414-182">INPUTS</span></span>

### <span data-ttu-id="33414-183">System. String</span><span class="sxs-lookup"><span data-stu-id="33414-183">System.String</span></span>

### <span data-ttu-id="33414-184">System. string []</span><span class="sxs-lookup"><span data-stu-id="33414-184">System.String[]</span></span>

## <span data-ttu-id="33414-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33414-185">OUTPUTS</span></span>

### <span data-ttu-id="33414-186">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="33414-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="33414-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33414-187">NOTES</span></span>

## <span data-ttu-id="33414-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33414-188">RELATED LINKS</span></span>

[<span data-ttu-id="33414-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="33414-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="33414-190">Új – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="33414-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="33414-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="33414-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


