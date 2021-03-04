---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: f7d8b5665ff150e0501d77a76c2dde7e4a947cb5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935121"
---
# <span data-ttu-id="2dd1b-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dd1b-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="2dd1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dd1b-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd1b-103">DigitalTwinsInstance végpont törlése.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="2dd1b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2dd1b-104">SYNTAX</span></span>

### <span data-ttu-id="2dd1b-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2dd1b-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2dd1b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2dd1b-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2dd1b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2dd1b-107">DESCRIPTION</span></span>
<span data-ttu-id="2dd1b-108">DigitalTwinsInstance végpont törlése.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="2dd1b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2dd1b-109">EXAMPLES</span></span>

### <span data-ttu-id="2dd1b-110">1. példa: Az AzDigitalTwinsEndPoint törlése endPointName szerint</span><span class="sxs-lookup"><span data-stu-id="2dd1b-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="2dd1b-111">Az AzDigitalTwinsEndPoint by EndPointName ResourceGroupName és ResourceName törlése</span><span class="sxs-lookup"><span data-stu-id="2dd1b-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="2dd1b-112">2. példa: Az azDigitalTwinsEndPoint törlése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="2dd1b-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="2dd1b-113">Az AzDigitalTwinsEndPoint törlése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="2dd1b-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="2dd1b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dd1b-114">PARAMETERS</span></span>

### <span data-ttu-id="2dd1b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dd1b-115">-AsJob</span></span>
<span data-ttu-id="2dd1b-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="2dd1b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2dd1b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd1b-117">-DefaultProfile</span></span>
<span data-ttu-id="2dd1b-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dd1b-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2dd1b-119">-EndpointName</span></span>
<span data-ttu-id="2dd1b-120">A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-120">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd1b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dd1b-121">-InputObject</span></span>
<span data-ttu-id="2dd1b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd1b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2dd1b-123">-NoWait</span></span>
<span data-ttu-id="2dd1b-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="2dd1b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2dd1b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dd1b-125">-PassThru</span></span>
<span data-ttu-id="2dd1b-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="2dd1b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2dd1b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd1b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2dd1b-128">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd1b-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2dd1b-129">-ResourceName</span></span>
<span data-ttu-id="2dd1b-130">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-130">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd1b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2dd1b-131">-SubscriptionId</span></span>
<span data-ttu-id="2dd1b-132">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-132">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd1b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dd1b-133">-Confirm</span></span>
<span data-ttu-id="2dd1b-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dd1b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd1b-135">-WhatIf</span></span>
<span data-ttu-id="2dd1b-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd1b-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dd1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd1b-138">CommonParameters</span></span>
<span data-ttu-id="2dd1b-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd1b-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dd1b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd1b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2dd1b-141">INPUTS</span></span>

### <span data-ttu-id="2dd1b-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="2dd1b-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="2dd1b-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2dd1b-143">OUTPUTS</span></span>

### <span data-ttu-id="2dd1b-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="2dd1b-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="2dd1b-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2dd1b-145">NOTES</span></span>

<span data-ttu-id="2dd1b-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2dd1b-146">ALIASES</span></span>

<span data-ttu-id="2dd1b-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2dd1b-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2dd1b-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2dd1b-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2dd1b-150">INPUTOBJECT: <IDigitalTwinsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2dd1b-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2dd1b-151">`[EndpointName <String>]`: A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="2dd1b-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="2dd1b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2dd1b-153">`[Location <String>]`: A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2dd1b-154">`[ResourceGroupName <String>]`: A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2dd1b-155">`[ResourceName <String>]`: A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2dd1b-156">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="2dd1b-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2dd1b-157">RELATED LINKS</span></span>

