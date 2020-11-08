---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: ab0617b4012ca623bf67471a9a5bcc3ccf54d905
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011736"
---
# <span data-ttu-id="ad6c7-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ad6c7-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="ad6c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad6c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6c7-103">Házirend-hozzárendelés módosítása</span><span class="sxs-lookup"><span data-stu-id="ad6c7-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="ad6c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad6c7-104">SYNTAX</span></span>

### <span data-ttu-id="ad6c7-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad6c7-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6c7-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad6c7-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6c7-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad6c7-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6c7-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad6c7-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6c7-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad6c7-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6c7-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad6c7-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad6c7-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad6c7-111">DESCRIPTION</span></span>
<span data-ttu-id="ad6c7-112">A **set-AzPolicyAssignment** parancsmag módosította egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="ad6c7-113">Adjon meg egy hozzárendelést azonosító alapján vagy név és hatókör szerint.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="ad6c7-114">Példák</span><span class="sxs-lookup"><span data-stu-id="ad6c7-114">EXAMPLES</span></span>

### <span data-ttu-id="ad6c7-115">Példa 1: a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="ad6c7-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="ad6c7-116">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ad6c7-117">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="ad6c7-118">A második parancs az Get-AzPolicyAssignment parancsmag használatával kapja meg a PolicyAssignment nevű házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="ad6c7-119">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ad6c7-120">A végleges parancs frissíti a megjelenítendő nevet az $ResourceGroup **ResourceId** tulajdonsága által azonosított erőforráscsoport házirend-hozzárendelésében.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="ad6c7-121">2. példa: felügyelt identitás hozzáadása a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="ad6c7-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="ad6c7-122">Az első parancs a PolicyAssignment nevű házirend-hozzárendelést az aktuális előfizetésből az Get-AzPolicyAssignment parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="ad6c7-123">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ad6c7-124">A végleges parancs a felügyelt identitást a házirend-hozzárendeléshez rendeli.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="ad6c7-125">3. példa: házirend-hozzárendelési paraméterek frissítése új házirend-paraméteres objektummal</span><span class="sxs-lookup"><span data-stu-id="ad6c7-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="ad6c7-126">Az első és a második parancs az összes Azure-régiót tartalmazó objektumot hoz létre, amelynek a nevei a "Franciaország" vagy az "Egyesült Királyság" betűvel kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="ad6c7-127">A második parancs az objektumot a $AllowedLocations változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="ad6c7-128">A harmadik parancs a "PolicyAssignment" nevű házirend-hozzárendelést kapja meg, a parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ad6c7-129">A végleges parancs frissíti a PolicyAssignment nevű házirend-hozzárendelés paramétereinek értékeit.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="ad6c7-130">Példa 4: házirend-hozzárendelési paraméterek frissítése házirend-paraméteres fájllal</span><span class="sxs-lookup"><span data-stu-id="ad6c7-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="ad6c7-131">A következő tartalommal hozzon létre egy _AllowedLocations.js_ nevű fájlt a helyi munkakönyvtárban.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="ad6c7-132">A parancs frissíti a "PolicyAssignment" nevű házirend-hozzárendelést a helyi munkakönyvtárból AllowedLocations.jsházirend-paraméter fájljában.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="ad6c7-133">Példa 5: enforcementMode frissítése</span><span class="sxs-lookup"><span data-stu-id="ad6c7-133">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="ad6c7-134">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-134">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ad6c7-135">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-135">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="ad6c7-136">A második parancs az Get-AzPolicyAssignment parancsmag használatával kapja meg a PolicyAssignment nevű házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-136">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="ad6c7-137">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-137">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ad6c7-138">A végleges parancs frissíti a enforcementMode tulajdonságot az $ResourceGroup **ResourceId** tulajdonsága által azonosított erőforráscsoport házirend-hozzárendeléseiben.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-138">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="ad6c7-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad6c7-139">PARAMETERS</span></span>

### <span data-ttu-id="ad6c7-140">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ad6c7-140">-ApiVersion</span></span>
<span data-ttu-id="ad6c7-141">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-141">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ad6c7-142">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-142">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ad6c7-143">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ad6c7-143">-AssignIdentity</span></span>
<span data-ttu-id="ad6c7-144">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="ad6c7-144">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="ad6c7-145">Az identitás a "deployIfNotExists" házirendek telepítésének végrehajtásakor lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-145">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="ad6c7-146">Az identitás hozzárendelésekor a hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-146">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="ad6c7-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6c7-147">-DefaultProfile</span></span>
<span data-ttu-id="ad6c7-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ad6c7-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad6c7-149">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ad6c7-149">-Description</span></span>
<span data-ttu-id="ad6c7-150">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="ad6c7-150">The description for policy assignment</span></span>

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

### <span data-ttu-id="ad6c7-151">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ad6c7-151">-DisplayName</span></span>
<span data-ttu-id="ad6c7-152">A házirend-hozzárendelés új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-152">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="ad6c7-153">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="ad6c7-153">-EnforcementMode</span></span>
<span data-ttu-id="ad6c7-154">A házirend-hozzárendelés kényszerítési módja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-154">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="ad6c7-155">Jelenleg az érvényes értékek az alapértelmezettek, a DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-155">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="ad6c7-156">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ad6c7-156">-Id</span></span>
<span data-ttu-id="ad6c7-157">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-157">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ad6c7-158">-Hely</span><span class="sxs-lookup"><span data-stu-id="ad6c7-158">-Location</span></span>
<span data-ttu-id="ad6c7-159">A házirend-hozzárendelés erőforrás-identitásának helye.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-159">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="ad6c7-160">Erre akkor van szükség, ha a-AssignIdentity kapcsolót használja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-160">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="ad6c7-161">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ad6c7-161">-Metadata</span></span>
<span data-ttu-id="ad6c7-162">A házirend-hozzárendelés frissített metaadatai.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-162">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="ad6c7-163">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-163">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="ad6c7-164">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad6c7-164">-Name</span></span>
<span data-ttu-id="ad6c7-165">Annak a házirend-hozzárendelésnek a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-165">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ad6c7-166">-NotScope</span><span class="sxs-lookup"><span data-stu-id="ad6c7-166">-NotScope</span></span>
<span data-ttu-id="ad6c7-167">A házirend-hozzárendelés nem hatókörök.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-167">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="ad6c7-168">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="ad6c7-168">-PolicyParameter</span></span>
<span data-ttu-id="ad6c7-169">A házirend-hozzárendelés új házirend-paraméterei fájlelérési útja vagy karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-169">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="ad6c7-170">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="ad6c7-170">-PolicyParameterObject</span></span>
<span data-ttu-id="ad6c7-171">A házirend-hozzárendelés új házirend-paraméterei objektuma.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-171">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="ad6c7-172">-Pre</span><span class="sxs-lookup"><span data-stu-id="ad6c7-172">-Pre</span></span>
<span data-ttu-id="ad6c7-173">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-173">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ad6c7-174">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="ad6c7-174">-Scope</span></span>
<span data-ttu-id="ad6c7-175">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-175">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="ad6c7-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6c7-176">CommonParameters</span></span>
<span data-ttu-id="ad6c7-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad6c7-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6c7-178">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6c7-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad6c7-179">INPUTS</span></span>

### <span data-ttu-id="ad6c7-180">System. String</span><span class="sxs-lookup"><span data-stu-id="ad6c7-180">System.String</span></span>

### <span data-ttu-id="ad6c7-181">System. string []</span><span class="sxs-lookup"><span data-stu-id="ad6c7-181">System.String[]</span></span>

## <span data-ttu-id="ad6c7-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad6c7-182">OUTPUTS</span></span>

### <span data-ttu-id="ad6c7-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ad6c7-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ad6c7-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad6c7-184">NOTES</span></span>

## <span data-ttu-id="ad6c7-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad6c7-185">RELATED LINKS</span></span>

[<span data-ttu-id="ad6c7-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ad6c7-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="ad6c7-187">Új – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ad6c7-187">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="ad6c7-188">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ad6c7-188">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


