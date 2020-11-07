---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836863"
---
# <span data-ttu-id="d03cc-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="d03cc-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="d03cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d03cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d03cc-103">Tervrajz-definíció hozzárendelése előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="d03cc-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="d03cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d03cc-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d03cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d03cc-105">DESCRIPTION</span></span>
<span data-ttu-id="d03cc-106">Tervrajz-definíció hozzárendelése előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="d03cc-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="d03cc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d03cc-107">EXAMPLES</span></span>

### <span data-ttu-id="d03cc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d03cc-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="d03cc-109">Hozzon létre egy új tervrajzot a terv definíciója alapján a `$blueprintObject` megadott előfizetésből a megadott paraméter és erőforráscsoport szótár használatával.</span><span class="sxs-lookup"><span data-stu-id="d03cc-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="d03cc-110">A rendszer által hozzárendelt identitást használja.</span><span class="sxs-lookup"><span data-stu-id="d03cc-110">Uses system-assigned identity.</span></span> <span data-ttu-id="d03cc-111">A hely határozza meg a felügyelt identitás létrehozásának területét.</span><span class="sxs-lookup"><span data-stu-id="d03cc-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="d03cc-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d03cc-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="d03cc-113">Hozzon létre egy új tervrajzot a terv definíciója alapján a `$blueprintObject` megadott előfizetésben a definiált paraméter és erőforráscsoport szótár segítségével, és konfigurálja az erőforrás-zárolást a **AllResources** -ra.</span><span class="sxs-lookup"><span data-stu-id="d03cc-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="d03cc-114">Alapértelmezések a rendszerszintű identitás használatához</span><span class="sxs-lookup"><span data-stu-id="d03cc-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="d03cc-115">A hely határozza meg a felügyelt identitás létrehozásának területét.</span><span class="sxs-lookup"><span data-stu-id="d03cc-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="d03cc-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="d03cc-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="d03cc-117">Hozzon létre egy új tervrajzot a terv definíciója alapján a `$blueprintObject` megadott előfizetésben a megadott paraméter és erőforráscsoport szótár segítségével a megadott felhasználó által kiosztott azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="d03cc-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="d03cc-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d03cc-118">PARAMETERS</span></span>

### <span data-ttu-id="d03cc-119">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="d03cc-119">-Blueprint</span></span>
<span data-ttu-id="d03cc-120">Blueprint definition objektum.</span><span class="sxs-lookup"><span data-stu-id="d03cc-120">Blueprint definition object.</span></span>

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

### <span data-ttu-id="d03cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03cc-121">-DefaultProfile</span></span>
<span data-ttu-id="d03cc-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d03cc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d03cc-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="d03cc-123">-Location</span></span>
<span data-ttu-id="d03cc-124">Annak a tartománynak a neve, amelyhez a felügyelt identitást létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="d03cc-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="d03cc-125">További információ a aka.ms/blueprintmsi-on</span><span class="sxs-lookup"><span data-stu-id="d03cc-125">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="d03cc-126">-Lock</span><span class="sxs-lookup"><span data-stu-id="d03cc-126">-Lock</span></span>
<span data-ttu-id="d03cc-127">Erőforrások zárolása</span><span class="sxs-lookup"><span data-stu-id="d03cc-127">Lock resources.</span></span>
<span data-ttu-id="d03cc-128">További információ a aka.ms/blueprintlocks-on</span><span class="sxs-lookup"><span data-stu-id="d03cc-128">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="d03cc-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d03cc-129">-Name</span></span>
<span data-ttu-id="d03cc-130">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="d03cc-130">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="d03cc-131">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="d03cc-131">-Parameter</span></span>
<span data-ttu-id="d03cc-132">A tárgy paraméterei.</span><span class="sxs-lookup"><span data-stu-id="d03cc-132">Artifact parameters.</span></span>

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

### <span data-ttu-id="d03cc-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="d03cc-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="d03cc-134">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="d03cc-134">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="d03cc-135">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="d03cc-135">-SecureStringParameter</span></span>
<span data-ttu-id="d03cc-136">A "biztonságos karakterlánc" paraméter a "a" parancshoz, név és verzió.</span><span class="sxs-lookup"><span data-stu-id="d03cc-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="d03cc-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d03cc-137">-SubscriptionId</span></span>
<span data-ttu-id="d03cc-138">Előfizetés azonosítója: a terv definíciójának hozzárendelése.</span><span class="sxs-lookup"><span data-stu-id="d03cc-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="d03cc-139">A subscriptionId-karakterláncok vesszővel elválasztott listája lehet.</span><span class="sxs-lookup"><span data-stu-id="d03cc-139">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="d03cc-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d03cc-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="d03cc-141">A rendszerhez rendelt identitás (MSI) a leletek központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d03cc-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="d03cc-142">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d03cc-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="d03cc-143">A felhasználó által kiosztott identitás (MSI) a leletek üzembe helyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d03cc-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="d03cc-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d03cc-144">-Confirm</span></span>
<span data-ttu-id="d03cc-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d03cc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d03cc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d03cc-146">-WhatIf</span></span>
<span data-ttu-id="d03cc-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d03cc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d03cc-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d03cc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d03cc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03cc-149">CommonParameters</span></span>
<span data-ttu-id="d03cc-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d03cc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03cc-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d03cc-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03cc-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d03cc-152">INPUTS</span></span>

### <span data-ttu-id="d03cc-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d03cc-153">System.String</span></span>

### <span data-ttu-id="d03cc-154">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="d03cc-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="d03cc-155">System. string []</span><span class="sxs-lookup"><span data-stu-id="d03cc-155">System.String[]</span></span>

### <span data-ttu-id="d03cc-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d03cc-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d03cc-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d03cc-157">OUTPUTS</span></span>

### <span data-ttu-id="d03cc-158">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="d03cc-158">System.Object</span></span>
## <span data-ttu-id="d03cc-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d03cc-159">NOTES</span></span>

## <span data-ttu-id="d03cc-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d03cc-160">RELATED LINKS</span></span>
