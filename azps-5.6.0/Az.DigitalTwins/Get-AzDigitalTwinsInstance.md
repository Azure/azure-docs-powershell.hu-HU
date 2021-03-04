---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 38f9aef513e13b2676569d434977752f3d193062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935162"
---
# <span data-ttu-id="aee43-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="aee43-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="aee43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aee43-102">SYNOPSIS</span></span>
<span data-ttu-id="aee43-103">DigitalTwinsInstances erőforrás lekérte.</span><span class="sxs-lookup"><span data-stu-id="aee43-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="aee43-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aee43-104">SYNTAX</span></span>

### <span data-ttu-id="aee43-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aee43-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aee43-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="aee43-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aee43-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aee43-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="aee43-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="aee43-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="aee43-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aee43-109">DESCRIPTION</span></span>
<span data-ttu-id="aee43-110">DigitalTwinsInstances erőforrás lekérte.</span><span class="sxs-lookup"><span data-stu-id="aee43-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="aee43-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aee43-111">EXAMPLES</span></span>

### <span data-ttu-id="aee43-112">1. példa: Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aee43-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="aee43-113">Az összes DigitalTwinsInstance alapértelmezés szerint</span><span class="sxs-lookup"><span data-stu-id="aee43-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="aee43-114">2. példa: Get</span><span class="sxs-lookup"><span data-stu-id="aee43-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="aee43-115">A megadott AzDigitalTwinsInstance by ResourceName</span><span class="sxs-lookup"><span data-stu-id="aee43-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="aee43-116">3. példa: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aee43-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="aee43-117">A megadott AzDigitalTwinsInstance by Object</span><span class="sxs-lookup"><span data-stu-id="aee43-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="aee43-118">4. példa: Lista1</span><span class="sxs-lookup"><span data-stu-id="aee43-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="aee43-119">Az összes DigitalTwinsInstance by ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aee43-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="aee43-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aee43-120">PARAMETERS</span></span>

### <span data-ttu-id="aee43-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee43-121">-DefaultProfile</span></span>
<span data-ttu-id="aee43-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aee43-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aee43-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aee43-123">-InputObject</span></span>
<span data-ttu-id="aee43-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="aee43-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aee43-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aee43-125">-ResourceGroupName</span></span>
<span data-ttu-id="aee43-126">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aee43-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee43-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aee43-127">-ResourceName</span></span>
<span data-ttu-id="aee43-128">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="aee43-128">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee43-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aee43-129">-SubscriptionId</span></span>
<span data-ttu-id="aee43-130">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aee43-130">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee43-131">CommonParameters</span></span>
<span data-ttu-id="aee43-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aee43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee43-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aee43-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee43-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aee43-134">INPUTS</span></span>

### <span data-ttu-id="aee43-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="aee43-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="aee43-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aee43-136">OUTPUTS</span></span>

### <span data-ttu-id="aee43-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="aee43-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="aee43-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aee43-138">NOTES</span></span>

<span data-ttu-id="aee43-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aee43-139">ALIASES</span></span>

<span data-ttu-id="aee43-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="aee43-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aee43-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="aee43-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aee43-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aee43-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aee43-143">INPUTOBJECT: <IDigitalTwinsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="aee43-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aee43-144">`[EndpointName <String>]`: A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="aee43-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="aee43-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="aee43-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aee43-146">`[Location <String>]`: A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="aee43-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="aee43-147">`[ResourceGroupName <String>]`: A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aee43-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="aee43-148">`[ResourceName <String>]`: A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="aee43-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="aee43-149">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aee43-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="aee43-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aee43-150">RELATED LINKS</span></span>

