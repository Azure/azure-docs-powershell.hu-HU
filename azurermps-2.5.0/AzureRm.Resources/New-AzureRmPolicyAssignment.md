---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: 6183d4b8da931836a1ec613c113b32c71871bbf2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850266"
---
# <span data-ttu-id="4c584-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4c584-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="4c584-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c584-102">SYNOPSIS</span></span>
<span data-ttu-id="4c584-103">Házirend-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4c584-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c584-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c584-104">SYNTAX</span></span>

### <span data-ttu-id="4c584-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c584-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4c584-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c584-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4c584-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c584-107">PolicyParameterStringParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4c584-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c584-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4c584-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c584-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4c584-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c584-110">DESCRIPTION</span></span>
<span data-ttu-id="4c584-111">A **New-AzureRmPolicyAssignment** parancsmag létrehoz egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="4c584-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="4c584-112">Adjon meg egy házirendet és egy hatókört.</span><span class="sxs-lookup"><span data-stu-id="4c584-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="4c584-113">Példák</span><span class="sxs-lookup"><span data-stu-id="4c584-113">EXAMPLES</span></span>

### <span data-ttu-id="4c584-114">1. példa: házirend-hozzárendelés az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="4c584-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="4c584-115">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzureRMResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c584-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4c584-116">A második parancs a VirtualMachinePolicy nevű házirend-definíciót a Get-AzureRmPolicyDefinition parancsmag használatával kapja meg, és a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c584-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="4c584-117">A végleges parancs a házirendet a $ResourceGroup **ResourceId** tulajdonsága által azonosított erőforráscsoport szintjén rendeli $Policy.</span><span class="sxs-lookup"><span data-stu-id="4c584-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="4c584-118">2. példa: házirend-hozzárendelés az erőforráscsoport szintjén a házirend-paraméter objektummal</span><span class="sxs-lookup"><span data-stu-id="4c584-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="4c584-119">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="4c584-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="4c584-120">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c584-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4c584-121">A második parancs az engedélyezett helyek beépített házirend-definícióját az Get-AzureRmPolicyDefinition parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4c584-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4c584-122">A parancs az objektumot a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c584-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="4c584-123">A harmadik és a negyedik parancs a nevében a "Kelet" nevű összes Azure-régiót tartalmazó objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4c584-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="4c584-124">A parancsok az objektumot a $AllowedLocations változóban tárolják.</span><span class="sxs-lookup"><span data-stu-id="4c584-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="4c584-125">A végleges parancs az $AllowedLocationsban a Policy paraméter objektummal az erőforráscsoport szintjén rendeli hozzá a házirendet a $Policyban.</span><span class="sxs-lookup"><span data-stu-id="4c584-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="4c584-126">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="4c584-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="4c584-127">3. példa: házirend-hozzárendelés az erőforráscsoport szintjén a házirend-paraméter fájllal</span><span class="sxs-lookup"><span data-stu-id="4c584-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="4c584-128">A következő tartalommal hozzon létre egy _AllowedLocations.js_ nevű fájlt a helyi munkakönyvtárban.</span><span class="sxs-lookup"><span data-stu-id="4c584-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="4c584-129">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzureRMResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c584-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4c584-130">A második parancs beolvassa az engedélyezett helyek beépített házirend-definícióját az Get-AzureRmPolicyDefinition parancsmag használatával, és a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c584-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="4c584-131">A végleges parancs kiosztja a házirendet $Policy a $ResourceGroup **ResourceId** tulajdonság által meghatározott erőforráscsoport AllowedLocations.jsa helyi munkakönyvtárban a Policy paramétert tartalmazó fájllal.</span><span class="sxs-lookup"><span data-stu-id="4c584-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="4c584-132">4. példa: házirend-hozzárendelés felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="4c584-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="4c584-133">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzureRMResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c584-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4c584-134">A második parancs a VirtualMachinePolicy nevű házirend-definíciót a Get-AzureRmPolicyDefinition parancsmag használatával kapja meg, és a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c584-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="4c584-135">A végleges parancs a házirendet a $Policy az erőforráscsoport-csoportba rendeli.</span><span class="sxs-lookup"><span data-stu-id="4c584-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="4c584-136">A rendszer automatikusan létrehoz egy felügyelt identitást, és hozzárendeli a házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="4c584-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="4c584-137">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c584-137">PARAMETERS</span></span>

### <span data-ttu-id="4c584-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4c584-138">-ApiVersion</span></span>
<span data-ttu-id="4c584-139">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c584-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4c584-140">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4c584-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4c584-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4c584-141">-AssignIdentity</span></span>
<span data-ttu-id="4c584-142">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="4c584-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="4c584-143">Az identitás a "deployIfNotExists" házirendek telepítésének végrehajtásakor lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="4c584-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="4c584-144">Az identitás hozzárendelésekor a hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="4c584-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="4c584-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c584-145">-DefaultProfile</span></span>
<span data-ttu-id="4c584-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4c584-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c584-147">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4c584-147">-Description</span></span>
<span data-ttu-id="4c584-148">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="4c584-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="4c584-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4c584-149">-DisplayName</span></span>
<span data-ttu-id="4c584-150">A házirend-hozzárendelés megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c584-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="4c584-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4c584-151">-InformationAction</span></span>
<span data-ttu-id="4c584-152">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="4c584-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="4c584-153">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4c584-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c584-154">Folytassa</span><span class="sxs-lookup"><span data-stu-id="4c584-154">Continue</span></span>
- <span data-ttu-id="4c584-155">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="4c584-155">Ignore</span></span>
- <span data-ttu-id="4c584-156">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="4c584-156">Inquire</span></span>
- <span data-ttu-id="4c584-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4c584-157">SilentlyContinue</span></span>
- <span data-ttu-id="4c584-158">állj</span><span class="sxs-lookup"><span data-stu-id="4c584-158">Stop</span></span>
- <span data-ttu-id="4c584-159">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="4c584-159">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c584-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4c584-160">-InformationVariable</span></span>
<span data-ttu-id="4c584-161">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="4c584-161">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c584-162">-Hely</span><span class="sxs-lookup"><span data-stu-id="4c584-162">-Location</span></span>
<span data-ttu-id="4c584-163">A házirend-hozzárendelés erőforrás-identitásának helye.</span><span class="sxs-lookup"><span data-stu-id="4c584-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="4c584-164">Erre akkor van szükség, ha a-AssignIdentity kapcsolót használja.</span><span class="sxs-lookup"><span data-stu-id="4c584-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="4c584-165">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4c584-165">-Metadata</span></span>
<span data-ttu-id="4c584-166">Az új házirend-hozzárendelés metaadatai.</span><span class="sxs-lookup"><span data-stu-id="4c584-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="4c584-167">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="4c584-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="4c584-168">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c584-168">-Name</span></span>
<span data-ttu-id="4c584-169">A házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c584-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="4c584-170">-NotScope</span><span class="sxs-lookup"><span data-stu-id="4c584-170">-NotScope</span></span>
<span data-ttu-id="4c584-171">A házirend-hozzárendeléshez nem tartozó hatókörök</span><span class="sxs-lookup"><span data-stu-id="4c584-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="4c584-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4c584-172">-PolicyDefinition</span></span>
<span data-ttu-id="4c584-173">A házirendet adja meg **PsPolicyDefinition** -objektumként, amely a házirend-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4c584-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="4c584-174">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="4c584-174">-PolicyParameter</span></span>
<span data-ttu-id="4c584-175">A házirend paraméterének fájlelérési útja vagy a házirend paraméterének karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="4c584-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="4c584-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="4c584-176">-PolicyParameterObject</span></span>
<span data-ttu-id="4c584-177">A Policy paraméter objektuma.</span><span class="sxs-lookup"><span data-stu-id="4c584-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="4c584-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="4c584-178">-PolicySetDefinition</span></span>
<span data-ttu-id="4c584-179">A Policy set definition objektum.</span><span class="sxs-lookup"><span data-stu-id="4c584-179">The policy set definition object.</span></span>

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

### <span data-ttu-id="4c584-180">-Pre</span><span class="sxs-lookup"><span data-stu-id="4c584-180">-Pre</span></span>
<span data-ttu-id="4c584-181">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4c584-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4c584-182">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="4c584-182">-Scope</span></span>
<span data-ttu-id="4c584-183">A házirend hozzárendelésének hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c584-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="4c584-184">Ha például egy erőforrás-csoporthoz szeretne házirendet rendelni, adja meg a következőt: `/subscriptions/` előfizetés azonosítója `/resourcegroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="4c584-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="4c584-185">-SKU</span><span class="sxs-lookup"><span data-stu-id="4c584-185">-Sku</span></span>
<span data-ttu-id="4c584-186">A SKU tulajdonságokat reprezentáló kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="4c584-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="4c584-187">Az alapértelmezett érték a szabad SKU értékkel az értékekkel: `@{Name = 'A0'; Tier = 'Free'}` .</span><span class="sxs-lookup"><span data-stu-id="4c584-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="4c584-188">A standard SKU használatához használja az értékeket: `@{Name = 'A1'; Tier = 'Standard'}` .</span><span class="sxs-lookup"><span data-stu-id="4c584-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c584-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c584-189">CommonParameters</span></span>
<span data-ttu-id="4c584-190">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c584-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c584-191">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c584-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c584-192">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c584-192">INPUTS</span></span>

## <span data-ttu-id="4c584-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c584-193">OUTPUTS</span></span>

## <span data-ttu-id="4c584-194">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c584-194">NOTES</span></span>

## <span data-ttu-id="4c584-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c584-195">RELATED LINKS</span></span>

[<span data-ttu-id="4c584-196">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4c584-196">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4c584-197">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4c584-197">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="4c584-198">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4c584-198">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="4c584-199">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4c584-199">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


