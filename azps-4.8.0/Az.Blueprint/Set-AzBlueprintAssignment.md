---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180604"
---
# <span data-ttu-id="dd389-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="dd389-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="dd389-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd389-102">SYNOPSIS</span></span>
<span data-ttu-id="dd389-103">Meglévő tervrajz-hozzárendelés frissítése</span><span class="sxs-lookup"><span data-stu-id="dd389-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="dd389-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd389-104">SYNTAX</span></span>

### <span data-ttu-id="dd389-105">UpdateBlueprintAssignment (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd389-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd389-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="dd389-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd389-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd389-107">DESCRIPTION</span></span>
<span data-ttu-id="dd389-108">Meglévő tervrajz-hozzárendelés frissítése</span><span class="sxs-lookup"><span data-stu-id="dd389-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="dd389-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dd389-109">EXAMPLES</span></span>

### <span data-ttu-id="dd389-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd389-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="dd389-111">A megadott előfizetésben a terv meghatározásának meglévő tervrajz-hozzárendelését frissítheti `$blueprintObject` , frissítheti a paramétereket.</span><span class="sxs-lookup"><span data-stu-id="dd389-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="dd389-112">A rendszer által hozzárendelt identitást használja.</span><span class="sxs-lookup"><span data-stu-id="dd389-112">Uses system-assigned identity.</span></span> <span data-ttu-id="dd389-113">A hely határozza meg a felügyelt identitás létrehozásának területét.</span><span class="sxs-lookup"><span data-stu-id="dd389-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="dd389-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="dd389-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="dd389-115">Egy hozzárendelés-fájlon keresztül frissítheti a meglévő terv hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="dd389-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="dd389-116">A hozzárendelés-fájl formátuma megtalálható a kérés/válasz mintájában: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="dd389-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="dd389-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="dd389-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="dd389-118">A terv definíciójának egy meglévő tervrajz-hozzárendelését frissítheti a `$blueprintObject` definiált paraméterrel meghatározott kezelési csoportban megadott előfizetésre.</span><span class="sxs-lookup"><span data-stu-id="dd389-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="dd389-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd389-119">PARAMETERS</span></span>

### <span data-ttu-id="dd389-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="dd389-120">-AssignmentFile</span></span>
<span data-ttu-id="dd389-121">A hozzárendelt fájl helye JSON formátumban a lemezen.</span><span class="sxs-lookup"><span data-stu-id="dd389-121">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="dd389-122">-Blueprint</span></span>
<span data-ttu-id="dd389-123">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="dd389-123">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd389-124">-DefaultProfile</span></span>
<span data-ttu-id="dd389-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd389-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd389-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="dd389-126">-Location</span></span>
<span data-ttu-id="dd389-127">Annak a tartománynak a neve, amelyhez a felügyelt identitást létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="dd389-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="dd389-128">További információ a aka.ms/blueprintmsi-on</span><span class="sxs-lookup"><span data-stu-id="dd389-128">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="dd389-129">-Lock</span></span>
<span data-ttu-id="dd389-130">Erőforrások zárolása</span><span class="sxs-lookup"><span data-stu-id="dd389-130">Lock resources.</span></span>
<span data-ttu-id="dd389-131">További információ a aka.ms/blueprintlocks-on</span><span class="sxs-lookup"><span data-stu-id="dd389-131">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: UpdateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="dd389-132">-ManagementGroupId</span></span>
<span data-ttu-id="dd389-133">Annak a kezelési csoportnak az azonosítója, amelybe a Blueprint-hozzárendelés (oka) t menti.</span><span class="sxs-lookup"><span data-stu-id="dd389-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd389-134">-Name</span></span>
<span data-ttu-id="dd389-135">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="dd389-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-136">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="dd389-136">-Parameter</span></span>
<span data-ttu-id="dd389-137">Eltérés paraméter</span><span class="sxs-lookup"><span data-stu-id="dd389-137">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="dd389-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="dd389-139">A Hashtable az erőforráscsoport tárgyát adja át.</span><span class="sxs-lookup"><span data-stu-id="dd389-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="dd389-140">-SecureStringParameter</span></span>
<span data-ttu-id="dd389-141">A "biztonságos karakterlánc" paraméter a "a" parancshoz, név és verzió.</span><span class="sxs-lookup"><span data-stu-id="dd389-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd389-142">-SubscriptionId</span></span>
<span data-ttu-id="dd389-143">SubscriptionId a tervezet hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="dd389-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="dd389-144">A subscriptionId-karakterláncok vesszővel elválasztott listája lehet.</span><span class="sxs-lookup"><span data-stu-id="dd389-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="dd389-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="dd389-146">A rendszerhez rendelt identitás (MSI) a leletek központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="dd389-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="dd389-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="dd389-148">A felhasználó által kiosztott identitás (MSI) a leletek üzembe helyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="dd389-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd389-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd389-149">-Confirm</span></span>
<span data-ttu-id="dd389-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd389-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd389-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd389-151">-WhatIf</span></span>
<span data-ttu-id="dd389-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd389-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd389-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd389-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd389-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd389-154">CommonParameters</span></span>
<span data-ttu-id="dd389-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd389-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd389-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dd389-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd389-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd389-157">INPUTS</span></span>

### <span data-ttu-id="dd389-158">System. String</span><span class="sxs-lookup"><span data-stu-id="dd389-158">System.String</span></span>

### <span data-ttu-id="dd389-159">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="dd389-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="dd389-160">System. string []</span><span class="sxs-lookup"><span data-stu-id="dd389-160">System.String[]</span></span>

### <span data-ttu-id="dd389-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dd389-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dd389-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd389-162">OUTPUTS</span></span>

### <span data-ttu-id="dd389-163">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="dd389-163">System.Object</span></span>
## <span data-ttu-id="dd389-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd389-164">NOTES</span></span>

## <span data-ttu-id="dd389-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd389-165">RELATED LINKS</span></span>
