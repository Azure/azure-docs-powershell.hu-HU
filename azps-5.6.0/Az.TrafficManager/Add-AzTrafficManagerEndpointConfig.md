---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 79e3547a8065b20b693b05b7fe4582bbd775abdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936522"
---
# <span data-ttu-id="f2299-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f2299-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="f2299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2299-102">SYNOPSIS</span></span>
<span data-ttu-id="f2299-103">Hozzáad egy végpontot egy helyi Traffic Manager-profilobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f2299-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="f2299-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2299-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2299-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2299-105">DESCRIPTION</span></span>
<span data-ttu-id="f2299-106">Az **Add-AzTrafficManagerEndpointConfig parancsmag** hozzáad egy végpontot egy helyi Azure Traffic Manager-profilobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f2299-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f2299-107">A profilt a New-AzTrafficManagerProfile vagy Get-AzTrafficManagerProfile használhatja.</span><span class="sxs-lookup"><span data-stu-id="f2299-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f2299-108">Ez a parancsmag a helyi profilobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="f2299-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f2299-109">A Forgalomkezelőben a módosításokat a Set-AzTrafficManagerProfile el.</span><span class="sxs-lookup"><span data-stu-id="f2299-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f2299-110">Végpont létrehozásához és a módosítás egyetlen művelettel való véglegesítéshez használja a New-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f2299-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="f2299-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2299-111">EXAMPLES</span></span>

### <span data-ttu-id="f2299-112">1. példa: Végpont hozzáadása profilhoz</span><span class="sxs-lookup"><span data-stu-id="f2299-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f2299-113">Az első parancs a **Get-AzTrafficManagerProfile** parancsmag használatával kap egy Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="f2299-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f2299-114">A parancs a helyi profilt a $TrafficManagerProfile tárolja.</span><span class="sxs-lookup"><span data-stu-id="f2299-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f2299-115">A második parancs hozzáadja a contoso nevű végpontot a $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f2299-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f2299-116">A parancs a végpont konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f2299-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="f2299-117">Ez a parancs csak a helyi objektumot módosítja.</span><span class="sxs-lookup"><span data-stu-id="f2299-117">This command changes only the local object.</span></span>

<span data-ttu-id="f2299-118">Az utolsó parancs frissíti a Traffic Manager-profilt az Azure-ban úgy, hogy megfeleljen a helyi $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f2299-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f2299-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2299-119">PARAMETERS</span></span>

### <span data-ttu-id="f2299-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="f2299-120">-CustomHeader</span></span>
<span data-ttu-id="f2299-121">Egyéni fejlécnév és értékpárok listája a kérések igényléséhez.</span><span class="sxs-lookup"><span data-stu-id="f2299-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="f2299-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2299-122">-DefaultProfile</span></span>
<span data-ttu-id="f2299-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2299-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2299-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="f2299-124">-EndpointLocation</span></span>
<span data-ttu-id="f2299-125">Megadja a végpontnak a Performance traffic-routing metódusban használnia kell helyét.</span><span class="sxs-lookup"><span data-stu-id="f2299-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="f2299-126">Ez a paraméter csak az ExternalEndpoints vagy NestedEndpoints típusú végpontokra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="f2299-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="f2299-127">Ezt a paramétert a Performance traffic-routing metódus használata esetén kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="f2299-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="f2299-128">Adjon meg egy Azure-régiónevet.</span><span class="sxs-lookup"><span data-stu-id="f2299-128">Specify an Azure region name.</span></span>
<span data-ttu-id="f2299-129">Az Azure-régiók teljes listáját az Azure Régiók http://azure.microsoft.com/regions/ ( ( ) http://azure.microsoft.com/regions/) tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f2299-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="f2299-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f2299-130">-EndpointName</span></span>
<span data-ttu-id="f2299-131">Megadja annak a Traffic Manager-végpontnak a nevét, amelybe ez a parancsmag hozzáadja.</span><span class="sxs-lookup"><span data-stu-id="f2299-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f2299-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="f2299-132">-EndpointStatus</span></span>
<span data-ttu-id="f2299-133">A végpont állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f2299-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="f2299-134">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="f2299-134">Valid values are:</span></span> 

- <span data-ttu-id="f2299-135">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="f2299-135">Enabled</span></span> 
- <span data-ttu-id="f2299-136">Letiltva</span><span class="sxs-lookup"><span data-stu-id="f2299-136">Disabled</span></span> 

<span data-ttu-id="f2299-137">Ha az állapot engedélyezve van, a végpont a végpont állapotát jelzi, és szerepel a forgalom-útválasztási metódusban.</span><span class="sxs-lookup"><span data-stu-id="f2299-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="f2299-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="f2299-138">-GeoMapping</span></span>
<span data-ttu-id="f2299-139">Az ehhez a végponthoz csatlakoztatott régiók listája a "Földrajzi" forgalom útválasztási metódusának használata esetén.</span><span class="sxs-lookup"><span data-stu-id="f2299-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="f2299-140">Az elfogadott értékek teljes listáját a Traffic Manager [dokumentációjában találhatja meg.](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions)</span><span class="sxs-lookup"><span data-stu-id="f2299-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="f2299-141">-MinDentEndpoints</span><span class="sxs-lookup"><span data-stu-id="f2299-141">-MinChildEndpoints</span></span>
<span data-ttu-id="f2299-142">Azon végpontok minimális száma, amelyeknek elérhetőnek kell lennie a gyermekprofilban ahhoz, hogy a szülőprofil beágyazott végpontja elérhetőnek számítson.</span><span class="sxs-lookup"><span data-stu-id="f2299-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="f2299-143">Csak a "NestedEndpoints" típusú végpontokra alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="f2299-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="f2299-144">-Priority</span><span class="sxs-lookup"><span data-stu-id="f2299-144">-Priority</span></span>
<span data-ttu-id="f2299-145">Megadja a Traffic Manager által a végponthoz hozzárendelt prioritást.</span><span class="sxs-lookup"><span data-stu-id="f2299-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="f2299-146">Ezt a paramétert csak akkor használja a rendszer, ha a Traffic Manager-profil a Prioritás forgalomirányítási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="f2299-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="f2299-147">Az érvényes értékek az 1 és 1000 között egész értékek.</span><span class="sxs-lookup"><span data-stu-id="f2299-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="f2299-148">Az alacsonyabb értékek magasabb prioritást jelentenek.</span><span class="sxs-lookup"><span data-stu-id="f2299-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="f2299-149">Prioritás megadása esetén a profil összes végpontja számára meg kell adnia a prioritást, és két végpont nem oszthatja meg ugyanazt a prioritásértéket.</span><span class="sxs-lookup"><span data-stu-id="f2299-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="f2299-150">Ha nem ad meg prioritást, a Traffic Manager egy (1) értékkel kezdődően alapértelmezett prioritásértékeket rendel a végpontokhoz abban a sorrendben, amely a végpontokat felsorolja.</span><span class="sxs-lookup"><span data-stu-id="f2299-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="f2299-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="f2299-151">-SubnetMapping</span></span>
<span data-ttu-id="f2299-152">A végpontnak megfeleltetett címtartományok vagy alhálózatok listája az alhálózati forgalom útválasztási metódusának használata esetén.</span><span class="sxs-lookup"><span data-stu-id="f2299-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="f2299-153">-Target</span><span class="sxs-lookup"><span data-stu-id="f2299-153">-Target</span></span>
<span data-ttu-id="f2299-154">A végpont teljes DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2299-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="f2299-155">A Traffic Manager ezt az értéket adja vissza a DNS-válaszokban, amikor a forgalmat erre a végpontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="f2299-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="f2299-156">Ezt a paramétert csak az ExternalEndpoints végponttípushoz adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2299-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="f2299-157">Más végponttípusok esetén adja meg a *TargetResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="f2299-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="f2299-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f2299-158">-TargetResourceId</span></span>
<span data-ttu-id="f2299-159">A cél erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2299-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="f2299-160">Ezt a paramétert csak az AzureEndpoints és NestedEndpoints végponttípusainál adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2299-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="f2299-161">Az ExternalEndpoints végponttípusnál adja meg a *Cél paramétert.*</span><span class="sxs-lookup"><span data-stu-id="f2299-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="f2299-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2299-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="f2299-163">Helyi **TrafficManagerProfile objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="f2299-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f2299-164">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="f2299-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f2299-165">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f2299-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2299-166">-Type</span><span class="sxs-lookup"><span data-stu-id="f2299-166">-Type</span></span>
<span data-ttu-id="f2299-167">Megadja, hogy a parancsmag milyen típusú végpontot ad hozzá az Azure Traffic Manager-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="f2299-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f2299-168">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="f2299-168">Valid values are:</span></span> 

- <span data-ttu-id="f2299-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="f2299-169">AzureEndpoints</span></span>
- <span data-ttu-id="f2299-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="f2299-170">ExternalEndpoints</span></span>
- <span data-ttu-id="f2299-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="f2299-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="f2299-172">-Weight</span><span class="sxs-lookup"><span data-stu-id="f2299-172">-Weight</span></span>
<span data-ttu-id="f2299-173">A Traffic Manager által a végponthoz hozzárendelt súly megadása.</span><span class="sxs-lookup"><span data-stu-id="f2299-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="f2299-174">Az érvényes értékek az 1 és 1000 között egész értékek.</span><span class="sxs-lookup"><span data-stu-id="f2299-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="f2299-175">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="f2299-175">The default value is one (1).</span></span>
<span data-ttu-id="f2299-176">Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja súlyozott forgalom-útválasztási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="f2299-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="f2299-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2299-177">CommonParameters</span></span>
<span data-ttu-id="f2299-178">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2299-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2299-179">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2299-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2299-180">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2299-180">INPUTS</span></span>

### <span data-ttu-id="f2299-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2299-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f2299-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2299-182">OUTPUTS</span></span>

### <span data-ttu-id="f2299-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2299-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f2299-184">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2299-184">NOTES</span></span>

## <span data-ttu-id="f2299-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2299-185">RELATED LINKS</span></span>

[<span data-ttu-id="f2299-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2299-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f2299-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2299-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="f2299-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f2299-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f2299-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2299-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


