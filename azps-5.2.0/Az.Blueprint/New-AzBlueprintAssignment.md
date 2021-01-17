---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365775"
---
# <span data-ttu-id="404a3-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="404a3-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="404a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="404a3-102">SYNOPSIS</span></span>
<span data-ttu-id="404a3-103">Tervrajzdefiníció hozzárendelése előfizetéshez vagy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="404a3-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="404a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="404a3-104">SYNTAX</span></span>

### <span data-ttu-id="404a3-105">CreateBlueprintAssignment (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="404a3-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="404a3-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="404a3-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="404a3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="404a3-107">DESCRIPTION</span></span>
<span data-ttu-id="404a3-108">Tervrajzdefiníció hozzárendelése előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="404a3-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="404a3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="404a3-109">EXAMPLES</span></span>

### <span data-ttu-id="404a3-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="404a3-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="404a3-111">A megadott előfizetésben a megadott paraméter- és erőforráscsoportszótár használatával létrehozhat egy új tervrajz-hozzárendelést a `$blueprintObject` tervdefinícióhoz.</span><span class="sxs-lookup"><span data-stu-id="404a3-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="404a3-112">Rendszer által hozzárendelt identitást használ.</span><span class="sxs-lookup"><span data-stu-id="404a3-112">Uses system-assigned identity.</span></span> <span data-ttu-id="404a3-113">A hely határozza meg a felügyelt identitás létrehozására vonatkozó régiót.</span><span class="sxs-lookup"><span data-stu-id="404a3-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="404a3-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="404a3-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="404a3-115">Hozzon létre egy új tervrajz-hozzárendelést a megadott előfizetésben a megadott paraméter- és erőforráscsoportszótár alapján, és konfigurálja az erőforrászárolást az `$blueprintObject` **AllResources szolgáltatásban.**</span><span class="sxs-lookup"><span data-stu-id="404a3-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="404a3-116">Alapértelmezés szerint a rendszer által hozzárendelt identitást használja.</span><span class="sxs-lookup"><span data-stu-id="404a3-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="404a3-117">A hely határozza meg a felügyelt identitás létrehozására vonatkozó régiót.</span><span class="sxs-lookup"><span data-stu-id="404a3-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="404a3-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="404a3-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="404a3-119">A megadott előfizetésben a megadott paraméter- és erőforráscsoport-szótár használatával létrehozhatja a tervdefiníció új tervrajz-hozzárendelését a megadott felhasználó által hozzárendelt `$blueprintObject` identitásazonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="404a3-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="404a3-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="404a3-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="404a3-121">Terv-hozzárendelés létrehozása egy feladatfájlon keresztül.</span><span class="sxs-lookup"><span data-stu-id="404a3-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="404a3-122">A feladatfájl formátuma megtalálható a kérelem/válasz mintáiban: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="404a3-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="404a3-123">5. példa</span><span class="sxs-lookup"><span data-stu-id="404a3-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="404a3-124">Hozzon létre egy új tervrajz-hozzárendelést a megadott előfizetéshez a megadott felügyeleti csoporton belül a megadott paraméter `$blueprintObject` használatával.</span><span class="sxs-lookup"><span data-stu-id="404a3-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="404a3-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="404a3-125">PARAMETERS</span></span>

### <span data-ttu-id="404a3-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="404a3-126">-AssignmentFile</span></span>
<span data-ttu-id="404a3-127">A feladatfájl helye lemezen JSON formátumban.</span><span class="sxs-lookup"><span data-stu-id="404a3-127">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-128">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="404a3-128">-Blueprint</span></span>
<span data-ttu-id="404a3-129">Blueprint definition object.</span><span class="sxs-lookup"><span data-stu-id="404a3-129">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="404a3-130">-DefaultProfile</span></span>
<span data-ttu-id="404a3-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="404a3-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="404a3-132">-Location</span><span class="sxs-lookup"><span data-stu-id="404a3-132">-Location</span></span>
<span data-ttu-id="404a3-133">Régió, ahol a felügyelt identitást létre kell hoznunk.</span><span class="sxs-lookup"><span data-stu-id="404a3-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="404a3-134">További információ a aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="404a3-134">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-135">-Lock</span><span class="sxs-lookup"><span data-stu-id="404a3-135">-Lock</span></span>
<span data-ttu-id="404a3-136">Erőforrások zárolása</span><span class="sxs-lookup"><span data-stu-id="404a3-136">Lock resources.</span></span>
<span data-ttu-id="404a3-137">További információ a aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="404a3-137">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: CreateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="404a3-138">-ManagementGroupId</span></span>
<span data-ttu-id="404a3-139">Annak a felügyeleti csoportnak az azonosítója, amelybe a Tervrajz hozzárendelés(eket) menti a rendszer.</span><span class="sxs-lookup"><span data-stu-id="404a3-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-140">-Name</span><span class="sxs-lookup"><span data-stu-id="404a3-140">-Name</span></span>
<span data-ttu-id="404a3-141">A terv feladatának neve.</span><span class="sxs-lookup"><span data-stu-id="404a3-141">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="404a3-142">-Parameter</span></span>
<span data-ttu-id="404a3-143">Az összetevő paraméterei.</span><span class="sxs-lookup"><span data-stu-id="404a3-143">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="404a3-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="404a3-145">Az erőforráscsoport-összetevőnek átadni szükséges paraméterek kivonata.</span><span class="sxs-lookup"><span data-stu-id="404a3-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="404a3-146">-SecureStringParameter</span></span>
<span data-ttu-id="404a3-147">Secure string parameter for KeyVault resource id, name and version.</span><span class="sxs-lookup"><span data-stu-id="404a3-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="404a3-148">-SubscriptionId</span></span>
<span data-ttu-id="404a3-149">Előfizetés azonosítója a tervrajzdefiníció hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="404a3-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="404a3-150">Az előfizetésazonosító karakterláncai vesszővel tagolt listája lehet.</span><span class="sxs-lookup"><span data-stu-id="404a3-150">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="404a3-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="404a3-152">A rendszer által hozzárendelt identitás(MSI) az összetevők telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="404a3-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="404a3-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="404a3-154">Felhasználó által hozzárendelt identitás(MSI) az összetevők telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="404a3-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="404a3-155">-Confirm</span></span>
<span data-ttu-id="404a3-156">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="404a3-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="404a3-157">-WhatIf</span></span>
<span data-ttu-id="404a3-158">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="404a3-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="404a3-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="404a3-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404a3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404a3-160">CommonParameters</span></span>
<span data-ttu-id="404a3-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404a3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404a3-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="404a3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404a3-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="404a3-163">INPUTS</span></span>

### <span data-ttu-id="404a3-164">System.String</span><span class="sxs-lookup"><span data-stu-id="404a3-164">System.String</span></span>

### <span data-ttu-id="404a3-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="404a3-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="404a3-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="404a3-166">System.String[]</span></span>

### <span data-ttu-id="404a3-167">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="404a3-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="404a3-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="404a3-168">OUTPUTS</span></span>

### <span data-ttu-id="404a3-169">System.Object</span><span class="sxs-lookup"><span data-stu-id="404a3-169">System.Object</span></span>
## <span data-ttu-id="404a3-170">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="404a3-170">NOTES</span></span>

## <span data-ttu-id="404a3-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="404a3-171">RELATED LINKS</span></span>
