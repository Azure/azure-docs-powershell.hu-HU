---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479042"
---
# <span data-ttu-id="7bde2-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="7bde2-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="7bde2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bde2-102">SYNOPSIS</span></span>
<span data-ttu-id="7bde2-103">Új telepítési régiók hozzáadása a PsApiManagement-példányhoz.</span><span class="sxs-lookup"><span data-stu-id="7bde2-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="7bde2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7bde2-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bde2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7bde2-105">DESCRIPTION</span></span>
<span data-ttu-id="7bde2-106">Az **Add-AzApiManagementRegion** parancsmag hozzáadja a **PsApiManagementRegion** új példányát a **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement** típusú megadott példány **AdditionalRegions** gyűjteményéhez.</span><span class="sxs-lookup"><span data-stu-id="7bde2-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="7bde2-107">Ez a parancsmag nem telepít semmit önmagában, de frissíti a **PsApiManagement** in-memory példányát.</span><span class="sxs-lookup"><span data-stu-id="7bde2-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="7bde2-108">Egy API-kezelés telepítésének frissítéséhez át kell adni a **módosított PsApiManagement-példányt** a Set-AzApiManagementnek.</span><span class="sxs-lookup"><span data-stu-id="7bde2-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="7bde2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7bde2-109">EXAMPLES</span></span>

### <span data-ttu-id="7bde2-110">1. példa: Új telepítési régiók hozzáadása a PsApiManagement-példányhoz</span><span class="sxs-lookup"><span data-stu-id="7bde2-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="7bde2-111">Ez a parancs hozzáad két prémium termékváltozatot és a Kelet-US régiót a **PsApiManagement példányhoz.**</span><span class="sxs-lookup"><span data-stu-id="7bde2-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="7bde2-112">2. példa: Új telepítési régiók hozzáadása a PsApiManagement-példányhoz, majd a telepítés frissítése</span><span class="sxs-lookup"><span data-stu-id="7bde2-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="7bde2-113">Ez a parancs egy **PsApiManagement** objektumot kap, hozzáad két prémium termékváltozatot az EGYESÜLT Államok keleti régiója számára, majd frissíti az üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="7bde2-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="7bde2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bde2-114">PARAMETERS</span></span>

### <span data-ttu-id="7bde2-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7bde2-115">-ApiManagement</span></span>
<span data-ttu-id="7bde2-116">Azt a **PsApiManagement-példányt** adja meg, amelybe a parancsmag további telepítési régiókat ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="7bde2-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="7bde2-117">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="7bde2-117">-Capacity</span></span>
<span data-ttu-id="7bde2-118">A telepítési régió termékváltozatának kapacitását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7bde2-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="7bde2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bde2-119">-DefaultProfile</span></span>
<span data-ttu-id="7bde2-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bde2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bde2-121">-Location</span><span class="sxs-lookup"><span data-stu-id="7bde2-121">-Location</span></span>
<span data-ttu-id="7bde2-122">Megadja az új telepítési régió helyét az Api Management szolgáltatás támogatott régiója között.</span><span class="sxs-lookup"><span data-stu-id="7bde2-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="7bde2-123">Érvényes helyek beszerzéséhez használja a Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" parancsmagot | ahol {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="7bde2-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="7bde2-124">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="7bde2-124">-Sku</span></span>
<span data-ttu-id="7bde2-125">Az üzembe helyezési régió rétegét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7bde2-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="7bde2-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="7bde2-126">Valid values are:</span></span> 
- <span data-ttu-id="7bde2-127">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="7bde2-127">Developer</span></span>
- <span data-ttu-id="7bde2-128">Normál</span><span class="sxs-lookup"><span data-stu-id="7bde2-128">Standard</span></span>
- <span data-ttu-id="7bde2-129">Prémium</span><span class="sxs-lookup"><span data-stu-id="7bde2-129">Premium</span></span>

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

### <span data-ttu-id="7bde2-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bde2-130">-VirtualNetwork</span></span>
<span data-ttu-id="7bde2-131">Virtuális hálózati konfigurációt ad meg.</span><span class="sxs-lookup"><span data-stu-id="7bde2-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="7bde2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bde2-132">CommonParameters</span></span>
<span data-ttu-id="7bde2-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bde2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bde2-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bde2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bde2-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bde2-135">INPUTS</span></span>

### <span data-ttu-id="7bde2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="7bde2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="7bde2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bde2-137">OUTPUTS</span></span>

### <span data-ttu-id="7bde2-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="7bde2-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="7bde2-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7bde2-139">NOTES</span></span>
* <span data-ttu-id="7bde2-140">A parancsmag a frissített **PsApiManagement-példányt** folyamatba írja.</span><span class="sxs-lookup"><span data-stu-id="7bde2-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="7bde2-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bde2-141">RELATED LINKS</span></span>

[<span data-ttu-id="7bde2-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="7bde2-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="7bde2-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="7bde2-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="7bde2-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="7bde2-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


