---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012603"
---
# <span data-ttu-id="a3d7e-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d7e-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="a3d7e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d7e-103">A forgalomirányító-profilban hoz létre végpontot.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="a3d7e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3d7e-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3d7e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="a3d7e-106">A **New-AzTrafficManagerEndpoint** parancsmag létrehoz egy végpontot az Azure Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="a3d7e-107">Ez a parancsmag minden új végpontot véglegesít a forgalomirányítási szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="a3d7e-108">Ha több végpontot szeretne felvenni egy helyi forgalomirányítási profil objektumba, és egyetlen műveletben szeretne módosításokat végrehajtani, használja az Add-AzTrafficManagerEndpointConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="a3d7e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a3d7e-109">EXAMPLES</span></span>

### <span data-ttu-id="a3d7e-110">Példa 1: külső végpont létrehozása profilhoz</span><span class="sxs-lookup"><span data-stu-id="a3d7e-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="a3d7e-111">Ez a parancs létrehoz egy contoso nevű külső végpontot a ResourceGroup11 nevű erőforráscsoport ContosoProfile nevű profiljában.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="a3d7e-112">2. példa: Azure-végpont létrehozása profilhoz</span><span class="sxs-lookup"><span data-stu-id="a3d7e-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="a3d7e-113">A parancs létrehoz egy contoso nevű Azure-végpontot az erőforráscsoport ResourceGroup11 nevű ContosoProfile-profilban.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="a3d7e-114">Az Azure-végpont arra az Azure Web App-pontra mutat, amelynek az Azure Resource Manager AZONOSÍTÓját az *TARGETRESOURCEID* URI elérési útja adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="a3d7e-115">A parancs nem adja meg a *EndpointLocation* paramétert, mert a Web App-erőforrás megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="a3d7e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3d7e-116">PARAMETERS</span></span>

### <span data-ttu-id="a3d7e-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="a3d7e-117">-CustomHeader</span></span>
<span data-ttu-id="a3d7e-118">Az egyéni élőfej neve és az érték párok listája a szonda-kérésekhez.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="a3d7e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d7e-119">-DefaultProfile</span></span>
<span data-ttu-id="a3d7e-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3d7e-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="a3d7e-121">-EndpointLocation</span></span>
<span data-ttu-id="a3d7e-122">A teljesítmény-továbbítási módszerben használandó végpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="a3d7e-123">Ez a paraméter csak a ExternalEndpoints vagy a NestedEndpoints típusú végpontokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="a3d7e-124">Ezt a paramétert akkor kell megadnia, ha a teljesítményadatok-útválasztási módszert használja.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="a3d7e-125">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-125">Specify an Azure region name.</span></span>
<span data-ttu-id="a3d7e-126">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="a3d7e-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="a3d7e-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="a3d7e-127">-EndpointStatus</span></span>
<span data-ttu-id="a3d7e-128">A végpont állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="a3d7e-129">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="a3d7e-129">Valid values are:</span></span> 

- <span data-ttu-id="a3d7e-130">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="a3d7e-130">Enabled</span></span> 
- <span data-ttu-id="a3d7e-131">Tiltva</span><span class="sxs-lookup"><span data-stu-id="a3d7e-131">Disabled</span></span> 

<span data-ttu-id="a3d7e-132">Ha az állapot engedélyezve van, akkor a végpontok állapotát a program kikapcsolja, és a forgalom-útválasztási módszer tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="a3d7e-133">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="a3d7e-133">-GeoMapping</span></span>
<span data-ttu-id="a3d7e-134">A végponthoz rendelt régiók listája a földrajzi forgalom útválasztási módszerének használatakor.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="a3d7e-135">Kérjük, hogy az elfogadott értékek teljes listáját a Traffic Manager dokumentációjában találja.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="a3d7e-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="a3d7e-136">-MinChildEndpoints</span></span>
<span data-ttu-id="a3d7e-137">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-137">Specify an Azure region name.</span></span>
<span data-ttu-id="a3d7e-138">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="a3d7e-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="a3d7e-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3d7e-139">-Name</span></span>
<span data-ttu-id="a3d7e-140">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a3d7e-141">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="a3d7e-141">-Priority</span></span>
<span data-ttu-id="a3d7e-142">Azt a prioritást adja meg, amelyet a forgalomirányítási rendel a végponthoz.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="a3d7e-143">Ez a paraméter csak akkor használatos, ha a forgalomirányítási profil a Priority Traffic-Routing metódussal van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="a3d7e-144">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="a3d7e-145">Az alacsonyabb értékek magasabb prioritást jelentenek.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="a3d7e-146">Ha prioritást ad meg, a profil minden végpontján meg kell adnia a prioritást, és nincs két végpont sem osztható meg ugyanazzal a prioritási értékkel.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="a3d7e-147">Ha nem adja meg a prioritásokat, a forgalomirányító a végpontokhoz rendeli az alapértelmezett prioritási értékeket a végpontokhoz (1) kezdve, abban a sorrendben, ahogyan a profil a végpontokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="a3d7e-148">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="a3d7e-148">-ProfileName</span></span>
<span data-ttu-id="a3d7e-149">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag hozzáadja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="a3d7e-150">Ha profilt szeretne beolvasni, használja az New-AzTrafficManagerProfile vagy Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="a3d7e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d7e-151">-ResourceGroupName</span></span>
<span data-ttu-id="a3d7e-152">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a3d7e-153">Ez a parancsmag egy forgalomirányítási végpontot hoz létre abban a csoportban, amelyben ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3d7e-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="a3d7e-154">-SubnetMapping</span></span>
<span data-ttu-id="a3d7e-155">Az adott végponthoz hozzárendelt címtartomány vagy alhálózatok listája, amikor az "alhálózat" forgalmi útválasztási módszert használja.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="a3d7e-156">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="a3d7e-156">-Target</span></span>
<span data-ttu-id="a3d7e-157">A végpont teljesen minősített DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="a3d7e-158">A Traffic Manager ezt az értéket a DNS-válaszokban akkor jeleníti meg, amikor a forgalmat a végpontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="a3d7e-159">Ezt a paramétert csak a ExternalEndpoints végpont típusára adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="a3d7e-160">A többi végpont típusnál adja meg ehelyett a *TargetResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="a3d7e-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a3d7e-161">-TargetResourceId</span></span>
<span data-ttu-id="a3d7e-162">A cél erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="a3d7e-163">Ezt a paramétert csak a AzureEndpoints és a NestedEndpoints végpont típusához adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="a3d7e-164">A ExternalEndpoints végpont típusnál adja meg ehelyett a *cél* paramétert.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="a3d7e-165">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="a3d7e-165">-Type</span></span>
<span data-ttu-id="a3d7e-166">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="a3d7e-167">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="a3d7e-167">Valid values are:</span></span> 

- <span data-ttu-id="a3d7e-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="a3d7e-168">AzureEndpoints</span></span>
- <span data-ttu-id="a3d7e-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="a3d7e-169">ExternalEndpoints</span></span>
- <span data-ttu-id="a3d7e-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="a3d7e-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="a3d7e-171">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="a3d7e-171">-Weight</span></span>
<span data-ttu-id="a3d7e-172">A forgalomirányító által a végponthoz hozzárendelt vastagságot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="a3d7e-173">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="a3d7e-174">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="a3d7e-174">The default value is one (1).</span></span>
<span data-ttu-id="a3d7e-175">Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja a súlyozott forgalom-útválasztási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="a3d7e-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="a3d7e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d7e-176">CommonParameters</span></span>
<span data-ttu-id="a3d7e-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3d7e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d7e-178">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3d7e-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d7e-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3d7e-179">INPUTS</span></span>

### <span data-ttu-id="a3d7e-180">Nincs</span><span class="sxs-lookup"><span data-stu-id="a3d7e-180">None</span></span>

## <span data-ttu-id="a3d7e-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3d7e-181">OUTPUTS</span></span>

### <span data-ttu-id="a3d7e-182">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d7e-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a3d7e-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3d7e-183">NOTES</span></span>

## <span data-ttu-id="a3d7e-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3d7e-184">RELATED LINKS</span></span>

[<span data-ttu-id="a3d7e-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d7e-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a3d7e-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d7e-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a3d7e-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d7e-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a3d7e-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3d7e-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="a3d7e-189">Új – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3d7e-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="a3d7e-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d7e-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a3d7e-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3d7e-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


