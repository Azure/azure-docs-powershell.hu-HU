---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017900"
---
# <span data-ttu-id="de72d-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="de72d-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="de72d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de72d-102">SYNOPSIS</span></span>
<span data-ttu-id="de72d-103">Tervrajz-definíció hozzárendelése előfizetéshez vagy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="de72d-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="de72d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de72d-104">SYNTAX</span></span>

### <span data-ttu-id="de72d-105">CreateBlueprintAssignment (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de72d-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de72d-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="de72d-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de72d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="de72d-107">DESCRIPTION</span></span>
<span data-ttu-id="de72d-108">Tervrajz-definíció hozzárendelése előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="de72d-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="de72d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="de72d-109">EXAMPLES</span></span>

### <span data-ttu-id="de72d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de72d-110">Example 1</span></span>
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

<span data-ttu-id="de72d-111">Hozzon létre egy új tervrajzot a terv definíciója alapján a `$blueprintObject` megadott előfizetésből a megadott paraméter és erőforráscsoport szótár használatával.</span><span class="sxs-lookup"><span data-stu-id="de72d-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="de72d-112">A rendszer által hozzárendelt identitást használja.</span><span class="sxs-lookup"><span data-stu-id="de72d-112">Uses system-assigned identity.</span></span> <span data-ttu-id="de72d-113">A hely határozza meg a felügyelt identitás létrehozásának területét.</span><span class="sxs-lookup"><span data-stu-id="de72d-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="de72d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="de72d-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="de72d-115">Hozzon létre egy új tervrajzot a terv definíciója alapján a `$blueprintObject` megadott előfizetésben a definiált paraméter és erőforráscsoport szótár segítségével, és konfigurálja az erőforrás-zárolást a **AllResources** -ra.</span><span class="sxs-lookup"><span data-stu-id="de72d-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="de72d-116">Alapértelmezések a rendszerszintű identitás használatához</span><span class="sxs-lookup"><span data-stu-id="de72d-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="de72d-117">A hely határozza meg a felügyelt identitás létrehozásának területét.</span><span class="sxs-lookup"><span data-stu-id="de72d-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="de72d-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="de72d-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="de72d-119">Hozzon létre egy új tervrajzot a terv definíciója alapján a `$blueprintObject` megadott előfizetésben a megadott paraméter és erőforráscsoport szótár segítségével a megadott felhasználó által kiosztott azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="de72d-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="de72d-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="de72d-120">Example 4</span></span>
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

<span data-ttu-id="de72d-121">Terv létrehozása hozzárendelés-fájlon keresztül</span><span class="sxs-lookup"><span data-stu-id="de72d-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="de72d-122">A hozzárendelés-fájl formátuma megtalálható a kérés/válasz mintájában: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="de72d-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="de72d-123">Példa 5</span><span class="sxs-lookup"><span data-stu-id="de72d-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="de72d-124">Hozzon létre egy új Blueprint-feladatot a terv definíciójában a meghatározott `$blueprintObject` kezelési csoportban megadott előfizetéshez a megadott paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="de72d-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="de72d-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de72d-125">PARAMETERS</span></span>

### <span data-ttu-id="de72d-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="de72d-126">-AssignmentFile</span></span>
<span data-ttu-id="de72d-127">A hozzárendelt fájl helye JSON formátumban a lemezen.</span><span class="sxs-lookup"><span data-stu-id="de72d-127">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="de72d-128">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="de72d-128">-Blueprint</span></span>
<span data-ttu-id="de72d-129">Blueprint definition objektum.</span><span class="sxs-lookup"><span data-stu-id="de72d-129">Blueprint definition object.</span></span>

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

### <span data-ttu-id="de72d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de72d-130">-DefaultProfile</span></span>
<span data-ttu-id="de72d-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de72d-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de72d-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="de72d-132">-Location</span></span>
<span data-ttu-id="de72d-133">Annak a tartománynak a neve, amelyhez a felügyelt identitást létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="de72d-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="de72d-134">További információ a aka.ms/blueprintmsi-on</span><span class="sxs-lookup"><span data-stu-id="de72d-134">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="de72d-135">-Lock</span><span class="sxs-lookup"><span data-stu-id="de72d-135">-Lock</span></span>
<span data-ttu-id="de72d-136">Erőforrások zárolása</span><span class="sxs-lookup"><span data-stu-id="de72d-136">Lock resources.</span></span>
<span data-ttu-id="de72d-137">További információ a aka.ms/blueprintlocks-on</span><span class="sxs-lookup"><span data-stu-id="de72d-137">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="de72d-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="de72d-138">-ManagementGroupId</span></span>
<span data-ttu-id="de72d-139">Annak a kezelési csoportnak az azonosítója, amelybe a Blueprint-hozzárendelés (oka) t menti.</span><span class="sxs-lookup"><span data-stu-id="de72d-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="de72d-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de72d-140">-Name</span></span>
<span data-ttu-id="de72d-141">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="de72d-141">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="de72d-142">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="de72d-142">-Parameter</span></span>
<span data-ttu-id="de72d-143">A tárgy paraméterei.</span><span class="sxs-lookup"><span data-stu-id="de72d-143">Artifact parameters.</span></span>

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

### <span data-ttu-id="de72d-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="de72d-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="de72d-145">A Hashtable az erőforráscsoport tárgyát adja át.</span><span class="sxs-lookup"><span data-stu-id="de72d-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="de72d-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="de72d-146">-SecureStringParameter</span></span>
<span data-ttu-id="de72d-147">A "biztonságos karakterlánc" paraméter a "a" parancshoz, név és verzió.</span><span class="sxs-lookup"><span data-stu-id="de72d-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="de72d-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de72d-148">-SubscriptionId</span></span>
<span data-ttu-id="de72d-149">Előfizetés azonosítója: a terv definíciójának hozzárendelése.</span><span class="sxs-lookup"><span data-stu-id="de72d-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="de72d-150">A subscriptionId-karakterláncok vesszővel elválasztott listája lehet.</span><span class="sxs-lookup"><span data-stu-id="de72d-150">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="de72d-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="de72d-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="de72d-152">A rendszerhez rendelt identitás (MSI) a leletek központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="de72d-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="de72d-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="de72d-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="de72d-154">A felhasználó által kiosztott identitás (MSI) a leletek üzembe helyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="de72d-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="de72d-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de72d-155">-Confirm</span></span>
<span data-ttu-id="de72d-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de72d-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de72d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de72d-157">-WhatIf</span></span>
<span data-ttu-id="de72d-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de72d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de72d-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de72d-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de72d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de72d-160">CommonParameters</span></span>
<span data-ttu-id="de72d-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de72d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de72d-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de72d-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de72d-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de72d-163">INPUTS</span></span>

### <span data-ttu-id="de72d-164">System. String</span><span class="sxs-lookup"><span data-stu-id="de72d-164">System.String</span></span>

### <span data-ttu-id="de72d-165">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="de72d-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="de72d-166">System. string []</span><span class="sxs-lookup"><span data-stu-id="de72d-166">System.String[]</span></span>

### <span data-ttu-id="de72d-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="de72d-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="de72d-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de72d-168">OUTPUTS</span></span>

### <span data-ttu-id="de72d-169">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="de72d-169">System.Object</span></span>
## <span data-ttu-id="de72d-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de72d-170">NOTES</span></span>

## <span data-ttu-id="de72d-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de72d-171">RELATED LINKS</span></span>
