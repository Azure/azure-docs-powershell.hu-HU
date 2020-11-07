---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 6117bbae035653762d99096eb8735885c0554d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673201"
---
# <span data-ttu-id="db6c3-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="db6c3-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="db6c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="db6c3-103">A forgalomirányító-profilban hoz létre végpontot.</span><span class="sxs-lookup"><span data-stu-id="db6c3-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db6c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db6c3-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db6c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db6c3-105">DESCRIPTION</span></span>
<span data-ttu-id="db6c3-106">A **New-AzureRmTrafficManagerEndpoint** parancsmag létrehoz egy végpontot az Azure Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="db6c3-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="db6c3-107">Ez a parancsmag minden új végpontot véglegesít a forgalomirányítási szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="db6c3-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="db6c3-108">Ha több végpontot szeretne felvenni egy helyi forgalomirányítási profil objektumba, és egyetlen műveletben szeretne módosításokat végrehajtani, használja az Add-AzureRmTrafficManagerEndpointConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="db6c3-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="db6c3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="db6c3-109">EXAMPLES</span></span>

### <span data-ttu-id="db6c3-110">Példa 1: külső végpont létrehozása profilhoz</span><span class="sxs-lookup"><span data-stu-id="db6c3-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="db6c3-111">Ez a parancs létrehoz egy contoso nevű külső végpontot a ResourceGroup11 nevű erőforráscsoport ContosoProfile nevű profiljában.</span><span class="sxs-lookup"><span data-stu-id="db6c3-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="db6c3-112">2. példa: Azure-végpont létrehozása profilhoz</span><span class="sxs-lookup"><span data-stu-id="db6c3-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="db6c3-113">A parancs létrehoz egy contoso nevű Azure-végpontot az erőforráscsoport ResouceGroup11 nevű ContosoProfile-profilban.</span><span class="sxs-lookup"><span data-stu-id="db6c3-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="db6c3-114">Az Azure-végpont arra az Azure Web App-pontra mutat, amelynek az Azure Resource Manager AZONOSÍTÓját az *TARGETRESOURCEID* URI elérési útja adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="db6c3-115">A parancs nem adja meg a *EndpointLocation* paramétert, mert a Web App-erőforrás megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="db6c3-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="db6c3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db6c3-116">PARAMETERS</span></span>

### <span data-ttu-id="db6c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6c3-117">-DefaultProfile</span></span>
<span data-ttu-id="db6c3-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db6c3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6c3-119">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="db6c3-119">-EndpointLocation</span></span>
<span data-ttu-id="db6c3-120">A teljesítmény-továbbítási módszerben használandó végpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-120">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="db6c3-121">Ez a paraméter csak a ExternalEndpoints vagy a NestedEndpoints típusú végpontokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="db6c3-121">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="db6c3-122">Ezt a paramétert akkor kell megadnia, ha a teljesítményadatok-útválasztási módszert használja.</span><span class="sxs-lookup"><span data-stu-id="db6c3-122">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="db6c3-123">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="db6c3-123">Specify an Azure region name.</span></span>
<span data-ttu-id="db6c3-124">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="db6c3-124">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="db6c3-125">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="db6c3-125">-EndpointStatus</span></span>
<span data-ttu-id="db6c3-126">A végpont állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-126">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="db6c3-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="db6c3-127">Valid values are:</span></span> 

- <span data-ttu-id="db6c3-128">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="db6c3-128">Enabled</span></span> 
- <span data-ttu-id="db6c3-129">Tiltva</span><span class="sxs-lookup"><span data-stu-id="db6c3-129">Disabled</span></span> 

<span data-ttu-id="db6c3-130">Ha az állapot engedélyezve van, akkor a végpontok állapotát a program kikapcsolja, és a forgalom-útválasztási módszer tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="db6c3-130">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="db6c3-131">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="db6c3-131">-GeoMapping</span></span>
<span data-ttu-id="db6c3-132">A végponthoz rendelt régiók listája a földrajzi forgalom útválasztási módszerének használatakor.</span><span class="sxs-lookup"><span data-stu-id="db6c3-132">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="db6c3-133">Kérjük, hogy az elfogadott értékek teljes listáját a Traffic Manager dokumentációjában találja.</span><span class="sxs-lookup"><span data-stu-id="db6c3-133">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="db6c3-134">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="db6c3-134">-MinChildEndpoints</span></span>
<span data-ttu-id="db6c3-135">Adjon meg egy Azure region nevet.</span><span class="sxs-lookup"><span data-stu-id="db6c3-135">Specify an Azure region name.</span></span>
<span data-ttu-id="db6c3-136">Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="db6c3-136">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="db6c3-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db6c3-137">-Name</span></span>
<span data-ttu-id="db6c3-138">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="db6c3-138">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="db6c3-139">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="db6c3-139">-Priority</span></span>
<span data-ttu-id="db6c3-140">Azt a prioritást adja meg, amelyet a forgalomirányítási rendel a végponthoz.</span><span class="sxs-lookup"><span data-stu-id="db6c3-140">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="db6c3-141">Ez a paraméter csak akkor használatos, ha a forgalomirányítási profil a Priority Traffic-Routing metódussal van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="db6c3-141">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="db6c3-142">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="db6c3-142">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="db6c3-143">Az alacsonyabb értékek magasabb prioritást jelentenek.</span><span class="sxs-lookup"><span data-stu-id="db6c3-143">Lower values represent higher priority.</span></span>

<span data-ttu-id="db6c3-144">Ha prioritást ad meg, a profil minden végpontján meg kell adnia a prioritást, és nincs két végpont sem osztható meg ugyanazzal a prioritási értékkel.</span><span class="sxs-lookup"><span data-stu-id="db6c3-144">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="db6c3-145">Ha nem adja meg a prioritásokat, a forgalomirányító a végpontokhoz rendeli az alapértelmezett prioritási értékeket a végpontokhoz (1) kezdve, abban a sorrendben, ahogyan a profil a végpontokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="db6c3-145">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="db6c3-146">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="db6c3-146">-ProfileName</span></span>
<span data-ttu-id="db6c3-147">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag hozzáadja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="db6c3-147">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="db6c3-148">Ha profilt szeretne beolvasni, használja az New-AzureRmTrafficManagerProfile vagy Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="db6c3-148">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="db6c3-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db6c3-149">-ResourceGroupName</span></span>
<span data-ttu-id="db6c3-150">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="db6c3-151">Ez a parancsmag egy forgalomirányítási végpontot hoz létre abban a csoportban, amelyben ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-151">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="db6c3-152">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="db6c3-152">-Target</span></span>
<span data-ttu-id="db6c3-153">A végpont teljesen minősített DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-153">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="db6c3-154">A Traffic Manager ezt az értéket a DNS-válaszokban akkor jeleníti meg, amikor a forgalmat a végpontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="db6c3-154">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="db6c3-155">Ezt a paramétert csak a ExternalEndpoints végpont típusára adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-155">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="db6c3-156">A többi végpont típusnál adja meg ehelyett a *TargetResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="db6c3-156">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="db6c3-157">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="db6c3-157">-TargetResourceId</span></span>
<span data-ttu-id="db6c3-158">A cél erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-158">Specifies resource ID of the target.</span></span>
<span data-ttu-id="db6c3-159">Ezt a paramétert csak a AzureEndpoints és a NestedEndpoints végpont típusához adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-159">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="db6c3-160">A ExternalEndpoints végpont típusnál adja meg ehelyett a *cél* paramétert.</span><span class="sxs-lookup"><span data-stu-id="db6c3-160">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="db6c3-161">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="db6c3-161">-Type</span></span>
<span data-ttu-id="db6c3-162">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="db6c3-162">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="db6c3-163">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="db6c3-163">Valid values are:</span></span> 

- <span data-ttu-id="db6c3-164">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="db6c3-164">AzureEndpoints</span></span>
- <span data-ttu-id="db6c3-165">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="db6c3-165">ExternalEndpoints</span></span>
- <span data-ttu-id="db6c3-166">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="db6c3-166">NestedEndpoints</span></span>

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

### <span data-ttu-id="db6c3-167">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="db6c3-167">-Weight</span></span>
<span data-ttu-id="db6c3-168">A forgalomirányító által a végponthoz hozzárendelt vastagságot adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6c3-168">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="db6c3-169">Az érvényes értékek 1 és 1000 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="db6c3-169">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="db6c3-170">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="db6c3-170">The default value is one (1).</span></span>
<span data-ttu-id="db6c3-171">Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja a súlyozott forgalom-útválasztási módszerrel van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="db6c3-171">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="db6c3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6c3-172">CommonParameters</span></span>
<span data-ttu-id="db6c3-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db6c3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6c3-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6c3-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6c3-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db6c3-175">INPUTS</span></span>

### <span data-ttu-id="db6c3-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="db6c3-176">None</span></span>
<span data-ttu-id="db6c3-177">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="db6c3-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db6c3-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db6c3-178">OUTPUTS</span></span>

### <span data-ttu-id="db6c3-179">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="db6c3-179">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="db6c3-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db6c3-180">NOTES</span></span>

## <span data-ttu-id="db6c3-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db6c3-181">RELATED LINKS</span></span>

[<span data-ttu-id="db6c3-182">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="db6c3-182">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="db6c3-183">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="db6c3-183">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="db6c3-184">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="db6c3-184">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="db6c3-185">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="db6c3-185">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="db6c3-186">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="db6c3-186">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="db6c3-187">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="db6c3-187">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="db6c3-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="db6c3-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


