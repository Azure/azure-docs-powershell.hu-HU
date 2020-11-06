---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 3c77ca67999ffa9cecbe35de4d4533f5d163f17f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504235"
---
# <span data-ttu-id="b5d8b-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b5d8b-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="b5d8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d8b-103">Egy végpontot ad hozzá egy helyi forgalomirányítási profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5d8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5d8b-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5d8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="b5d8b-106">A **Add-AzureRmTrafficManagerEndpointConfig** parancsmag hozzáad egy végpontot egy helyi Azure Traffic Manager-profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="b5d8b-107">A New-AzureRmTrafficManagerProfile-vagy Get-AzureRmTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="b5d8b-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="b5d8b-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b5d8b-110">Ha végpontot szeretne létrehozni, és egyetlen műveletben szeretné végrehajtani a változást, használja az New-AzureRmTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="b5d8b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b5d8b-111">EXAMPLES</span></span>

### <span data-ttu-id="b5d8b-112">1. példa: végpont felvétele a profilba</span><span class="sxs-lookup"><span data-stu-id="b5d8b-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b5d8b-113">Az első parancs az Azure Traffic Manager-profilt a **Get-AzureRmTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="b5d8b-114">A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b5d8b-115">A második parancs hozzáadja a contoso nevű végpontot az $TrafficManagerProfile tárolt profiljához.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b5d8b-116">A parancs a végponthoz tartozó konfigurációs adatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="b5d8b-117">Ez a parancs csak a helyi objektumot módosítja.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-117">This command changes only the local object.</span></span>

<span data-ttu-id="b5d8b-118">A végleges parancs frissíti a forgalomirányítási profilt az Azure-ban az $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b5d8b-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5d8b-119">PARAMETERS</span></span>

### <span data-ttu-id="b5d8b-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="b5d8b-120">-CustomHeader</span></span>
<span data-ttu-id="b5d8b-121">Az egyéni élőfej neve és az érték párok listája a szonda-kérésekhez.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="b5d8b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d8b-122">-DefaultProfile</span></span>
<span data-ttu-id="b5d8b-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d8b-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="b5d8b-124">-EndpointLocation</span></span>
<span data-ttu-id="b5d8b-125">A teljesítmény-továbbítási módszerben használandó végpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="b5d8b-126">Ez a paraméter csak a ExternalEndpoints vagy a NestedEndpoints típusú végpontokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="b5d8b-127">Ezt a paramétert akkor kell megadnia, ha a teljesítményadatok-útválasztási módszert használja.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="b5d8b-128">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-128">Specify an Azure region name.</span></span>
<span data-ttu-id="b5d8b-129">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="b5d8b-129">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="b5d8b-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b5d8b-130">-EndpointName</span></span>
<span data-ttu-id="b5d8b-131">Annak a forgalomirányító-végpontnak a nevét adja meg, amelyre a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b5d8b-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="b5d8b-132">-EndpointStatus</span></span>
<span data-ttu-id="b5d8b-133">A végpont állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="b5d8b-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b5d8b-134">Valid values are:</span></span> 

- <span data-ttu-id="b5d8b-135">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="b5d8b-135">Enabled</span></span> 
- <span data-ttu-id="b5d8b-136">Tiltva</span><span class="sxs-lookup"><span data-stu-id="b5d8b-136">Disabled</span></span> 

<span data-ttu-id="b5d8b-137">Ha az állapot engedélyezve van, akkor a végpontok állapotát a program kikapcsolja, és a forgalom-útválasztási módszer tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="b5d8b-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="b5d8b-138">-GeoMapping</span></span>
<span data-ttu-id="b5d8b-139">A végponthoz rendelt régiók listája a földrajzi forgalom útválasztási módszerének használatakor.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="b5d8b-140">Kérjük, hogy az [elfogadott értékek teljes listáját](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)a Traffic Manager dokumentációjában találja.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="b5d8b-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="b5d8b-141">-MinChildEndpoints</span></span>
<span data-ttu-id="b5d8b-142">Azoknak a végpontoknak a minimális száma, amelyeknek elérhetőnek kell lenniük a gyermek profilban, hogy a beágyazott végpont a szülő profilban legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="b5d8b-143">Csak a "NestedEndpoints" típusú végpontra érvényes.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="b5d8b-144">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="b5d8b-144">-Priority</span></span>
<span data-ttu-id="b5d8b-145">Azt a prioritást adja meg, amelyet a forgalomirányítási rendel a végponthoz.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="b5d8b-146">Ez a paraméter csak akkor használatos, ha a forgalomirányítási profil a Priority Traffic-Routing metódussal van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="b5d8b-147">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="b5d8b-148">Az alacsonyabb értékek magasabb prioritást jelentenek.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="b5d8b-149">Ha prioritást ad meg, a profil minden végpontján meg kell adnia a prioritást, és nincs két végpont sem osztható meg ugyanazzal a prioritási értékkel.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="b5d8b-150">Ha nem adja meg a prioritásokat, a forgalomirányító a végpontokhoz rendeli az alapértelmezett prioritási értékeket a végpontokhoz (1) kezdve, abban a sorrendben, ahogyan a profil a végpontokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="b5d8b-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="b5d8b-151">-SubnetMapping</span></span>
<span data-ttu-id="b5d8b-152">Az e végponthoz hozzárendelt címtartomány vagy alhálózatok listája, ha a â € ̃Subnetâ €™ forgalmi útválasztási módszert használja.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-152">The list of address ranges or subnets mapped to this endpoint when using the â€˜Subnetâ€™ traffic routing method.</span></span>

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

### <span data-ttu-id="b5d8b-153">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="b5d8b-153">-Target</span></span>
<span data-ttu-id="b5d8b-154">A végpont teljesen minősített DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="b5d8b-155">A Traffic Manager ezt az értéket a DNS-válaszokban akkor jeleníti meg, amikor a forgalmat a végpontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="b5d8b-156">Ezt a paramétert csak a ExternalEndpoints végpont típusára adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="b5d8b-157">A többi végpont típusnál adja meg ehelyett a *TargetResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="b5d8b-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b5d8b-158">-TargetResourceId</span></span>
<span data-ttu-id="b5d8b-159">A cél erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="b5d8b-160">Ezt a paramétert csak a AzureEndpoints és a NestedEndpoints végpont típusához adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="b5d8b-161">A ExternalEndpoints végpont típusnál adja meg ehelyett a *cél* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="b5d8b-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5d8b-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="b5d8b-163">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b5d8b-164">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b5d8b-165">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-165">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b5d8b-166">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="b5d8b-166">-Type</span></span>
<span data-ttu-id="b5d8b-167">Azt adja meg, hogy a parancsmag milyen típusú végpontot ad az Azure Traffic Manager profiljához.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b5d8b-168">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b5d8b-168">Valid values are:</span></span> 

- <span data-ttu-id="b5d8b-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="b5d8b-169">AzureEndpoints</span></span>
- <span data-ttu-id="b5d8b-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="b5d8b-170">ExternalEndpoints</span></span>
- <span data-ttu-id="b5d8b-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="b5d8b-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="b5d8b-172">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="b5d8b-172">-Weight</span></span>
<span data-ttu-id="b5d8b-173">A forgalomirányító által a végponthoz hozzárendelt vastagságot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="b5d8b-174">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="b5d8b-175">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="b5d8b-175">The default value is one (1).</span></span>
<span data-ttu-id="b5d8b-176">Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja a súlyozott forgalom-útválasztási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="b5d8b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d8b-177">CommonParameters</span></span>
<span data-ttu-id="b5d8b-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5d8b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d8b-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d8b-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d8b-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5d8b-180">INPUTS</span></span>

### <span data-ttu-id="b5d8b-181">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5d8b-181">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b5d8b-182">Ez a parancsmag egy **TrafficManagerProfile** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-182">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="b5d8b-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5d8b-183">OUTPUTS</span></span>

### <span data-ttu-id="b5d8b-184">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5d8b-184">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b5d8b-185">Ez a parancsmag egy módosított **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="b5d8b-185">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="b5d8b-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5d8b-186">NOTES</span></span>

## <span data-ttu-id="b5d8b-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5d8b-187">RELATED LINKS</span></span>

[<span data-ttu-id="b5d8b-188">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5d8b-188">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b5d8b-189">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5d8b-189">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b5d8b-190">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b5d8b-190">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b5d8b-191">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5d8b-191">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

