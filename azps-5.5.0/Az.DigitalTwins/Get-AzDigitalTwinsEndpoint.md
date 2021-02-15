---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155746"
---
# <span data-ttu-id="7bdb7-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bdb7-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="7bdb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bdb7-102">SYNOPSIS</span></span>
<span data-ttu-id="7bdb7-103">DigitalTwinsInstances Végpont lekérte.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="7bdb7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7bdb7-104">SYNTAX</span></span>

### <span data-ttu-id="7bdb7-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7bdb7-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7bdb7-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="7bdb7-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7bdb7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7bdb7-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7bdb7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7bdb7-108">DESCRIPTION</span></span>
<span data-ttu-id="7bdb7-109">A DigitalTwinsInstances végpont lekérte.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="7bdb7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7bdb7-110">EXAMPLES</span></span>

### <span data-ttu-id="7bdb7-111">1. példa: List AzDigitalTwinsEndpoint in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7bdb7-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="7bdb7-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bdb7-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="7bdb7-113">2. példa: AzDigitalTwinsEndpoint – EndpointName</span><span class="sxs-lookup"><span data-stu-id="7bdb7-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="7bdb7-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7bdb7-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="7bdb7-115">3. példa: AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Objektum</span><span class="sxs-lookup"><span data-stu-id="7bdb7-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="7bdb7-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span><span class="sxs-lookup"><span data-stu-id="7bdb7-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="7bdb7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bdb7-117">PARAMETERS</span></span>

### <span data-ttu-id="7bdb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bdb7-118">-DefaultProfile</span></span>
<span data-ttu-id="7bdb7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bdb7-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7bdb7-120">-EndpointName</span></span>
<span data-ttu-id="7bdb7-121">A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="7bdb7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bdb7-122">-InputObject</span></span>
<span data-ttu-id="7bdb7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7bdb7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bdb7-124">-ResourceGroupName</span></span>
<span data-ttu-id="7bdb7-125">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb7-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7bdb7-126">-ResourceName</span></span>
<span data-ttu-id="7bdb7-127">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bdb7-128">-SubscriptionId</span></span>
<span data-ttu-id="7bdb7-129">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-129">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bdb7-130">CommonParameters</span></span>
<span data-ttu-id="7bdb7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bdb7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bdb7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bdb7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bdb7-133">INPUTS</span></span>

### <span data-ttu-id="7bdb7-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7bdb7-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="7bdb7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bdb7-135">OUTPUTS</span></span>

### <span data-ttu-id="7bdb7-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="7bdb7-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="7bdb7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7bdb7-137">NOTES</span></span>

<span data-ttu-id="7bdb7-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7bdb7-138">ALIASES</span></span>

<span data-ttu-id="7bdb7-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7bdb7-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7bdb7-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7bdb7-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7bdb7-142">INPUTOBJECT: <IDigitalTwinsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7bdb7-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7bdb7-143">`[EndpointName <String>]`: A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="7bdb7-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7bdb7-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7bdb7-145">`[Location <String>]`: A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7bdb7-146">`[ResourceGroupName <String>]`: A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7bdb7-147">`[ResourceName <String>]`: A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7bdb7-148">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7bdb7-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="7bdb7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bdb7-149">RELATED LINKS</span></span>

