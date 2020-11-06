---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: e9e6817d9a290acf1e91067edfd90cdf8081f1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500351"
---
# <span data-ttu-id="7883e-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="7883e-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="7883e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7883e-102">SYNOPSIS</span></span>
<span data-ttu-id="7883e-103">Egy végpontot ad hozzá egy helyi forgalomirányítási profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="7883e-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7883e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7883e-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7883e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7883e-105">DESCRIPTION</span></span>
<span data-ttu-id="7883e-106">A **Add-AzureRmTrafficManagerEndpointConfig** parancsmag hozzáad egy végpontot egy helyi Azure Traffic Manager-profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="7883e-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="7883e-107">A New-AzureRmTrafficManagerProfile-vagy Get-AzureRmTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="7883e-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="7883e-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="7883e-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="7883e-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="7883e-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="7883e-110">Ha végpontot szeretne létrehozni, és egyetlen műveletben szeretné végrehajtani a változást, használja az New-AzureRmTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7883e-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="7883e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7883e-111">EXAMPLES</span></span>

### <span data-ttu-id="7883e-112">1. példa: végpont felvétele a profilba</span><span class="sxs-lookup"><span data-stu-id="7883e-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="7883e-113">Az első parancs az Azure Traffic Manager-profilt a **Get-AzureRmTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7883e-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="7883e-114">A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.</span><span class="sxs-lookup"><span data-stu-id="7883e-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="7883e-115">A második parancs hozzáadja a contoso nevű végpontot az $TrafficManagerProfile tárolt profiljához.</span><span class="sxs-lookup"><span data-stu-id="7883e-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="7883e-116">A parancs a végponthoz tartozó konfigurációs adatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7883e-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="7883e-117">Ez a parancs csak a helyi objektumot módosítja.</span><span class="sxs-lookup"><span data-stu-id="7883e-117">This command changes only the local object.</span></span>

<span data-ttu-id="7883e-118">A végleges parancs frissíti a forgalomirányítási profilt az Azure-ban az $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="7883e-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="7883e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7883e-119">PARAMETERS</span></span>

### <span data-ttu-id="7883e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7883e-120">-DefaultProfile</span></span>
<span data-ttu-id="7883e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7883e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-122">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="7883e-122">-EndpointLocation</span></span>
<span data-ttu-id="7883e-123">A teljesítmény-továbbítási módszerben használandó végpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7883e-123">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="7883e-124">Ez a paraméter csak a ExternalEndpoints vagy a NestedEndpoints típusú végpontokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="7883e-124">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="7883e-125">Ezt a paramétert akkor kell megadnia, ha a teljesítményadatok-útválasztási módszert használja.</span><span class="sxs-lookup"><span data-stu-id="7883e-125">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="7883e-126">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="7883e-126">Specify an Azure region name.</span></span>
<span data-ttu-id="7883e-127">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="7883e-127">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-128">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7883e-128">-EndpointName</span></span>
<span data-ttu-id="7883e-129">Annak a forgalomirányító-végpontnak a nevét adja meg, amelyre a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="7883e-129">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-130">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="7883e-130">-EndpointStatus</span></span>
<span data-ttu-id="7883e-131">A végpont állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7883e-131">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="7883e-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="7883e-132">Valid values are:</span></span> 

- <span data-ttu-id="7883e-133">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="7883e-133">Enabled</span></span> 
- <span data-ttu-id="7883e-134">Tiltva</span><span class="sxs-lookup"><span data-stu-id="7883e-134">Disabled</span></span> 

<span data-ttu-id="7883e-135">Ha az állapot engedélyezve van, akkor a végpontok állapotát a program kikapcsolja, és a forgalom-útválasztási módszer tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7883e-135">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-136">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="7883e-136">-GeoMapping</span></span>
<span data-ttu-id="7883e-137">A végponthoz rendelt régiók listája a földrajzi forgalom útválasztási módszerének használatakor.</span><span class="sxs-lookup"><span data-stu-id="7883e-137">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="7883e-138">Kérjük, hogy az [elfogadott értékek teljes listáját](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)a Traffic Manager dokumentációjában találja.</span><span class="sxs-lookup"><span data-stu-id="7883e-138">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="7883e-139">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="7883e-139">-MinChildEndpoints</span></span>
<span data-ttu-id="7883e-140">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="7883e-140">Specify an Azure region name.</span></span>
<span data-ttu-id="7883e-141">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="7883e-141">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-142">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="7883e-142">-Priority</span></span>
<span data-ttu-id="7883e-143">Azt a prioritást adja meg, amelyet a forgalomirányítási rendel a végponthoz.</span><span class="sxs-lookup"><span data-stu-id="7883e-143">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="7883e-144">Ez a paraméter csak akkor használatos, ha a forgalomirányítási profil a Priority Traffic-Routing metódussal van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="7883e-144">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="7883e-145">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="7883e-145">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="7883e-146">Az alacsonyabb értékek magasabb prioritást jelentenek.</span><span class="sxs-lookup"><span data-stu-id="7883e-146">Lower values represent higher priority.</span></span>

<span data-ttu-id="7883e-147">Ha prioritást ad meg, a profil minden végpontján meg kell adnia a prioritást, és nincs két végpont sem osztható meg ugyanazzal a prioritási értékkel.</span><span class="sxs-lookup"><span data-stu-id="7883e-147">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="7883e-148">Ha nem adja meg a prioritásokat, a forgalomirányító a végpontokhoz rendeli az alapértelmezett prioritási értékeket a végpontokhoz (1) kezdve, abban a sorrendben, ahogyan a profil a végpontokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="7883e-148">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-149">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="7883e-149">-Target</span></span>
<span data-ttu-id="7883e-150">A végpont teljesen minősített DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7883e-150">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="7883e-151">A Traffic Manager ezt az értéket a DNS-válaszokban akkor jeleníti meg, amikor a forgalmat a végpontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="7883e-151">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="7883e-152">Ezt a paramétert csak a ExternalEndpoints végpont típusára adja meg.</span><span class="sxs-lookup"><span data-stu-id="7883e-152">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="7883e-153">A többi végpont típusnál adja meg ehelyett a *TargetResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="7883e-153">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7883e-154">-TargetResourceId</span></span>
<span data-ttu-id="7883e-155">A cél erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7883e-155">Specifies resource ID of the target.</span></span>
<span data-ttu-id="7883e-156">Ezt a paramétert csak a AzureEndpoints és a NestedEndpoints végpont típusához adja meg.</span><span class="sxs-lookup"><span data-stu-id="7883e-156">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="7883e-157">A ExternalEndpoints végpont típusnál adja meg ehelyett a *cél* paramétert.</span><span class="sxs-lookup"><span data-stu-id="7883e-157">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-158">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7883e-158">-TrafficManagerProfile</span></span>
<span data-ttu-id="7883e-159">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7883e-159">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="7883e-160">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="7883e-160">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="7883e-161">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7883e-161">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-162">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="7883e-162">-Type</span></span>
<span data-ttu-id="7883e-163">Azt adja meg, hogy a parancsmag milyen típusú végpontot ad az Azure Traffic Manager profiljához.</span><span class="sxs-lookup"><span data-stu-id="7883e-163">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7883e-164">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="7883e-164">Valid values are:</span></span> 

- <span data-ttu-id="7883e-165">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="7883e-165">AzureEndpoints</span></span>
- <span data-ttu-id="7883e-166">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="7883e-166">ExternalEndpoints</span></span>
- <span data-ttu-id="7883e-167">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="7883e-167">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-168">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="7883e-168">-Weight</span></span>
<span data-ttu-id="7883e-169">A forgalomirányító által a végponthoz hozzárendelt vastagságot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7883e-169">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="7883e-170">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="7883e-170">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="7883e-171">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="7883e-171">The default value is one (1).</span></span>
<span data-ttu-id="7883e-172">Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja a súlyozott forgalom-útválasztási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="7883e-172">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7883e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7883e-173">CommonParameters</span></span>
<span data-ttu-id="7883e-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7883e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7883e-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7883e-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7883e-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7883e-176">INPUTS</span></span>

### <span data-ttu-id="7883e-177">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7883e-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="7883e-178">Ez a parancsmag egy **TrafficManagerProfile** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="7883e-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="7883e-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7883e-179">OUTPUTS</span></span>

### <span data-ttu-id="7883e-180">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7883e-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="7883e-181">Ez a parancsmag egy módosított **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7883e-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="7883e-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7883e-182">NOTES</span></span>

## <span data-ttu-id="7883e-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7883e-183">RELATED LINKS</span></span>

[<span data-ttu-id="7883e-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7883e-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7883e-185">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7883e-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7883e-186">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="7883e-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="7883e-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7883e-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


