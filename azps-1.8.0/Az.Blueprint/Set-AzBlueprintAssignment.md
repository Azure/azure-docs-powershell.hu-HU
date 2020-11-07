---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836865"
---
# <span data-ttu-id="01c14-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="01c14-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="01c14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01c14-102">SYNOPSIS</span></span>
<span data-ttu-id="01c14-103">Meglévő tervrajz-hozzárendelés frissítése</span><span class="sxs-lookup"><span data-stu-id="01c14-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="01c14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01c14-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c14-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01c14-105">DESCRIPTION</span></span>
<span data-ttu-id="01c14-106">Meglévő tervrajz-hozzárendelés frissítése</span><span class="sxs-lookup"><span data-stu-id="01c14-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="01c14-107">Példák</span><span class="sxs-lookup"><span data-stu-id="01c14-107">EXAMPLES</span></span>

### <span data-ttu-id="01c14-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="01c14-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="01c14-109">A megadott előfizetésben a terv meghatározásának meglévő tervrajz-hozzárendelését frissítheti `$blueprintObject` , frissítheti a paramétereket.</span><span class="sxs-lookup"><span data-stu-id="01c14-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="01c14-110">A rendszer által hozzárendelt identitást használja.</span><span class="sxs-lookup"><span data-stu-id="01c14-110">Uses system-assigned identity.</span></span> <span data-ttu-id="01c14-111">A hely határozza meg a felügyelt identitás létrehozásának területét.</span><span class="sxs-lookup"><span data-stu-id="01c14-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="01c14-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01c14-112">PARAMETERS</span></span>

### <span data-ttu-id="01c14-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="01c14-113">-Blueprint</span></span>
<span data-ttu-id="01c14-114">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="01c14-114">Blueprint object.</span></span>

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

### <span data-ttu-id="01c14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c14-115">-DefaultProfile</span></span>
<span data-ttu-id="01c14-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01c14-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01c14-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="01c14-117">-Location</span></span>
<span data-ttu-id="01c14-118">Annak a tartománynak a neve, amelyhez a felügyelt identitást létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="01c14-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="01c14-119">További információ a aka.ms/blueprintmsi-on</span><span class="sxs-lookup"><span data-stu-id="01c14-119">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="01c14-120">-Lock</span><span class="sxs-lookup"><span data-stu-id="01c14-120">-Lock</span></span>
<span data-ttu-id="01c14-121">Erőforrások zárolása</span><span class="sxs-lookup"><span data-stu-id="01c14-121">Lock resources.</span></span>
<span data-ttu-id="01c14-122">További információ a aka.ms/blueprintlocks-on</span><span class="sxs-lookup"><span data-stu-id="01c14-122">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="01c14-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="01c14-123">-Name</span></span>
<span data-ttu-id="01c14-124">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="01c14-124">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="01c14-125">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="01c14-125">-Parameter</span></span>
<span data-ttu-id="01c14-126">Eltérés paraméter</span><span class="sxs-lookup"><span data-stu-id="01c14-126">Artifact parameter.</span></span>

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

### <span data-ttu-id="01c14-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="01c14-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="01c14-128">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="01c14-128">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="01c14-129">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="01c14-129">-SecureStringParameter</span></span>
<span data-ttu-id="01c14-130">A "biztonságos karakterlánc" paraméter a "a" parancshoz, név és verzió.</span><span class="sxs-lookup"><span data-stu-id="01c14-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="01c14-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01c14-131">-SubscriptionId</span></span>
<span data-ttu-id="01c14-132">SubscriptionId a tervezet hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="01c14-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="01c14-133">A subscriptionId-karakterláncok vesszővel elválasztott listája lehet.</span><span class="sxs-lookup"><span data-stu-id="01c14-133">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="01c14-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="01c14-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="01c14-135">A rendszerhez rendelt identitás (MSI) a leletek központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="01c14-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="01c14-136">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="01c14-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="01c14-137">A felhasználó által kiosztott identitás (MSI) a leletek üzembe helyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="01c14-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="01c14-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="01c14-138">-Confirm</span></span>
<span data-ttu-id="01c14-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="01c14-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c14-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c14-140">-WhatIf</span></span>
<span data-ttu-id="01c14-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="01c14-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c14-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01c14-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c14-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c14-143">CommonParameters</span></span>
<span data-ttu-id="01c14-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01c14-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c14-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01c14-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c14-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01c14-146">INPUTS</span></span>

### <span data-ttu-id="01c14-147">System. String</span><span class="sxs-lookup"><span data-stu-id="01c14-147">System.String</span></span>

### <span data-ttu-id="01c14-148">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="01c14-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="01c14-149">System. string []</span><span class="sxs-lookup"><span data-stu-id="01c14-149">System.String[]</span></span>

### <span data-ttu-id="01c14-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="01c14-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01c14-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01c14-151">OUTPUTS</span></span>

### <span data-ttu-id="01c14-152">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="01c14-152">System.Object</span></span>
## <span data-ttu-id="01c14-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01c14-153">NOTES</span></span>

## <span data-ttu-id="01c14-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01c14-154">RELATED LINKS</span></span>
