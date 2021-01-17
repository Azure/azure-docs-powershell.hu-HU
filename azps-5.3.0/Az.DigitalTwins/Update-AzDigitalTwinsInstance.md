---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 4de7ab82f60c651e23565569ccf2cda7f4d949b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467749"
---
# <span data-ttu-id="de76c-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="de76c-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="de76c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de76c-102">SYNOPSIS</span></span>
<span data-ttu-id="de76c-103">A DigitalTwinsInstance metaadatainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="de76c-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="de76c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="de76c-104">SYNTAX</span></span>

### <span data-ttu-id="de76c-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de76c-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="de76c-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="de76c-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="de76c-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="de76c-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="de76c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="de76c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de76c-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="de76c-109">DESCRIPTION</span></span>
<span data-ttu-id="de76c-110">A DigitalTwinsInstance metaadatainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="de76c-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="de76c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="de76c-111">EXAMPLES</span></span>

### <span data-ttu-id="de76c-112">1. példa: UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de76c-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="de76c-113">A megadott DigitalTwinsInstance by ResourceGroupName frissítése</span><span class="sxs-lookup"><span data-stu-id="de76c-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="de76c-114">2. példa: Az AzDigitalTwinsInstance frissítése egy másik AzDigitalTwinsInstance szerint</span><span class="sxs-lookup"><span data-stu-id="de76c-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="de76c-115">Az AzDigitalTwinsInstance újabb AzDigitalTwinsInstance frissítése</span><span class="sxs-lookup"><span data-stu-id="de76c-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="de76c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de76c-116">PARAMETERS</span></span>

### <span data-ttu-id="de76c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de76c-117">-DefaultProfile</span></span>
<span data-ttu-id="de76c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de76c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de76c-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="de76c-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="de76c-120">A DigitalTwins szolgáltatás leírása.</span><span class="sxs-lookup"><span data-stu-id="de76c-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="de76c-121">Ennek létrehozásáról a DIGITALTWINSPATCHDESCRIPTION tulajdonságokat ismertető MEGJEGYZÉSEK című szakaszban és egy kivonattáblát hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="de76c-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de76c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de76c-122">-InputObject</span></span>
<span data-ttu-id="de76c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="de76c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de76c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de76c-124">-ResourceGroupName</span></span>
<span data-ttu-id="de76c-125">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de76c-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76c-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="de76c-126">-ResourceName</span></span>
<span data-ttu-id="de76c-127">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="de76c-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de76c-128">-SubscriptionId</span></span>
<span data-ttu-id="de76c-129">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="de76c-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="de76c-130">-Tag</span></span>
<span data-ttu-id="de76c-131">Példánycímkék</span><span class="sxs-lookup"><span data-stu-id="de76c-131">Instance tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de76c-132">-Confirm</span></span>
<span data-ttu-id="de76c-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="de76c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de76c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de76c-134">-WhatIf</span></span>
<span data-ttu-id="de76c-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="de76c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de76c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de76c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de76c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de76c-137">CommonParameters</span></span>
<span data-ttu-id="de76c-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de76c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de76c-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de76c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de76c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de76c-140">INPUTS</span></span>

### <span data-ttu-id="de76c-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="de76c-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="de76c-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="de76c-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="de76c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de76c-143">OUTPUTS</span></span>

### <span data-ttu-id="de76c-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="de76c-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="de76c-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="de76c-145">NOTES</span></span>

<span data-ttu-id="de76c-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="de76c-146">ALIASES</span></span>

<span data-ttu-id="de76c-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="de76c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="de76c-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="de76c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de76c-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="de76c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="de76c-150">DIGITALTWINSPATCHDESCRIPTION: <IDigitalTwinsPatchDescription> A DigitalTwins szolgáltatás leírása.</span><span class="sxs-lookup"><span data-stu-id="de76c-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="de76c-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Példánycímkék</span><span class="sxs-lookup"><span data-stu-id="de76c-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="de76c-152">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="de76c-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="de76c-153">INPUTOBJECT: <IDigitalTwinsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="de76c-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="de76c-154">`[EndpointName <String>]`: A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="de76c-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="de76c-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="de76c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="de76c-156">`[Location <String>]`: A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="de76c-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="de76c-157">`[ResourceGroupName <String>]`: A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de76c-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="de76c-158">`[ResourceName <String>]`: A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="de76c-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="de76c-159">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="de76c-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="de76c-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de76c-160">RELATED LINKS</span></span>

