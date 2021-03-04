---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: ff83b10755789f807e1ec28b1f247c9ebee1da18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935114"
---
# <span data-ttu-id="5e371-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="5e371-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="5e371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e371-102">SYNOPSIS</span></span>
<span data-ttu-id="5e371-103">DigitalTwinsInstance törlése</span><span class="sxs-lookup"><span data-stu-id="5e371-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="5e371-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e371-104">SYNTAX</span></span>

### <span data-ttu-id="5e371-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e371-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e371-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e371-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e371-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e371-107">DESCRIPTION</span></span>
<span data-ttu-id="5e371-108">DigitalTwinsInstance törlése</span><span class="sxs-lookup"><span data-stu-id="5e371-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="5e371-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e371-109">EXAMPLES</span></span>

### <span data-ttu-id="5e371-110">1. példa: AzDigitalTwinsInstance eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="5e371-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="5e371-111">Ez a parancs eltávolítja az AzDigitalTwinsInstance név szerint</span><span class="sxs-lookup"><span data-stu-id="5e371-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="5e371-112">2. példa: AzDigitalTwinsInstance by InputObject eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5e371-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="5e371-113">Ez a parancs eltávolítja az AzDigitalTwinsInstance név szerint</span><span class="sxs-lookup"><span data-stu-id="5e371-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="5e371-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e371-114">PARAMETERS</span></span>

### <span data-ttu-id="5e371-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e371-115">-AsJob</span></span>
<span data-ttu-id="5e371-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="5e371-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5e371-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e371-117">-DefaultProfile</span></span>
<span data-ttu-id="5e371-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e371-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e371-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e371-119">-InputObject</span></span>
<span data-ttu-id="5e371-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5e371-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e371-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5e371-121">-NoWait</span></span>
<span data-ttu-id="5e371-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="5e371-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e371-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e371-123">-PassThru</span></span>
<span data-ttu-id="5e371-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="5e371-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e371-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e371-125">-ResourceGroupName</span></span>
<span data-ttu-id="5e371-126">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5e371-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5e371-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5e371-127">-ResourceName</span></span>
<span data-ttu-id="5e371-128">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="5e371-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5e371-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e371-129">-SubscriptionId</span></span>
<span data-ttu-id="5e371-130">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5e371-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="5e371-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e371-131">-Confirm</span></span>
<span data-ttu-id="5e371-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5e371-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e371-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e371-133">-WhatIf</span></span>
<span data-ttu-id="5e371-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5e371-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e371-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e371-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e371-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e371-136">CommonParameters</span></span>
<span data-ttu-id="5e371-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e371-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e371-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e371-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e371-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e371-139">INPUTS</span></span>

### <span data-ttu-id="5e371-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="5e371-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="5e371-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e371-141">OUTPUTS</span></span>

### <span data-ttu-id="5e371-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="5e371-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="5e371-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e371-143">NOTES</span></span>

<span data-ttu-id="5e371-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5e371-144">ALIASES</span></span>

<span data-ttu-id="5e371-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5e371-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e371-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5e371-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e371-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e371-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e371-148">INPUTOBJECT: <IDigitalTwinsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5e371-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e371-149">`[EndpointName <String>]`: A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5e371-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="5e371-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5e371-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e371-151">`[Location <String>]`: A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="5e371-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5e371-152">`[ResourceGroupName <String>]`: A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5e371-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5e371-153">`[ResourceName <String>]`: A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="5e371-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5e371-154">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5e371-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="5e371-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e371-155">RELATED LINKS</span></span>

