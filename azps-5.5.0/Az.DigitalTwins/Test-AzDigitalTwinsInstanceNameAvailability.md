---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204159"
---
# <span data-ttu-id="ee6f0-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ee6f0-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="ee6f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee6f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ee6f0-103">Ellenőrizze, hogy elérhető-e DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="ee6f0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee6f0-104">SYNTAX</span></span>

### <span data-ttu-id="ee6f0-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee6f0-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ee6f0-106">Ellenőrzés</span><span class="sxs-lookup"><span data-stu-id="ee6f0-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ee6f0-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ee6f0-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ee6f0-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ee6f0-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee6f0-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee6f0-109">DESCRIPTION</span></span>
<span data-ttu-id="ee6f0-110">Ellenőrizze, hogy elérhető-e DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="ee6f0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee6f0-111">EXAMPLES</span></span>

### <span data-ttu-id="ee6f0-112">1. példa: Ellenőrizze a nevet hely és név szerint.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="ee6f0-113">Ellenőrizze a név elérhetőségét hely és név szerint.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="ee6f0-114">2. példa: Ellenőrizze a nevet DigitalTwinsObject és CheckNameObject szerint.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="ee6f0-115">A DigitalTwinsInstance függvényt bevetve létrehozhat egy Requset Objektumot a név elérhetőségének tesztelésére.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="ee6f0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee6f0-116">PARAMETERS</span></span>

### <span data-ttu-id="ee6f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee6f0-117">-DefaultProfile</span></span>
<span data-ttu-id="ee6f0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6f0-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="ee6f0-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="ee6f0-120">Az adatbázis-ellenőrzés elérhetőségi kérelmének eredménye.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="ee6f0-121">Ennek létrehozásához lásd a DIGITALTWINSINSTANCECHECKNAME tulajdonságokAT, és hozzon létre egy kivonattáblát a MEGJEGYZÉSEK szakaszban.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee6f0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee6f0-122">-InputObject</span></span>
<span data-ttu-id="ee6f0-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee6f0-124">-Location</span><span class="sxs-lookup"><span data-stu-id="ee6f0-124">-Location</span></span>
<span data-ttu-id="ee6f0-125">A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-125">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6f0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ee6f0-126">-Name</span></span>
<span data-ttu-id="ee6f0-127">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-127">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6f0-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee6f0-128">-SubscriptionId</span></span>
<span data-ttu-id="ee6f0-129">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6f0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee6f0-130">-Confirm</span></span>
<span data-ttu-id="ee6f0-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee6f0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee6f0-132">-WhatIf</span></span>
<span data-ttu-id="ee6f0-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee6f0-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee6f0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee6f0-135">CommonParameters</span></span>
<span data-ttu-id="ee6f0-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee6f0-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee6f0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee6f0-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee6f0-138">INPUTS</span></span>

### <span data-ttu-id="ee6f0-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="ee6f0-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="ee6f0-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="ee6f0-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="ee6f0-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee6f0-141">OUTPUTS</span></span>

### <span data-ttu-id="ee6f0-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ee6f0-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="ee6f0-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee6f0-143">NOTES</span></span>

<span data-ttu-id="ee6f0-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ee6f0-144">ALIASES</span></span>

<span data-ttu-id="ee6f0-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ee6f0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee6f0-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee6f0-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee6f0-148">DIGITALTWINSINSTANCECHECKNAME: Az adatbázis-ellenőrzés név-elérhetőségi kéréséből <ICheckNameRequest> visszaadott eredmény.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="ee6f0-149">`Name <String>`: Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="ee6f0-150">INPUTOBJECT: <IDigitalTwinsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ee6f0-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee6f0-151">`[EndpointName <String>]`: A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="ee6f0-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ee6f0-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee6f0-153">`[Location <String>]`: A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ee6f0-154">`[ResourceGroupName <String>]`: A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ee6f0-155">`[ResourceName <String>]`: A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ee6f0-156">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee6f0-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="ee6f0-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee6f0-157">RELATED LINKS</span></span>

