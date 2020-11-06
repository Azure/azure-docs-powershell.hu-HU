---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: f2abe6acd0406f78ba2bb691b562cd0bcbffeb35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492456"
---
# <span data-ttu-id="deca8-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="deca8-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="deca8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="deca8-102">SYNOPSIS</span></span>
<span data-ttu-id="deca8-103">Egy végpontot ad hozzá egy helyi forgalomirányítási profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="deca8-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deca8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="deca8-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="deca8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="deca8-105">DESCRIPTION</span></span>
<span data-ttu-id="deca8-106">A **Add-AzureRmTrafficManagerEndpointConfig** parancsmag hozzáad egy végpontot egy helyi Azure Traffic Manager-profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="deca8-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="deca8-107">A New-AzureRmTrafficManagerProfile-vagy Get-AzureRmTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="deca8-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="deca8-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="deca8-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="deca8-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="deca8-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="deca8-110">Ha végpontot szeretne létrehozni, és egyetlen műveletben szeretné végrehajtani a változást, használja az New-AzureRmTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="deca8-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="deca8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="deca8-111">EXAMPLES</span></span>

### <span data-ttu-id="deca8-112">1. példa: végpont felvétele a profilba</span><span class="sxs-lookup"><span data-stu-id="deca8-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="deca8-113">Az első parancs az Azure Traffic Manager-profilt a **Get-AzureRmTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="deca8-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="deca8-114">A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.</span><span class="sxs-lookup"><span data-stu-id="deca8-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="deca8-115">A második parancs hozzáadja a contoso nevű végpontot az $TrafficManagerProfile tárolt profiljához.</span><span class="sxs-lookup"><span data-stu-id="deca8-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="deca8-116">A parancs a végponthoz tartozó konfigurációs adatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="deca8-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="deca8-117">Ez a parancs csak a helyi objektumot módosítja.</span><span class="sxs-lookup"><span data-stu-id="deca8-117">This command changes only the local object.</span></span>

<span data-ttu-id="deca8-118">A végleges parancs frissíti a forgalomirányítási profilt az Azure-ban az $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="deca8-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="deca8-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="deca8-119">PARAMETERS</span></span>

### <span data-ttu-id="deca8-120">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="deca8-120">-EndpointLocation</span></span>
<span data-ttu-id="deca8-121">A teljesítmény-továbbítási módszerben használandó végpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="deca8-121">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="deca8-122">Ez a paraméter csak a ExternalEndpoints vagy a NestedEndpoints típusú végpontokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="deca8-122">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="deca8-123">Ezt a paramétert akkor kell megadnia, ha a teljesítményadatok-útválasztási módszert használja.</span><span class="sxs-lookup"><span data-stu-id="deca8-123">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="deca8-124">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="deca8-124">Specify an Azure region name.</span></span>
<span data-ttu-id="deca8-125">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="deca8-125">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="deca8-126">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="deca8-126">-EndpointName</span></span>
<span data-ttu-id="deca8-127">Annak a forgalomirányító-végpontnak a nevét adja meg, amelyre a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="deca8-127">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="deca8-128">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="deca8-128">-EndpointStatus</span></span>
<span data-ttu-id="deca8-129">A végpont állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="deca8-129">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="deca8-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="deca8-130">Valid values are:</span></span> 

- <span data-ttu-id="deca8-131">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="deca8-131">Enabled</span></span> 
- <span data-ttu-id="deca8-132">Tiltva</span><span class="sxs-lookup"><span data-stu-id="deca8-132">Disabled</span></span> 

<span data-ttu-id="deca8-133">Ha az állapot engedélyezve van, akkor a végpontok állapotát a program kikapcsolja, és a forgalom-útválasztási módszer tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="deca8-133">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="deca8-134">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="deca8-134">-GeoMapping</span></span>
<span data-ttu-id="deca8-135">A végponthoz rendelt régiók listája a földrajzi forgalom útválasztási módszerének használatakor.</span><span class="sxs-lookup"><span data-stu-id="deca8-135">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="deca8-136">Kérjük, hogy az [elfogadott értékek teljes listáját](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)a Traffic Manager dokumentációjában találja.</span><span class="sxs-lookup"><span data-stu-id="deca8-136">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="deca8-137">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="deca8-137">-MinChildEndpoints</span></span>
<span data-ttu-id="deca8-138">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="deca8-138">Specify an Azure region name.</span></span>
<span data-ttu-id="deca8-139">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="deca8-139">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="deca8-140">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="deca8-140">-Priority</span></span>
<span data-ttu-id="deca8-141">Azt a prioritást adja meg, amelyet a forgalomirányítási rendel a végponthoz.</span><span class="sxs-lookup"><span data-stu-id="deca8-141">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="deca8-142">Ez a paraméter csak akkor használatos, ha a forgalomirányítási profil a Priority Traffic-Routing metódussal van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="deca8-142">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="deca8-143">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="deca8-143">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="deca8-144">Az alacsonyabb értékek magasabb prioritást jelentenek.</span><span class="sxs-lookup"><span data-stu-id="deca8-144">Lower values represent higher priority.</span></span>

<span data-ttu-id="deca8-145">Ha prioritást ad meg, a profil minden végpontján meg kell adnia a prioritást, és nincs két végpont sem osztható meg ugyanazzal a prioritási értékkel.</span><span class="sxs-lookup"><span data-stu-id="deca8-145">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="deca8-146">Ha nem adja meg a prioritásokat, a forgalomirányító a végpontokhoz rendeli az alapértelmezett prioritási értékeket a végpontokhoz (1) kezdve, abban a sorrendben, ahogyan a profil a végpontokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="deca8-146">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="deca8-147">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="deca8-147">-Target</span></span>
<span data-ttu-id="deca8-148">A végpont teljesen minősített DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="deca8-148">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="deca8-149">A Traffic Manager ezt az értéket a DNS-válaszokban akkor jeleníti meg, amikor a forgalmat a végpontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="deca8-149">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="deca8-150">Ezt a paramétert csak a ExternalEndpoints végpont típusára adja meg.</span><span class="sxs-lookup"><span data-stu-id="deca8-150">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="deca8-151">A többi végpont típusnál adja meg ehelyett a *TargetResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="deca8-151">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="deca8-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="deca8-152">-TargetResourceId</span></span>
<span data-ttu-id="deca8-153">A cél erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="deca8-153">Specifies resource ID of the target.</span></span>
<span data-ttu-id="deca8-154">Ezt a paramétert csak a AzureEndpoints és a NestedEndpoints végpont típusához adja meg.</span><span class="sxs-lookup"><span data-stu-id="deca8-154">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="deca8-155">A ExternalEndpoints végpont típusnál adja meg ehelyett a *cél* paramétert.</span><span class="sxs-lookup"><span data-stu-id="deca8-155">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="deca8-156">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="deca8-156">-TrafficManagerProfile</span></span>
<span data-ttu-id="deca8-157">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="deca8-157">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="deca8-158">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="deca8-158">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="deca8-159">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="deca8-159">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="deca8-160">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="deca8-160">-Type</span></span>
<span data-ttu-id="deca8-161">Azt adja meg, hogy a parancsmag milyen típusú végpontot ad az Azure Traffic Manager profiljához.</span><span class="sxs-lookup"><span data-stu-id="deca8-161">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="deca8-162">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="deca8-162">Valid values are:</span></span> 

- <span data-ttu-id="deca8-163">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="deca8-163">AzureEndpoints</span></span>
- <span data-ttu-id="deca8-164">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="deca8-164">ExternalEndpoints</span></span>
- <span data-ttu-id="deca8-165">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="deca8-165">NestedEndpoints</span></span>

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

### <span data-ttu-id="deca8-166">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="deca8-166">-Weight</span></span>
<span data-ttu-id="deca8-167">A forgalomirányító által a végponthoz hozzárendelt vastagságot adja meg.</span><span class="sxs-lookup"><span data-stu-id="deca8-167">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="deca8-168">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="deca8-168">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="deca8-169">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="deca8-169">The default value is one (1).</span></span>
<span data-ttu-id="deca8-170">Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja a súlyozott forgalom-útválasztási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="deca8-170">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="deca8-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deca8-171">-DefaultProfile</span></span>
<span data-ttu-id="deca8-172">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="deca8-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deca8-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deca8-173">CommonParameters</span></span>
<span data-ttu-id="deca8-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="deca8-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deca8-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deca8-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deca8-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="deca8-176">INPUTS</span></span>

### <span data-ttu-id="deca8-177">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="deca8-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="deca8-178">Ez a parancsmag egy **TrafficManagerProfile** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="deca8-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="deca8-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deca8-179">OUTPUTS</span></span>

### <span data-ttu-id="deca8-180">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="deca8-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="deca8-181">Ez a parancsmag egy módosított **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="deca8-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="deca8-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="deca8-182">NOTES</span></span>

## <span data-ttu-id="deca8-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deca8-183">RELATED LINKS</span></span>

[<span data-ttu-id="deca8-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="deca8-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="deca8-185">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="deca8-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="deca8-186">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="deca8-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="deca8-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="deca8-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


