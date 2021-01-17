---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467774"
---
# <span data-ttu-id="80ee4-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="80ee4-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="80ee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="80ee4-103">A DigitalTwinsInstances erőforrás lekérte.</span><span class="sxs-lookup"><span data-stu-id="80ee4-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="80ee4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80ee4-104">SYNTAX</span></span>

### <span data-ttu-id="80ee4-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80ee4-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="80ee4-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="80ee4-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="80ee4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80ee4-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="80ee4-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="80ee4-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="80ee4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80ee4-109">DESCRIPTION</span></span>
<span data-ttu-id="80ee4-110">A DigitalTwinsInstances erőforrás lekérte.</span><span class="sxs-lookup"><span data-stu-id="80ee4-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="80ee4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80ee4-111">EXAMPLES</span></span>

### <span data-ttu-id="80ee4-112">1. példa: Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80ee4-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="80ee4-113">Az összes DigitalTwinsInstance alapértelmezés szerint</span><span class="sxs-lookup"><span data-stu-id="80ee4-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="80ee4-114">2. példa: Get</span><span class="sxs-lookup"><span data-stu-id="80ee4-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="80ee4-115">A megadott AzDigitalTwinsInstance by ResourceName</span><span class="sxs-lookup"><span data-stu-id="80ee4-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="80ee4-116">3. példa: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80ee4-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="80ee4-117">A megadott AzDigitalTwinsInstance by Object</span><span class="sxs-lookup"><span data-stu-id="80ee4-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="80ee4-118">4. példa: Lista1</span><span class="sxs-lookup"><span data-stu-id="80ee4-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="80ee4-119">Az összes DigitalTwinsInstance by ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ee4-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="80ee4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80ee4-120">PARAMETERS</span></span>

### <span data-ttu-id="80ee4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ee4-121">-DefaultProfile</span></span>
<span data-ttu-id="80ee4-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80ee4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80ee4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80ee4-123">-InputObject</span></span>
<span data-ttu-id="80ee4-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="80ee4-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80ee4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ee4-125">-ResourceGroupName</span></span>
<span data-ttu-id="80ee4-126">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="80ee4-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="80ee4-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="80ee4-127">-ResourceName</span></span>
<span data-ttu-id="80ee4-128">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="80ee4-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="80ee4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80ee4-129">-SubscriptionId</span></span>
<span data-ttu-id="80ee4-130">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="80ee4-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="80ee4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ee4-131">CommonParameters</span></span>
<span data-ttu-id="80ee4-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80ee4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ee4-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80ee4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ee4-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80ee4-134">INPUTS</span></span>

### <span data-ttu-id="80ee4-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="80ee4-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="80ee4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80ee4-136">OUTPUTS</span></span>

### <span data-ttu-id="80ee4-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="80ee4-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="80ee4-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80ee4-138">NOTES</span></span>

<span data-ttu-id="80ee4-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="80ee4-139">ALIASES</span></span>

<span data-ttu-id="80ee4-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="80ee4-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80ee4-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="80ee4-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80ee4-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80ee4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80ee4-143">INPUTOBJECT: <IDigitalTwinsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="80ee4-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80ee4-144">`[EndpointName <String>]`: A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="80ee4-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="80ee4-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="80ee4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80ee4-146">`[Location <String>]`: A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="80ee4-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="80ee4-147">`[ResourceGroupName <String>]`: A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="80ee4-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="80ee4-148">`[ResourceName <String>]`: A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="80ee4-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="80ee4-149">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="80ee4-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="80ee4-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80ee4-150">RELATED LINKS</span></span>

