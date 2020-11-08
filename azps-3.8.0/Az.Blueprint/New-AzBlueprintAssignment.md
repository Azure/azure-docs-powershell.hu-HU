---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 72c57f8310aaffdbe3c4afa38564c10132539749
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010636"
---
# <span data-ttu-id="e932a-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e932a-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e932a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e932a-102">SYNOPSIS</span></span>
<span data-ttu-id="e932a-103">Tervrajz-definíció hozzárendelése előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="e932a-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="e932a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e932a-104">SYNTAX</span></span>

### <span data-ttu-id="e932a-105">CreateBlueprintAssignment (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e932a-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e932a-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="e932a-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e932a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e932a-107">DESCRIPTION</span></span>
<span data-ttu-id="e932a-108">Tervrajz-definíció hozzárendelése előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="e932a-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="e932a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e932a-109">EXAMPLES</span></span>

### <span data-ttu-id="e932a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e932a-110">Example 1</span></span>
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

<span data-ttu-id="e932a-111">Hozzon létre egy új tervrajzot a terv definíciója alapján a `$blueprintObject` megadott előfizetésből a megadott paraméter és erőforráscsoport szótár használatával.</span><span class="sxs-lookup"><span data-stu-id="e932a-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="e932a-112">A rendszer által hozzárendelt identitást használja.</span><span class="sxs-lookup"><span data-stu-id="e932a-112">Uses system-assigned identity.</span></span> <span data-ttu-id="e932a-113">A hely határozza meg a felügyelt identitás létrehozásának területét.</span><span class="sxs-lookup"><span data-stu-id="e932a-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="e932a-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e932a-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="e932a-115">Hozzon létre egy új tervrajzot a terv definíciója alapján a `$blueprintObject` megadott előfizetésben a definiált paraméter és erőforráscsoport szótár segítségével, és konfigurálja az erőforrás-zárolást a **AllResources** -ra.</span><span class="sxs-lookup"><span data-stu-id="e932a-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="e932a-116">Alapértelmezések a rendszerszintű identitás használatához</span><span class="sxs-lookup"><span data-stu-id="e932a-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="e932a-117">A hely határozza meg a felügyelt identitás létrehozásának területét.</span><span class="sxs-lookup"><span data-stu-id="e932a-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="e932a-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="e932a-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="e932a-119">Hozzon létre egy új tervrajzot a terv definíciója alapján a `$blueprintObject` megadott előfizetésben a megadott paraméter és erőforráscsoport szótár segítségével a megadott felhasználó által kiosztott azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="e932a-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="e932a-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="e932a-120">Example 4</span></span>
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

<span data-ttu-id="e932a-121">Terv létrehozása hozzárendelés-fájlon keresztül</span><span class="sxs-lookup"><span data-stu-id="e932a-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="e932a-122">A hozzárendelés-fájl formátuma megtalálható a kérés/válasz mintájában: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="e932a-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="e932a-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e932a-123">PARAMETERS</span></span>

### <span data-ttu-id="e932a-124">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="e932a-124">-Blueprint</span></span>
<span data-ttu-id="e932a-125">Blueprint definition objektum.</span><span class="sxs-lookup"><span data-stu-id="e932a-125">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e932a-126">-DefaultProfile</span></span>
<span data-ttu-id="e932a-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e932a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e932a-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="e932a-128">-Location</span></span>
<span data-ttu-id="e932a-129">Annak a tartománynak a neve, amelyhez a felügyelt identitást létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="e932a-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="e932a-130">További információ a aka.ms/blueprintmsi-on</span><span class="sxs-lookup"><span data-stu-id="e932a-130">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="e932a-131">-Lock</span><span class="sxs-lookup"><span data-stu-id="e932a-131">-Lock</span></span>
<span data-ttu-id="e932a-132">Erőforrások zárolása</span><span class="sxs-lookup"><span data-stu-id="e932a-132">Lock resources.</span></span>
<span data-ttu-id="e932a-133">További információ a aka.ms/blueprintlocks-on</span><span class="sxs-lookup"><span data-stu-id="e932a-133">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e932a-134">-Name</span></span>
<span data-ttu-id="e932a-135">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="e932a-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="e932a-136">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="e932a-136">-Parameter</span></span>
<span data-ttu-id="e932a-137">A tárgy paraméterei.</span><span class="sxs-lookup"><span data-stu-id="e932a-137">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e932a-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="e932a-139">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="e932a-139">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="e932a-140">-SecureStringParameter</span></span>
<span data-ttu-id="e932a-141">A "biztonságos karakterlánc" paraméter a "a" parancshoz, név és verzió.</span><span class="sxs-lookup"><span data-stu-id="e932a-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e932a-142">-SubscriptionId</span></span>
<span data-ttu-id="e932a-143">Előfizetés azonosítója: a terv definíciójának hozzárendelése.</span><span class="sxs-lookup"><span data-stu-id="e932a-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="e932a-144">A subscriptionId-karakterláncok vesszővel elválasztott listája lehet.</span><span class="sxs-lookup"><span data-stu-id="e932a-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="e932a-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e932a-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e932a-146">A rendszerhez rendelt identitás (MSI) a leletek központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="e932a-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e932a-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e932a-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="e932a-148">A felhasználó által kiosztott identitás (MSI) a leletek üzembe helyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="e932a-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e932a-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e932a-149">-Confirm</span></span>
<span data-ttu-id="e932a-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e932a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e932a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e932a-151">-WhatIf</span></span>
<span data-ttu-id="e932a-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e932a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e932a-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e932a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e932a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e932a-154">CommonParameters</span></span>
<span data-ttu-id="e932a-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e932a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e932a-156">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e932a-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e932a-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e932a-157">INPUTS</span></span>

### <span data-ttu-id="e932a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="e932a-158">System.String</span></span>

### <span data-ttu-id="e932a-159">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="e932a-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e932a-160">System. string []</span><span class="sxs-lookup"><span data-stu-id="e932a-160">System.String[]</span></span>

### <span data-ttu-id="e932a-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e932a-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e932a-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e932a-162">OUTPUTS</span></span>

### <span data-ttu-id="e932a-163">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="e932a-163">System.Object</span></span>
## <span data-ttu-id="e932a-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e932a-164">NOTES</span></span>

## <span data-ttu-id="e932a-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e932a-165">RELATED LINKS</span></span>
