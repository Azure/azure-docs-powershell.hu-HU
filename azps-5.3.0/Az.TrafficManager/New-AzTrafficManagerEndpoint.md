---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382912"
---
# <span data-ttu-id="c5f4a-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f4a-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="c5f4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f4a-103">Végpontot hoz létre a Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="c5f4a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5f4a-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5f4a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="c5f4a-106">A **New-AzTrafficManagerEndpoint** parancsmag létrehoz egy végpontot egy Azure Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="c5f4a-107">Ez a parancsmag minden új végpontot véglegesen a Traffic Manager szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="c5f4a-108">Ha több végpontot szeretne hozzáadni egy helyi Traffic Manager-profilobjektumhoz, és egyetlen művelettel szeretne módosításokat véglegesni, használja a Add-AzTrafficManagerEndpointConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="c5f4a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5f4a-109">EXAMPLES</span></span>

### <span data-ttu-id="c5f4a-110">1. példa: Külső végpont létrehozása profilhoz</span><span class="sxs-lookup"><span data-stu-id="c5f4a-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="c5f4a-111">Ez a parancs létrehoz egy contoso nevű külső végpontot a ContosoProfile nevű profilban az Erőforráscsoport11 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="c5f4a-112">2. példa: Azure-végpont létrehozása profilhoz</span><span class="sxs-lookup"><span data-stu-id="c5f4a-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="c5f4a-113">Ez a parancs létrehoz egy contoso nevű Azure-végpontot az Erőforráscsoport11 erőforráscsoport ContosoProfile nevű profiljában.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="c5f4a-114">Az Azure-végpont az Azure Web Appra mutat, amelynek Azure Resource Manager-azonosítóját a *TargetResourceId* URI elérési útja tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="c5f4a-115">A parancs nem adja meg az *EndpointLocation* paramétert, mert a Web App erőforrás megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="c5f4a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5f4a-116">PARAMETERS</span></span>

### <span data-ttu-id="c5f4a-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="c5f4a-117">-CustomHeader</span></span>
<span data-ttu-id="c5f4a-118">Egyéni fejlécnév és értékpárok listája a kérések igényléséhez.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-118">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f4a-119">-DefaultProfile</span></span>
<span data-ttu-id="c5f4a-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5f4a-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="c5f4a-121">-EndpointLocation</span></span>
<span data-ttu-id="c5f4a-122">Megadja a végpontnak a Performance traffic-routing metódusban használnia kell helyét.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="c5f4a-123">Ez a paraméter csak az ExternalEndpoints vagy NestedEndpoints típusú végpontokra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="c5f4a-124">Ezt a paramétert a Performance traffic-routing metódus használata esetén kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="c5f4a-125">Adjon meg egy Azure-régiónevet.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-125">Specify an Azure region name.</span></span>
<span data-ttu-id="c5f4a-126">Az Azure-régiók teljes listáját az Azure Régiók http://azure.microsoft.com/regions/ ( ( ) http://azure.microsoft.com/regions/) tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="c5f4a-127">-EndpointStatus</span></span>
<span data-ttu-id="c5f4a-128">A végpont állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="c5f4a-129">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="c5f4a-129">Valid values are:</span></span> 

- <span data-ttu-id="c5f4a-130">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="c5f4a-130">Enabled</span></span> 
- <span data-ttu-id="c5f4a-131">Letiltva</span><span class="sxs-lookup"><span data-stu-id="c5f4a-131">Disabled</span></span> 

<span data-ttu-id="c5f4a-132">Ha az állapot engedélyezve van, a végpont a végpont állapotát jelzi, és szerepel a forgalom útválasztási metódusában.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-133">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="c5f4a-133">-GeoMapping</span></span>
<span data-ttu-id="c5f4a-134">A végpontnak megfeleltetett régiók listája a "Földrajzi" forgalom útválasztási metódusának használata esetén.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="c5f4a-135">Az elfogadott értékek teljes listáját a Traffic Manager dokumentációjában találhatja meg.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-136">-MinDentEndpoints</span><span class="sxs-lookup"><span data-stu-id="c5f4a-136">-MinChildEndpoints</span></span>
<span data-ttu-id="c5f4a-137">Adjon meg egy Azure-régiónevet.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-137">Specify an Azure region name.</span></span>
<span data-ttu-id="c5f4a-138">Az Azure-régiók teljes listáját az Azure Régiók http://azure.microsoft.com/regions/ ( ( ) http://azure.microsoft.com/regions/) tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-139">-Name</span><span class="sxs-lookup"><span data-stu-id="c5f4a-139">-Name</span></span>
<span data-ttu-id="c5f4a-140">A parancsmag által létrehozott Traffic Manager-végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="c5f4a-141">-Priority</span></span>
<span data-ttu-id="c5f4a-142">Megadja a Traffic Manager által a végponthoz hozzárendelt prioritást.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="c5f4a-143">Ezt a paramétert csak akkor használja a rendszer, ha a Traffic Manager-profil a Prioritás forgalomirányítási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="c5f4a-144">Az érvényes értékek az 1 és 1000 között egész értékek.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="c5f4a-145">Az alacsonyabb értékek magasabb prioritást jelentenek.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="c5f4a-146">Prioritás megadása esetén a profil összes végpontja számára meg kell adnia a prioritást, és két végpont nem oszthatja meg ugyanazt a prioritásértéket.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="c5f4a-147">Ha nem ad meg prioritást, a Traffic Manager egy (1) értékkel kezdődően alapértelmezett prioritásértékeket rendel a végpontokhoz abban a sorrendben, amely a végpontokat felsorolja.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c5f4a-148">-ProfileName</span></span>
<span data-ttu-id="c5f4a-149">Megadja annak a Traffic Manager-profilnak a nevét, amelyhez a parancsmag hozzáad egy végpontot.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="c5f4a-150">Profil beszerzéséhez használja a New-AzTrafficManagerProfile vagy Get-AzTrafficManagerProfile parancsmagokat.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5f4a-151">-ResourceGroupName</span></span>
<span data-ttu-id="c5f4a-152">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c5f4a-153">Ez a parancsmag létrehoz egy Traffic Manager-végpontot a paraméter által megadott csoportban.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="c5f4a-154">-SubnetMapping</span></span>
<span data-ttu-id="c5f4a-155">A végpontnak megfeleltetett címtartományok vagy alhálózatok listája az "Alhálózati" adatforgalom-útválasztási módszer használata esetén.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-156">-Target</span><span class="sxs-lookup"><span data-stu-id="c5f4a-156">-Target</span></span>
<span data-ttu-id="c5f4a-157">A végpont teljes DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="c5f4a-158">A Traffic Manager ezt az értéket adja vissza a DNS-válaszokban, amikor a forgalmat erre a végpontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="c5f4a-159">Ezt a paramétert csak az ExternalEndpoints végponttípushoz adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="c5f4a-160">Más végponttípusok esetén adja meg a *TargetResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c5f4a-161">-TargetResourceId</span></span>
<span data-ttu-id="c5f4a-162">A cél erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="c5f4a-163">Ezt a paramétert csak az AzureEndpoints és NestedEndpoints végponttípusainál adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="c5f4a-164">Az ExternalEndpoints végponttípusnál adja meg a *Cél paramétert.*</span><span class="sxs-lookup"><span data-stu-id="c5f4a-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-165">-Type</span><span class="sxs-lookup"><span data-stu-id="c5f4a-165">-Type</span></span>
<span data-ttu-id="c5f4a-166">Megadja, hogy a parancsmag milyen típusú végpontot ad hozzá a Traffic Manager-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="c5f4a-167">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="c5f4a-167">Valid values are:</span></span> 

- <span data-ttu-id="c5f4a-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="c5f4a-168">AzureEndpoints</span></span>
- <span data-ttu-id="c5f4a-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="c5f4a-169">ExternalEndpoints</span></span>
- <span data-ttu-id="c5f4a-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="c5f4a-170">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-171">-Weight</span><span class="sxs-lookup"><span data-stu-id="c5f4a-171">-Weight</span></span>
<span data-ttu-id="c5f4a-172">A Traffic Manager által a végponthoz hozzárendelt súly megadása.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="c5f4a-173">Az érvényes értékek az 1 és 1000 között egész értékek.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="c5f4a-174">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="c5f4a-174">The default value is one (1).</span></span>
<span data-ttu-id="c5f4a-175">Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja súlyozott forgalom-útválasztási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f4a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f4a-176">CommonParameters</span></span>
<span data-ttu-id="c5f4a-177">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f4a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f4a-178">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5f4a-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f4a-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5f4a-179">INPUTS</span></span>

### <span data-ttu-id="c5f4a-180">Nincs</span><span class="sxs-lookup"><span data-stu-id="c5f4a-180">None</span></span>

## <span data-ttu-id="c5f4a-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5f4a-181">OUTPUTS</span></span>

### <span data-ttu-id="c5f4a-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f4a-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c5f4a-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5f4a-183">NOTES</span></span>

## <span data-ttu-id="c5f4a-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5f4a-184">RELATED LINKS</span></span>

[<span data-ttu-id="c5f4a-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f4a-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c5f4a-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f4a-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c5f4a-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f4a-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c5f4a-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5f4a-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5f4a-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5f4a-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5f4a-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f4a-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c5f4a-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5f4a-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


