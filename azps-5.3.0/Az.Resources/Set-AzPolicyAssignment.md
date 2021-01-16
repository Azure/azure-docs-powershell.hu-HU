---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480200"
---
# <span data-ttu-id="0fa38-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0fa38-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="0fa38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fa38-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa38-103">Egy házirend-hozzárendelést módosít.</span><span class="sxs-lookup"><span data-stu-id="0fa38-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="0fa38-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0fa38-104">SYNTAX</span></span>

### <span data-ttu-id="0fa38-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fa38-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fa38-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa38-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fa38-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa38-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fa38-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa38-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fa38-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa38-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fa38-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa38-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fa38-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa38-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fa38-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0fa38-112">DESCRIPTION</span></span>
<span data-ttu-id="0fa38-113">A **Set-AzPolicyAssignment** parancsmag módosítja a házirend-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="0fa38-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="0fa38-114">Adjon meg egy feladatot azonosító, illetve név és hatókör szerint.</span><span class="sxs-lookup"><span data-stu-id="0fa38-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="0fa38-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0fa38-115">EXAMPLES</span></span>

### <span data-ttu-id="0fa38-116">1. példa: A megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="0fa38-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="0fa38-117">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="0fa38-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="0fa38-118">A parancs az objektumot a $ResourceGroup tárolja.</span><span class="sxs-lookup"><span data-stu-id="0fa38-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0fa38-119">A második parancs a Házirend hozzárendelése nevű házirend-hozzárendelést a Get-AzPolicyAssignment parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0fa38-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="0fa38-120">A parancs az objektumot a $PolicyAssignment tárolja.</span><span class="sxs-lookup"><span data-stu-id="0fa38-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0fa38-121">A végleges parancs frissíti a megjelenítendő nevet a házirend-hozzárendelésben az erőforráscsoport **ResourceId** tulajdonsága által meghatározott $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0fa38-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="0fa38-122">2. példa: Felügyelt identitás hozzáadása a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="0fa38-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="0fa38-123">Az első parancs a Házirend hozzárendelése nevű házirend-hozzárendelést az aktuális előfizetésből kapja meg a Get-AzPolicyAssignment parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="0fa38-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="0fa38-124">A parancs az objektumot a $PolicyAssignment tárolja.</span><span class="sxs-lookup"><span data-stu-id="0fa38-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0fa38-125">Az utolsó parancs felügyelt identitást rendel a házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="0fa38-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="0fa38-126">3. példa: Házirend-hozzárendelés paramétereinek frissítése új házirend paraméterobjektummal</span><span class="sxs-lookup"><span data-stu-id="0fa38-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="0fa38-127">Az első és a második parancs egy olyan objektumot hoz létre, amely tartalmazza az összes Olyan Azure-régiót, amelynek a neve "france" (franciaország) vagy "uk" (egyesült királyság) kezdetekkel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="0fa38-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="0fa38-128">A második parancs az objektumot a $AllowedLocations tárolja.</span><span class="sxs-lookup"><span data-stu-id="0fa38-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="0fa38-129">A harmadik parancs a "PolicyAssignment" nevű házirend-hozzárendelést kapja meg. A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0fa38-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0fa38-130">A végleges parancs frissíti a PolicyAssignment nevű házirend-hozzárendelés paraméterértékeit.</span><span class="sxs-lookup"><span data-stu-id="0fa38-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="0fa38-131">4. példa: Házirend-hozzárendelés paramétereinek frissítése a házirend paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="0fa38-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="0fa38-132">Hozzon létre egyAllowedLocations.js _nevű_ fájlt a helyi munkakönyvtárban az alábbi tartalommal.</span><span class="sxs-lookup"><span data-stu-id="0fa38-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="0fa38-133">A parancs frissíti a "PolicyAssignment" nevű házirend-hozzárendelést a helyi munkakönyvtárban AllowedLocations.jsparaméterfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="0fa38-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="0fa38-134">5. példa: A enforcementMode frissítése</span><span class="sxs-lookup"><span data-stu-id="0fa38-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="0fa38-135">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="0fa38-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="0fa38-136">A parancs az objektumot a $ResourceGroup tárolja.</span><span class="sxs-lookup"><span data-stu-id="0fa38-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0fa38-137">A második parancs a Házirend hozzárendelése nevű házirend-hozzárendelést a Get-AzPolicyAssignment parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0fa38-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="0fa38-138">A parancs az objektumot a $PolicyAssignment tárolja.</span><span class="sxs-lookup"><span data-stu-id="0fa38-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0fa38-139">A végleges parancs frissíti a enforcementMode tulajdonságot a házirend-hozzárendelésben az erőforráscsoport **ResourceId** tulajdonsága által $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0fa38-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="0fa38-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fa38-140">PARAMETERS</span></span>

### <span data-ttu-id="0fa38-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0fa38-141">-ApiVersion</span></span>
<span data-ttu-id="0fa38-142">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fa38-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0fa38-143">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0fa38-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0fa38-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0fa38-144">-AssignIdentity</span></span>
<span data-ttu-id="0fa38-145">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="0fa38-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="0fa38-146">Az identitást a "deployIfNotExists" házirendek telepítésének végrehajtásakor fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="0fa38-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="0fa38-147">Identitás hozzárendelésekor hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="0fa38-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="0fa38-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa38-148">-DefaultProfile</span></span>
<span data-ttu-id="0fa38-149">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0fa38-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fa38-150">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0fa38-150">-Description</span></span>
<span data-ttu-id="0fa38-151">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="0fa38-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="0fa38-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0fa38-152">-DisplayName</span></span>
<span data-ttu-id="0fa38-153">A házirend-hozzárendelés új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fa38-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="0fa38-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="0fa38-154">-EnforcementMode</span></span>
<span data-ttu-id="0fa38-155">A házirend-hozzárendelés kényszerítési módja.</span><span class="sxs-lookup"><span data-stu-id="0fa38-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="0fa38-156">Jelenleg az érvényes értékek az Alapértelmezett, a DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="0fa38-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="0fa38-157">-Id</span><span class="sxs-lookup"><span data-stu-id="0fa38-157">-Id</span></span>
<span data-ttu-id="0fa38-158">A parancsmag által módosított házirend-hozzárendelés teljes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fa38-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0fa38-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fa38-159">-InputObject</span></span>
<span data-ttu-id="0fa38-160">Az a házirend-hozzárendelési objektum, amely egy másik parancsmagból lett kimenetként frissítve.</span><span class="sxs-lookup"><span data-stu-id="0fa38-160">The policy assignment object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="0fa38-161">-Location</span><span class="sxs-lookup"><span data-stu-id="0fa38-161">-Location</span></span>
<span data-ttu-id="0fa38-162">A házirend-hozzárendelés erőforrás-identitásának helye.</span><span class="sxs-lookup"><span data-stu-id="0fa38-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="0fa38-163">Erre a -AssignIdentity kapcsoló használata esetén van szükség.</span><span class="sxs-lookup"><span data-stu-id="0fa38-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="0fa38-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0fa38-164">-Metadata</span></span>
<span data-ttu-id="0fa38-165">A házirend-hozzárendelés frissített metaadatai.</span><span class="sxs-lookup"><span data-stu-id="0fa38-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="0fa38-166">Ez lehet egy olyan fájlnév elérési útja, amely tartalmazza a metaadatokat, vagy karakterláncként a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="0fa38-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="0fa38-167">-Name</span><span class="sxs-lookup"><span data-stu-id="0fa38-167">-Name</span></span>
<span data-ttu-id="0fa38-168">Megadja annak a házirend-hozzárendelésnek a nevét, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="0fa38-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0fa38-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="0fa38-169">-NotScope</span></span>
<span data-ttu-id="0fa38-170">A házirend-hozzárendelésnek nincs hatóköre.</span><span class="sxs-lookup"><span data-stu-id="0fa38-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="0fa38-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="0fa38-171">-PolicyParameter</span></span>
<span data-ttu-id="0fa38-172">A házirend-hozzárendelés új házirendparaméterek fájl elérési útja vagy karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="0fa38-172">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="0fa38-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="0fa38-173">-PolicyParameterObject</span></span>
<span data-ttu-id="0fa38-174">A házirend-hozzárendelés új házirendparaméter-objektuma.</span><span class="sxs-lookup"><span data-stu-id="0fa38-174">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="0fa38-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="0fa38-175">-Pre</span></span>
<span data-ttu-id="0fa38-176">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="0fa38-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0fa38-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="0fa38-177">-Scope</span></span>
<span data-ttu-id="0fa38-178">A házirend hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0fa38-178">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="0fa38-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa38-179">CommonParameters</span></span>
<span data-ttu-id="0fa38-180">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa38-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa38-181">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fa38-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa38-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fa38-182">INPUTS</span></span>

### <span data-ttu-id="0fa38-183">System.String</span><span class="sxs-lookup"><span data-stu-id="0fa38-183">System.String</span></span>

### <span data-ttu-id="0fa38-184">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0fa38-184">System.String[]</span></span>

## <span data-ttu-id="0fa38-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fa38-185">OUTPUTS</span></span>

### <span data-ttu-id="0fa38-186">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="0fa38-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0fa38-187">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0fa38-187">NOTES</span></span>

## <span data-ttu-id="0fa38-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fa38-188">RELATED LINKS</span></span>

[<span data-ttu-id="0fa38-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0fa38-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="0fa38-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0fa38-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="0fa38-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0fa38-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


