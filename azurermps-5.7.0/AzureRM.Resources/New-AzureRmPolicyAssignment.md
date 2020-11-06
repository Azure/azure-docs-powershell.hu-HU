---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500412"
---
# <span data-ttu-id="edfb2-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="edfb2-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="edfb2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="edfb2-102">SYNOPSIS</span></span>
<span data-ttu-id="edfb2-103">Házirend-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="edfb2-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edfb2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="edfb2-104">SYNTAX</span></span>

### <span data-ttu-id="edfb2-105">CreateWithoutParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="edfb2-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="edfb2-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="edfb2-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="edfb2-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="edfb2-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="edfb2-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="edfb2-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="edfb2-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="edfb2-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="edfb2-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="edfb2-110">DESCRIPTION</span></span>
<span data-ttu-id="edfb2-111">A **New-AzureRmPolicyAssignment** parancsmag létrehoz egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="edfb2-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="edfb2-112">Adjon meg egy házirendet és egy hatókört.</span><span class="sxs-lookup"><span data-stu-id="edfb2-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="edfb2-113">Példák</span><span class="sxs-lookup"><span data-stu-id="edfb2-113">EXAMPLES</span></span>

### <span data-ttu-id="edfb2-114">1. példa: házirend-hozzárendelés az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="edfb2-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="edfb2-115">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="edfb2-116">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="edfb2-117">A második parancs az Get-AzureRmPolicyDefinition parancsmag segítségével a VirtualMachinePolicy nevű házirend-definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="edfb2-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="edfb2-118">A parancs az objektumot a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="edfb2-119">A végleges parancs az erőforráscsoport szintjén rendeli hozzá a házirendet a $Policyhoz.</span><span class="sxs-lookup"><span data-stu-id="edfb2-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="edfb2-120">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="edfb2-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="edfb2-121">2. példa: házirend-hozzárendelés az erőforráscsoport szintjén a házirend-paraméter objektummal</span><span class="sxs-lookup"><span data-stu-id="edfb2-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="edfb2-122">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="edfb2-123">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="edfb2-124">A második parancs az engedélyezett helyek beépített házirend-definícióját az Get-AzureRmPolicyDefinition parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="edfb2-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="edfb2-125">A parancs az objektumot a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="edfb2-126">A harmadik és a negyedik parancs a nevében a "Kelet" nevű összes Azure-régiót tartalmazó objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="edfb2-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="edfb2-127">A parancsok az objektumot a $AllowedLocations változóban tárolják.</span><span class="sxs-lookup"><span data-stu-id="edfb2-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="edfb2-128">A végleges parancs az $AllowedLocationsban a Policy paraméter objektummal az erőforráscsoport szintjén rendeli hozzá a házirendet a $Policyban.</span><span class="sxs-lookup"><span data-stu-id="edfb2-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="edfb2-129">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="edfb2-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="edfb2-130">3. példa: házirend-hozzárendelés az erőforráscsoport szintjén a házirend-paraméter fájllal</span><span class="sxs-lookup"><span data-stu-id="edfb2-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="edfb2-131">A következő tartalommal hozzon létre egy _AllowedLocations.js_ nevű fájlt a helyi munkakönyvtárban.</span><span class="sxs-lookup"><span data-stu-id="edfb2-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="edfb2-132">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="edfb2-133">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="edfb2-134">A második parancs az engedélyezett helyek beépített házirend-definícióját az Get-AzureRmPolicyDefinition parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="edfb2-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="edfb2-135">A parancs az objektumot a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="edfb2-136">A végleges parancs a házirendet a helyi munkakönyvtárból beAllowedLocations.jsházirend-paramétert tartalmazó $Policy alapján rendeli hozzá az erőforráscsoport szintjéhez.</span><span class="sxs-lookup"><span data-stu-id="edfb2-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="edfb2-137">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="edfb2-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="edfb2-138">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="edfb2-138">PARAMETERS</span></span>

### <span data-ttu-id="edfb2-139">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="edfb2-139">-ApiVersion</span></span>
<span data-ttu-id="edfb2-140">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="edfb2-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="edfb2-141">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfb2-142">-DefaultProfile</span></span>
<span data-ttu-id="edfb2-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="edfb2-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-144">-Leírás</span><span class="sxs-lookup"><span data-stu-id="edfb2-144">-Description</span></span>
<span data-ttu-id="edfb2-145">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="edfb2-145">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="edfb2-146">-DisplayName</span></span>
<span data-ttu-id="edfb2-147">A házirend-hozzárendelés megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="edfb2-147">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="edfb2-148">-InformationAction</span></span>
<span data-ttu-id="edfb2-149">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="edfb2-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="edfb2-150">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="edfb2-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="edfb2-151">Folytassa</span><span class="sxs-lookup"><span data-stu-id="edfb2-151">Continue</span></span>
- <span data-ttu-id="edfb2-152">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="edfb2-152">Ignore</span></span>
- <span data-ttu-id="edfb2-153">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="edfb2-153">Inquire</span></span>
- <span data-ttu-id="edfb2-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="edfb2-154">SilentlyContinue</span></span>
- <span data-ttu-id="edfb2-155">állj</span><span class="sxs-lookup"><span data-stu-id="edfb2-155">Stop</span></span>
- <span data-ttu-id="edfb2-156">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="edfb2-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="edfb2-157">-InformationVariable</span></span>
<span data-ttu-id="edfb2-158">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="edfb2-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="edfb2-159">-Name</span></span>
<span data-ttu-id="edfb2-160">A házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="edfb2-160">Specifies a name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-161">-NotScope</span><span class="sxs-lookup"><span data-stu-id="edfb2-161">-NotScope</span></span>
<span data-ttu-id="edfb2-162">A házirend-hozzárendeléshez nem tartozó hatókörök</span><span class="sxs-lookup"><span data-stu-id="edfb2-162">The not scopes for policy assignment.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="edfb2-163">-PolicyDefinition</span></span>
<span data-ttu-id="edfb2-164">A házirendet adja meg **PSObject** -objektumként, amely a házirend-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="edfb2-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-165">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="edfb2-165">-PolicyParameter</span></span>
<span data-ttu-id="edfb2-166">A házirend paraméterének fájlelérési útja vagy a házirend paraméterének karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="edfb2-166">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="edfb2-167">-PolicyParameterObject</span></span>
<span data-ttu-id="edfb2-168">A Policy paraméter objektuma.</span><span class="sxs-lookup"><span data-stu-id="edfb2-168">The policy parameter object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="edfb2-169">-PolicySetDefinition</span></span>
<span data-ttu-id="edfb2-170">A Policy set definition objektum.</span><span class="sxs-lookup"><span data-stu-id="edfb2-170">The policy set definition object.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-171">-Pre</span><span class="sxs-lookup"><span data-stu-id="edfb2-171">-Pre</span></span>
<span data-ttu-id="edfb2-172">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="edfb2-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-173">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="edfb2-173">-Scope</span></span>
<span data-ttu-id="edfb2-174">A házirend hozzárendelésének hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="edfb2-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="edfb2-175">Ha például egy erőforrás-csoporthoz szeretne házirendet rendelni, adja meg az alábbiakat:</span><span class="sxs-lookup"><span data-stu-id="edfb2-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="edfb2-176">`/subscriptions/`előfizetés-azonosító `/resourcegroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="edfb2-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-177">-SKU</span><span class="sxs-lookup"><span data-stu-id="edfb2-177">-Sku</span></span>
<span data-ttu-id="edfb2-178">A SKU tulajdonságokat reprezentáló kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="edfb2-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="edfb2-179">Alapértékek az ingyenes SKU-hoz: név = a0, Tier = FRE</span><span class="sxs-lookup"><span data-stu-id="edfb2-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb2-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfb2-180">CommonParameters</span></span>
<span data-ttu-id="edfb2-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="edfb2-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfb2-182">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edfb2-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfb2-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="edfb2-183">INPUTS</span></span>

### <span data-ttu-id="edfb2-184">Nincs</span><span class="sxs-lookup"><span data-stu-id="edfb2-184">None</span></span>
<span data-ttu-id="edfb2-185">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="edfb2-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="edfb2-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edfb2-186">OUTPUTS</span></span>

### <span data-ttu-id="edfb2-187">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="edfb2-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="edfb2-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="edfb2-188">NOTES</span></span>

## <span data-ttu-id="edfb2-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edfb2-189">RELATED LINKS</span></span>

[<span data-ttu-id="edfb2-190">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="edfb2-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="edfb2-191">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="edfb2-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="edfb2-192">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="edfb2-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="edfb2-193">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="edfb2-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


