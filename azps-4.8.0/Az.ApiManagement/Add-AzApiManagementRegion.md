---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024971"
---
# <span data-ttu-id="db832-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="db832-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="db832-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db832-102">SYNOPSIS</span></span>
<span data-ttu-id="db832-103">Új központi terjesztési régiók felvétele egy PsApiManagement-példányba.</span><span class="sxs-lookup"><span data-stu-id="db832-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="db832-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db832-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db832-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db832-105">DESCRIPTION</span></span>
<span data-ttu-id="db832-106">Az **Add-AzApiManagementRegion** parancsmag a **PsApiManagementRegion** új példányát adja a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagement** **AdditionalRegions** példányának.</span><span class="sxs-lookup"><span data-stu-id="db832-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="db832-107">Ez a parancsmag nem telepíti magát semmit, de a memória **PsApiManagement** példányát frissíti.</span><span class="sxs-lookup"><span data-stu-id="db832-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="db832-108">Ha frissíteni szeretné egy API-kezelés telepített példányát, a módosított **PsApiManagement** -példányt adja meg a set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="db832-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="db832-109">Példák</span><span class="sxs-lookup"><span data-stu-id="db832-109">EXAMPLES</span></span>

### <span data-ttu-id="db832-110">1. példa: új központi terjesztési régiók felvétele PsApiManagement-példányba</span><span class="sxs-lookup"><span data-stu-id="db832-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="db832-111">Ez a parancs két prémium SKU-egységet és a kelet-amerikai régiót a **PsApiManagement** -példányra helyezi.</span><span class="sxs-lookup"><span data-stu-id="db832-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="db832-112">2. példa: új üzembe állítási régiók felvétele PsApiManagement-példányba, majd a központi telepítő frissítése</span><span class="sxs-lookup"><span data-stu-id="db832-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="db832-113">Ez a parancs **PsApiManagement** objektumot kap, és két prémium SKU-egységet ad hozzá a kelet-amerikai régióhoz, majd frissíti a központi üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="db832-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="db832-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db832-114">PARAMETERS</span></span>

### <span data-ttu-id="db832-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db832-115">-ApiManagement</span></span>
<span data-ttu-id="db832-116">Azt a **PsApiManagement** -példányt adja meg, amelyre a parancsmag további központi terjesztési területeket ad.</span><span class="sxs-lookup"><span data-stu-id="db832-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db832-117">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="db832-117">-Capacity</span></span>
<span data-ttu-id="db832-118">A központi telepítő terület SKU-kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="db832-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db832-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db832-119">-DefaultProfile</span></span>
<span data-ttu-id="db832-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db832-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db832-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="db832-121">-Location</span></span>
<span data-ttu-id="db832-122">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="db832-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="db832-123">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="db832-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="db832-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="db832-124">-Sku</span></span>
<span data-ttu-id="db832-125">A központi telepítő terület küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db832-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="db832-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="db832-126">Valid values are:</span></span> 
- <span data-ttu-id="db832-127">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="db832-127">Developer</span></span>
- <span data-ttu-id="db832-128">Standard</span><span class="sxs-lookup"><span data-stu-id="db832-128">Standard</span></span>
- <span data-ttu-id="db832-129">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="db832-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db832-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db832-130">-VirtualNetwork</span></span>
<span data-ttu-id="db832-131">Virtuális hálózati konfigurációt ad meg.</span><span class="sxs-lookup"><span data-stu-id="db832-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db832-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db832-132">CommonParameters</span></span>
<span data-ttu-id="db832-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db832-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db832-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="db832-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db832-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db832-135">INPUTS</span></span>

### <span data-ttu-id="db832-136">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="db832-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="db832-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db832-137">OUTPUTS</span></span>

### <span data-ttu-id="db832-138">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="db832-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="db832-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db832-139">NOTES</span></span>
* <span data-ttu-id="db832-140">A parancsmag frissített **PsApiManagement** -példányt ír a pipeline-ra.</span><span class="sxs-lookup"><span data-stu-id="db832-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="db832-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db832-141">RELATED LINKS</span></span>

[<span data-ttu-id="db832-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="db832-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="db832-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="db832-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="db832-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="db832-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


