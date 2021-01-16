---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347045"
---
# <span data-ttu-id="ba7be-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="ba7be-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="ba7be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba7be-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7be-103">A DigitalTwinsInstances végpont lekérte.</span><span class="sxs-lookup"><span data-stu-id="ba7be-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="ba7be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba7be-104">SYNTAX</span></span>

### <span data-ttu-id="ba7be-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba7be-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba7be-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="ba7be-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba7be-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba7be-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba7be-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba7be-108">DESCRIPTION</span></span>
<span data-ttu-id="ba7be-109">A DigitalTwinsInstances végpont lekérte.</span><span class="sxs-lookup"><span data-stu-id="ba7be-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="ba7be-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba7be-110">EXAMPLES</span></span>

### <span data-ttu-id="ba7be-111">1. példa: List AzDigitalTwinsEndpoint in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ba7be-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="ba7be-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7be-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="ba7be-113">2. példa: AzDigitalTwinsEndpoint – EndpointName</span><span class="sxs-lookup"><span data-stu-id="ba7be-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="ba7be-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ba7be-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="ba7be-115">3. példa: AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Objektum</span><span class="sxs-lookup"><span data-stu-id="ba7be-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="ba7be-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span><span class="sxs-lookup"><span data-stu-id="ba7be-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="ba7be-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba7be-117">PARAMETERS</span></span>

### <span data-ttu-id="ba7be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7be-118">-DefaultProfile</span></span>
<span data-ttu-id="ba7be-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba7be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba7be-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ba7be-120">-EndpointName</span></span>
<span data-ttu-id="ba7be-121">A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7be-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="ba7be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba7be-122">-InputObject</span></span>
<span data-ttu-id="ba7be-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ba7be-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba7be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7be-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba7be-125">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba7be-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ba7be-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ba7be-126">-ResourceName</span></span>
<span data-ttu-id="ba7be-127">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="ba7be-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ba7be-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba7be-128">-SubscriptionId</span></span>
<span data-ttu-id="ba7be-129">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ba7be-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="ba7be-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7be-130">CommonParameters</span></span>
<span data-ttu-id="ba7be-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba7be-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7be-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba7be-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7be-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba7be-133">INPUTS</span></span>

### <span data-ttu-id="ba7be-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="ba7be-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="ba7be-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba7be-135">OUTPUTS</span></span>

### <span data-ttu-id="ba7be-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="ba7be-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="ba7be-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba7be-137">NOTES</span></span>

<span data-ttu-id="ba7be-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ba7be-138">ALIASES</span></span>

<span data-ttu-id="ba7be-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ba7be-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba7be-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ba7be-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba7be-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba7be-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba7be-142">INPUTOBJECT: <IDigitalTwinsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ba7be-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba7be-143">`[EndpointName <String>]`: A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7be-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="ba7be-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ba7be-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba7be-145">`[Location <String>]`: A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="ba7be-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ba7be-146">`[ResourceGroupName <String>]`: A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba7be-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ba7be-147">`[ResourceName <String>]`: A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="ba7be-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ba7be-148">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ba7be-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="ba7be-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba7be-149">RELATED LINKS</span></span>

