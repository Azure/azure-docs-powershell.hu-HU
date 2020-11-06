---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 7eaadd8c80fff6491983a3e1d9c750227eba43cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492453"
---
# <span data-ttu-id="c7eb6-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7eb6-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="c7eb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="c7eb6-103">A forgalomirányító-profilban hoz létre végpontot.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7eb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7eb6-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7eb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="c7eb6-106">A **New-AzureRmTrafficManagerEndpoint** parancsmag létrehoz egy végpontot az Azure Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="c7eb6-107">Ez a parancsmag minden új végpontot véglegesít a forgalomirányítási szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="c7eb6-108">Ha több végpontot szeretne felvenni egy helyi forgalomirányítási profil objektumba, és egyetlen műveletben szeretne módosításokat végrehajtani, használja az Add-AzureRmTrafficManagerEndpointConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="c7eb6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c7eb6-109">EXAMPLES</span></span>

### <span data-ttu-id="c7eb6-110">Példa 1: külső végpont létrehozása profilhoz</span><span class="sxs-lookup"><span data-stu-id="c7eb6-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="c7eb6-111">Ez a parancs létrehoz egy contoso nevű külső végpontot a ResourceGroup11 nevű erőforráscsoport ContosoProfile nevű profiljában.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="c7eb6-112">2. példa: Azure-végpont létrehozása profilhoz</span><span class="sxs-lookup"><span data-stu-id="c7eb6-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="c7eb6-113">A parancs létrehoz egy contoso nevű Azure-végpontot az erőforráscsoport ResouceGroup11 nevű ContosoProfile-profilban.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="c7eb6-114">Az Azure-végpont arra az Azure Web App-pontra mutat, amelynek az Azure Resource Manager AZONOSÍTÓját az *TARGETRESOURCEID* URI elérési útja adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="c7eb6-115">A parancs nem adja meg a *EndpointLocation* paramétert, mert a Web App-erőforrás megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="c7eb6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7eb6-116">PARAMETERS</span></span>

### <span data-ttu-id="c7eb6-117">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="c7eb6-117">-EndpointLocation</span></span>
<span data-ttu-id="c7eb6-118">A teljesítmény-továbbítási módszerben használandó végpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-118">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="c7eb6-119">Ez a paraméter csak a ExternalEndpoints vagy a NestedEndpoints típusú végpontokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-119">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="c7eb6-120">Ezt a paramétert akkor kell megadnia, ha a teljesítményadatok-útválasztási módszert használja.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-120">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="c7eb6-121">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-121">Specify an Azure region name.</span></span>
<span data-ttu-id="c7eb6-122">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="c7eb6-122">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="c7eb6-123">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="c7eb6-123">-EndpointStatus</span></span>
<span data-ttu-id="c7eb6-124">A végpont állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-124">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="c7eb6-125">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="c7eb6-125">Valid values are:</span></span> 

- <span data-ttu-id="c7eb6-126">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="c7eb6-126">Enabled</span></span> 
- <span data-ttu-id="c7eb6-127">Tiltva</span><span class="sxs-lookup"><span data-stu-id="c7eb6-127">Disabled</span></span> 

<span data-ttu-id="c7eb6-128">Ha az állapot engedélyezve van, akkor a végpontok állapotát a program kikapcsolja, és a forgalom-útválasztási módszer tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-128">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="c7eb6-129">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="c7eb6-129">-GeoMapping</span></span>
<span data-ttu-id="c7eb6-130">A végponthoz rendelt régiók listája a földrajzi forgalom útválasztási módszerének használatakor.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-130">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="c7eb6-131">Kérjük, hogy az elfogadott értékek teljes listáját a Traffic Manager dokumentációjában találja.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-131">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="c7eb6-132">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="c7eb6-132">-MinChildEndpoints</span></span>
<span data-ttu-id="c7eb6-133">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-133">Specify an Azure region name.</span></span>
<span data-ttu-id="c7eb6-134">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="c7eb6-134">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="c7eb6-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7eb6-135">-Name</span></span>
<span data-ttu-id="c7eb6-136">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-136">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c7eb6-137">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="c7eb6-137">-Priority</span></span>
<span data-ttu-id="c7eb6-138">Azt a prioritást adja meg, amelyet a forgalomirányítási rendel a végponthoz.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-138">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="c7eb6-139">Ez a paraméter csak akkor használatos, ha a forgalomirányítási profil a Priority Traffic-Routing metódussal van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-139">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="c7eb6-140">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-140">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="c7eb6-141">Az alacsonyabb értékek magasabb prioritást jelentenek.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-141">Lower values represent higher priority.</span></span>

<span data-ttu-id="c7eb6-142">Ha prioritást ad meg, a profil minden végpontján meg kell adnia a prioritást, és nincs két végpont sem osztható meg ugyanazzal a prioritási értékkel.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-142">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="c7eb6-143">Ha nem adja meg a prioritásokat, a forgalomirányító a végpontokhoz rendeli az alapértelmezett prioritási értékeket a végpontokhoz (1) kezdve, abban a sorrendben, ahogyan a profil a végpontokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-143">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="c7eb6-144">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="c7eb6-144">-ProfileName</span></span>
<span data-ttu-id="c7eb6-145">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag hozzáadja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-145">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="c7eb6-146">Ha profilt szeretne beolvasni, használja az New-AzureRmTrafficManagerProfile vagy Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-146">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="c7eb6-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7eb6-147">-ResourceGroupName</span></span>
<span data-ttu-id="c7eb6-148">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c7eb6-149">Ez a parancsmag egy forgalomirányítási végpontot hoz létre abban a csoportban, amelyben ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-149">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c7eb6-150">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="c7eb6-150">-Target</span></span>
<span data-ttu-id="c7eb6-151">A végpont teljesen minősített DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-151">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="c7eb6-152">A Traffic Manager ezt az értéket a DNS-válaszokban akkor jeleníti meg, amikor a forgalmat a végpontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-152">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="c7eb6-153">Ezt a paramétert csak a ExternalEndpoints végpont típusára adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-153">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="c7eb6-154">A többi végpont típusnál adja meg ehelyett a *TargetResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-154">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="c7eb6-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c7eb6-155">-TargetResourceId</span></span>
<span data-ttu-id="c7eb6-156">A cél erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-156">Specifies resource ID of the target.</span></span>
<span data-ttu-id="c7eb6-157">Ezt a paramétert csak a AzureEndpoints és a NestedEndpoints végpont típusához adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-157">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="c7eb6-158">A ExternalEndpoints végpont típusnál adja meg ehelyett a *cél* paramétert.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-158">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="c7eb6-159">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="c7eb6-159">-Type</span></span>
<span data-ttu-id="c7eb6-160">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-160">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="c7eb6-161">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="c7eb6-161">Valid values are:</span></span> 

- <span data-ttu-id="c7eb6-162">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="c7eb6-162">AzureEndpoints</span></span>
- <span data-ttu-id="c7eb6-163">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="c7eb6-163">ExternalEndpoints</span></span>
- <span data-ttu-id="c7eb6-164">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="c7eb6-164">NestedEndpoints</span></span>

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

### <span data-ttu-id="c7eb6-165">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="c7eb6-165">-Weight</span></span>
<span data-ttu-id="c7eb6-166">A forgalomirányító által a végponthoz hozzárendelt vastagságot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-166">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="c7eb6-167">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-167">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="c7eb6-168">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="c7eb6-168">The default value is one (1).</span></span>
<span data-ttu-id="c7eb6-169">Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja a súlyozott forgalom-útválasztási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-169">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="c7eb6-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7eb6-170">-DefaultProfile</span></span>
<span data-ttu-id="c7eb6-171">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7eb6-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7eb6-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7eb6-172">CommonParameters</span></span>
<span data-ttu-id="c7eb6-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7eb6-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7eb6-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7eb6-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7eb6-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7eb6-175">INPUTS</span></span>

## <span data-ttu-id="c7eb6-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7eb6-176">OUTPUTS</span></span>

### <span data-ttu-id="c7eb6-177">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7eb6-177">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c7eb6-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7eb6-178">NOTES</span></span>

## <span data-ttu-id="c7eb6-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7eb6-179">RELATED LINKS</span></span>

[<span data-ttu-id="c7eb6-180">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7eb6-180">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c7eb6-181">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7eb6-181">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c7eb6-182">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7eb6-182">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c7eb6-183">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7eb6-183">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c7eb6-184">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7eb6-184">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c7eb6-185">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7eb6-185">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c7eb6-186">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7eb6-186">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


