---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326545"
---
# <span data-ttu-id="055ad-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="055ad-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="055ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="055ad-102">SYNOPSIS</span></span>
<span data-ttu-id="055ad-103">Frissítheti a meglévő terv-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="055ad-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="055ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="055ad-104">SYNTAX</span></span>

### <span data-ttu-id="055ad-105">UpdateBlueprintAssignment (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="055ad-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="055ad-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="055ad-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="055ad-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="055ad-107">DESCRIPTION</span></span>
<span data-ttu-id="055ad-108">Frissítheti a meglévő terv-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="055ad-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="055ad-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="055ad-109">EXAMPLES</span></span>

### <span data-ttu-id="055ad-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="055ad-110">Example 1</span></span>
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

<span data-ttu-id="055ad-111">Frissítse a tervdefiníció meglévő hozzárendelését a megadott előfizetésen belül, és frissítse `$blueprintObject` a paramétereket.</span><span class="sxs-lookup"><span data-stu-id="055ad-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="055ad-112">Rendszer által hozzárendelt identitást használ.</span><span class="sxs-lookup"><span data-stu-id="055ad-112">Uses system-assigned identity.</span></span> <span data-ttu-id="055ad-113">A hely határozza meg a felügyelt identitás létrehozására vonatkozó régiót.</span><span class="sxs-lookup"><span data-stu-id="055ad-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="055ad-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="055ad-114">Example 2</span></span>
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

<span data-ttu-id="055ad-115">Frissítheti egy meglévő terv-hozzárendelést egy feladatfájlon keresztül.</span><span class="sxs-lookup"><span data-stu-id="055ad-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="055ad-116">A feladatfájl formátuma megtalálható a kérelem/válasz mintáiban: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="055ad-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="055ad-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="055ad-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="055ad-118">A megadott felügyeleti csoporton belül a megadott előfizetésre vonatkozó tervrajz-hozzárendelés frissítése a `$blueprintObject` megadott paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="055ad-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="055ad-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="055ad-119">PARAMETERS</span></span>

### <span data-ttu-id="055ad-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="055ad-120">-AssignmentFile</span></span>
<span data-ttu-id="055ad-121">A feladatfájl helye lemezen JSON formátumban.</span><span class="sxs-lookup"><span data-stu-id="055ad-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="055ad-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="055ad-122">-Blueprint</span></span>
<span data-ttu-id="055ad-123">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="055ad-123">Blueprint object.</span></span>

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

### <span data-ttu-id="055ad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055ad-124">-DefaultProfile</span></span>
<span data-ttu-id="055ad-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="055ad-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="055ad-126">-Location</span><span class="sxs-lookup"><span data-stu-id="055ad-126">-Location</span></span>
<span data-ttu-id="055ad-127">Régió, ahol a felügyelt identitást létre kell hoznunk.</span><span class="sxs-lookup"><span data-stu-id="055ad-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="055ad-128">További információ a aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="055ad-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="055ad-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="055ad-129">-Lock</span></span>
<span data-ttu-id="055ad-130">Erőforrások zárolása</span><span class="sxs-lookup"><span data-stu-id="055ad-130">Lock resources.</span></span>
<span data-ttu-id="055ad-131">További információ a aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="055ad-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="055ad-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="055ad-132">-ManagementGroupId</span></span>
<span data-ttu-id="055ad-133">Annak a felügyeleti csoportnak az azonosítója, amelybe a Tervrajz hozzárendelés(eket) menti a rendszer.</span><span class="sxs-lookup"><span data-stu-id="055ad-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="055ad-134">-Name</span><span class="sxs-lookup"><span data-stu-id="055ad-134">-Name</span></span>
<span data-ttu-id="055ad-135">A terv feladatának neve.</span><span class="sxs-lookup"><span data-stu-id="055ad-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="055ad-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="055ad-136">-Parameter</span></span>
<span data-ttu-id="055ad-137">Összetevő paramétere.</span><span class="sxs-lookup"><span data-stu-id="055ad-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="055ad-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="055ad-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="055ad-139">Az erőforráscsoport-összetevőnek átadni szükséges paraméterek kivonata.</span><span class="sxs-lookup"><span data-stu-id="055ad-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="055ad-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="055ad-140">-SecureStringParameter</span></span>
<span data-ttu-id="055ad-141">Secure string parameter for KeyVault resource id, name and version.</span><span class="sxs-lookup"><span data-stu-id="055ad-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="055ad-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="055ad-142">-SubscriptionId</span></span>
<span data-ttu-id="055ad-143">SubscriptionId to assign the Blueprint.</span><span class="sxs-lookup"><span data-stu-id="055ad-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="055ad-144">Az előfizetésazonosító karakterláncai vesszővel tagolt listája lehet.</span><span class="sxs-lookup"><span data-stu-id="055ad-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="055ad-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="055ad-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="055ad-146">A rendszer által hozzárendelt identitás(MSI) az összetevők telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="055ad-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="055ad-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="055ad-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="055ad-148">Felhasználó által hozzárendelt identitás(MSI) az összetevők telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="055ad-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="055ad-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="055ad-149">-Confirm</span></span>
<span data-ttu-id="055ad-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="055ad-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="055ad-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="055ad-151">-WhatIf</span></span>
<span data-ttu-id="055ad-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="055ad-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="055ad-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="055ad-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="055ad-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055ad-154">CommonParameters</span></span>
<span data-ttu-id="055ad-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="055ad-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055ad-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="055ad-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055ad-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="055ad-157">INPUTS</span></span>

### <span data-ttu-id="055ad-158">System.String</span><span class="sxs-lookup"><span data-stu-id="055ad-158">System.String</span></span>

### <span data-ttu-id="055ad-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="055ad-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="055ad-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="055ad-160">System.String[]</span></span>

### <span data-ttu-id="055ad-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="055ad-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="055ad-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="055ad-162">OUTPUTS</span></span>

### <span data-ttu-id="055ad-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="055ad-163">System.Object</span></span>
## <span data-ttu-id="055ad-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="055ad-164">NOTES</span></span>

## <span data-ttu-id="055ad-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="055ad-165">RELATED LINKS</span></span>
