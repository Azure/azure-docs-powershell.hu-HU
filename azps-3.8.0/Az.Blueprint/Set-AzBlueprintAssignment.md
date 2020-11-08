---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 418bb8a9ba8362e799d619705eccdc60e5418fc9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010986"
---
# <span data-ttu-id="53309-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="53309-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="53309-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53309-102">SYNOPSIS</span></span>
<span data-ttu-id="53309-103">Meglévő tervrajz-hozzárendelés frissítése</span><span class="sxs-lookup"><span data-stu-id="53309-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="53309-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53309-104">SYNTAX</span></span>

### <span data-ttu-id="53309-105">UpdateBlueprintAssignment (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53309-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53309-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="53309-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53309-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="53309-107">DESCRIPTION</span></span>
<span data-ttu-id="53309-108">Meglévő tervrajz-hozzárendelés frissítése</span><span class="sxs-lookup"><span data-stu-id="53309-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="53309-109">Példák</span><span class="sxs-lookup"><span data-stu-id="53309-109">EXAMPLES</span></span>

### <span data-ttu-id="53309-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="53309-110">Example 1</span></span>
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

<span data-ttu-id="53309-111">A megadott előfizetésben a terv meghatározásának meglévő tervrajz-hozzárendelését frissítheti `$blueprintObject` , frissítheti a paramétereket.</span><span class="sxs-lookup"><span data-stu-id="53309-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="53309-112">A rendszer által hozzárendelt identitást használja.</span><span class="sxs-lookup"><span data-stu-id="53309-112">Uses system-assigned identity.</span></span> <span data-ttu-id="53309-113">A hely határozza meg a felügyelt identitás létrehozásának területét.</span><span class="sxs-lookup"><span data-stu-id="53309-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="53309-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="53309-114">Example 2</span></span>
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

<span data-ttu-id="53309-115">Egy hozzárendelés-fájlon keresztül frissítheti a meglévő terv hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="53309-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="53309-116">A hozzárendelés-fájl formátuma megtalálható a kérés/válasz mintájában: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="53309-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="53309-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53309-117">PARAMETERS</span></span>

### <span data-ttu-id="53309-118">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="53309-118">-Blueprint</span></span>
<span data-ttu-id="53309-119">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="53309-119">Blueprint object.</span></span>

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

### <span data-ttu-id="53309-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53309-120">-DefaultProfile</span></span>
<span data-ttu-id="53309-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53309-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53309-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="53309-122">-Location</span></span>
<span data-ttu-id="53309-123">Annak a tartománynak a neve, amelyhez a felügyelt identitást létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="53309-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="53309-124">További információ a aka.ms/blueprintmsi-on</span><span class="sxs-lookup"><span data-stu-id="53309-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="53309-125">-Lock</span><span class="sxs-lookup"><span data-stu-id="53309-125">-Lock</span></span>
<span data-ttu-id="53309-126">Erőforrások zárolása</span><span class="sxs-lookup"><span data-stu-id="53309-126">Lock resources.</span></span>
<span data-ttu-id="53309-127">További információ a aka.ms/blueprintlocks-on</span><span class="sxs-lookup"><span data-stu-id="53309-127">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="53309-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53309-128">-Name</span></span>
<span data-ttu-id="53309-129">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="53309-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="53309-130">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="53309-130">-Parameter</span></span>
<span data-ttu-id="53309-131">Eltérés paraméter</span><span class="sxs-lookup"><span data-stu-id="53309-131">Artifact parameter.</span></span>

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

### <span data-ttu-id="53309-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="53309-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="53309-133">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="53309-133">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="53309-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="53309-134">-SecureStringParameter</span></span>
<span data-ttu-id="53309-135">A "biztonságos karakterlánc" paraméter a "a" parancshoz, név és verzió.</span><span class="sxs-lookup"><span data-stu-id="53309-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="53309-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53309-136">-SubscriptionId</span></span>
<span data-ttu-id="53309-137">SubscriptionId a tervezet hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="53309-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="53309-138">A subscriptionId-karakterláncok vesszővel elválasztott listája lehet.</span><span class="sxs-lookup"><span data-stu-id="53309-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="53309-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="53309-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="53309-140">A rendszerhez rendelt identitás (MSI) a leletek központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="53309-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="53309-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="53309-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="53309-142">A felhasználó által kiosztott identitás (MSI) a leletek üzembe helyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="53309-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="53309-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53309-143">-Confirm</span></span>
<span data-ttu-id="53309-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53309-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53309-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53309-145">-WhatIf</span></span>
<span data-ttu-id="53309-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53309-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53309-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53309-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53309-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53309-148">CommonParameters</span></span>
<span data-ttu-id="53309-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53309-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53309-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53309-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53309-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53309-151">INPUTS</span></span>

### <span data-ttu-id="53309-152">System. String</span><span class="sxs-lookup"><span data-stu-id="53309-152">System.String</span></span>

### <span data-ttu-id="53309-153">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="53309-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="53309-154">System. string []</span><span class="sxs-lookup"><span data-stu-id="53309-154">System.String[]</span></span>

### <span data-ttu-id="53309-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="53309-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="53309-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53309-156">OUTPUTS</span></span>

### <span data-ttu-id="53309-157">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="53309-157">System.Object</span></span>
## <span data-ttu-id="53309-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53309-158">NOTES</span></span>

## <span data-ttu-id="53309-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53309-159">RELATED LINKS</span></span>
