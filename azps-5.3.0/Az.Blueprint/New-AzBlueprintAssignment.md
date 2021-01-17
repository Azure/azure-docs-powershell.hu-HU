---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478074"
---
# <span data-ttu-id="22efb-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="22efb-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="22efb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22efb-102">SYNOPSIS</span></span>
<span data-ttu-id="22efb-103">Tervrajzdefiníció hozzárendelése előfizetéshez vagy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="22efb-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="22efb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22efb-104">SYNTAX</span></span>

### <span data-ttu-id="22efb-105">CreateBlueprintAssignment (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22efb-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22efb-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="22efb-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22efb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22efb-107">DESCRIPTION</span></span>
<span data-ttu-id="22efb-108">Tervrajzdefiníció hozzárendelése előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="22efb-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="22efb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22efb-109">EXAMPLES</span></span>

### <span data-ttu-id="22efb-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="22efb-110">Example 1</span></span>
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

<span data-ttu-id="22efb-111">A megadott előfizetésben a megadott paraméter- és erőforráscsoportszótár használatával létrehozhat egy új tervrajz-hozzárendelést a `$blueprintObject` tervdefinícióhoz.</span><span class="sxs-lookup"><span data-stu-id="22efb-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="22efb-112">Rendszer által hozzárendelt identitást használ.</span><span class="sxs-lookup"><span data-stu-id="22efb-112">Uses system-assigned identity.</span></span> <span data-ttu-id="22efb-113">A hely határozza meg a felügyelt identitás létrehozására vonatkozó régiót.</span><span class="sxs-lookup"><span data-stu-id="22efb-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="22efb-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="22efb-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="22efb-115">Hozzon létre egy új tervrajz-hozzárendelést a megadott előfizetésben a megadott paraméter- és erőforráscsoportszótár alapján, és konfigurálja az erőforrászárolást az `$blueprintObject` **AllResources szolgáltatásban.**</span><span class="sxs-lookup"><span data-stu-id="22efb-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="22efb-116">Alapértelmezés szerint a rendszer által hozzárendelt identitást használja.</span><span class="sxs-lookup"><span data-stu-id="22efb-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="22efb-117">A hely határozza meg a felügyelt identitás létrehozására vonatkozó régiót.</span><span class="sxs-lookup"><span data-stu-id="22efb-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="22efb-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="22efb-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="22efb-119">A megadott előfizetésben a megadott paraméter- és erőforráscsoport-szótár használatával létrehozhatja a tervdefiníció új tervrajz-hozzárendelését a megadott felhasználó által hozzárendelt `$blueprintObject` identitásazonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="22efb-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="22efb-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="22efb-120">Example 4</span></span>
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

<span data-ttu-id="22efb-121">Terv-hozzárendelés létrehozása egy feladatfájlon keresztül.</span><span class="sxs-lookup"><span data-stu-id="22efb-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="22efb-122">A feladatfájl formátuma a kérelem/válasz mintáiban található: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="22efb-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="22efb-123">5. példa</span><span class="sxs-lookup"><span data-stu-id="22efb-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="22efb-124">Hozzon létre egy új tervrajz-hozzárendelést a megadott előfizetéshez a megadott felügyeleti csoporton belül a megadott paraméter `$blueprintObject` használatával.</span><span class="sxs-lookup"><span data-stu-id="22efb-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="22efb-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22efb-125">PARAMETERS</span></span>

### <span data-ttu-id="22efb-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="22efb-126">-AssignmentFile</span></span>
<span data-ttu-id="22efb-127">A feladatfájl helye lemezen JSON formátumban.</span><span class="sxs-lookup"><span data-stu-id="22efb-127">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="22efb-128">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="22efb-128">-Blueprint</span></span>
<span data-ttu-id="22efb-129">Blueprint definition object.</span><span class="sxs-lookup"><span data-stu-id="22efb-129">Blueprint definition object.</span></span>

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

### <span data-ttu-id="22efb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22efb-130">-DefaultProfile</span></span>
<span data-ttu-id="22efb-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22efb-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22efb-132">-Location</span><span class="sxs-lookup"><span data-stu-id="22efb-132">-Location</span></span>
<span data-ttu-id="22efb-133">Régió, ahol a felügyelt identitást létre kell hoznunk.</span><span class="sxs-lookup"><span data-stu-id="22efb-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="22efb-134">További információ a aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="22efb-134">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="22efb-135">-Lock</span><span class="sxs-lookup"><span data-stu-id="22efb-135">-Lock</span></span>
<span data-ttu-id="22efb-136">Erőforrások zárolása</span><span class="sxs-lookup"><span data-stu-id="22efb-136">Lock resources.</span></span>
<span data-ttu-id="22efb-137">További információ a aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="22efb-137">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="22efb-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="22efb-138">-ManagementGroupId</span></span>
<span data-ttu-id="22efb-139">Annak a felügyeleti csoportnak az azonosítója, amelybe a Tervrajz hozzárendelés(eket) menti a rendszer.</span><span class="sxs-lookup"><span data-stu-id="22efb-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="22efb-140">-Name</span><span class="sxs-lookup"><span data-stu-id="22efb-140">-Name</span></span>
<span data-ttu-id="22efb-141">A terv feladatának neve.</span><span class="sxs-lookup"><span data-stu-id="22efb-141">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="22efb-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="22efb-142">-Parameter</span></span>
<span data-ttu-id="22efb-143">Az összetevő paraméterei.</span><span class="sxs-lookup"><span data-stu-id="22efb-143">Artifact parameters.</span></span>

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

### <span data-ttu-id="22efb-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="22efb-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="22efb-145">Az erőforráscsoport-összetevőnek átadni szükséges paraméterek kivonata.</span><span class="sxs-lookup"><span data-stu-id="22efb-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="22efb-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="22efb-146">-SecureStringParameter</span></span>
<span data-ttu-id="22efb-147">Secure string parameter for KeyVault resource id, name and version.</span><span class="sxs-lookup"><span data-stu-id="22efb-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="22efb-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22efb-148">-SubscriptionId</span></span>
<span data-ttu-id="22efb-149">Előfizetés azonosítója a tervrajzdefiníció hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="22efb-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="22efb-150">Az előfizetésazonosító karakterláncai vesszővel tagolt listája lehet.</span><span class="sxs-lookup"><span data-stu-id="22efb-150">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="22efb-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="22efb-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="22efb-152">A rendszer által hozzárendelt identitás(MSI) az összetevők telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="22efb-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="22efb-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="22efb-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="22efb-154">Felhasználó által hozzárendelt identitás(MSI) az összetevők telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="22efb-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="22efb-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22efb-155">-Confirm</span></span>
<span data-ttu-id="22efb-156">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22efb-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22efb-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22efb-157">-WhatIf</span></span>
<span data-ttu-id="22efb-158">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22efb-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22efb-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22efb-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22efb-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22efb-160">CommonParameters</span></span>
<span data-ttu-id="22efb-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22efb-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22efb-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22efb-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22efb-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22efb-163">INPUTS</span></span>

### <span data-ttu-id="22efb-164">System.String</span><span class="sxs-lookup"><span data-stu-id="22efb-164">System.String</span></span>

### <span data-ttu-id="22efb-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="22efb-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="22efb-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="22efb-166">System.String[]</span></span>

### <span data-ttu-id="22efb-167">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="22efb-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22efb-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22efb-168">OUTPUTS</span></span>

### <span data-ttu-id="22efb-169">System.Object</span><span class="sxs-lookup"><span data-stu-id="22efb-169">System.Object</span></span>
## <span data-ttu-id="22efb-170">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22efb-170">NOTES</span></span>

## <span data-ttu-id="22efb-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22efb-171">RELATED LINKS</span></span>
