---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 3f9c88177d3f791acdd0be5c81eec2fb5bc6911c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400705"
---
# <span data-ttu-id="ff0e4-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ff0e4-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="ff0e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0e4-103">A PsApiManagement-példány meglévő telepítési régiójának frissítése.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="ff0e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ff0e4-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff0e4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ff0e4-105">DESCRIPTION</span></span>
<span data-ttu-id="ff0e4-106">Az **Update-AzApiManagementRegion** parancsmag frissíti a **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** típus meglévő  példányát a **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="ff0e4-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="ff0e4-107">Ez a parancsmag nem telepít semmit, csak frissíti a **PsApiManagement** egy példányát a memóriában.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="ff0e4-108">Az API-kezelés telepítésének frissítéséhez használja a **módosított PsApiManagementInstance** Set-AzApiManagement parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="ff0e4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ff0e4-109">EXAMPLES</span></span>

### <span data-ttu-id="ff0e4-110">1. példa: A További régió kapacitásának növelése egy PsApiManagement-példányban</span><span class="sxs-lookup"><span data-stu-id="ff0e4-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="ff0e4-111">Ez a parancs az API Management Premium termékváltozat szolgáltatást kapja, amely az USA déli részén és észak-közép részén található régiókkal.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="ff0e4-112">Ezután az **Update-AzApiManagementRegion segítségével 2-re növeli az észak-közép-amerikai régió kapacitását.**</span><span class="sxs-lookup"><span data-stu-id="ff0e4-112">It then increases the Capacity of the North Central US region to 2 using the **Update-AzApiManagementRegion**.</span></span> <span data-ttu-id="ff0e4-113">A következő parancsmag Set-AzApiManagement a konfigurációs változást az Api Management szolgáltatásra.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-113">The next cmdlet Set-AzApiManagement applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="ff0e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff0e4-114">PARAMETERS</span></span>

### <span data-ttu-id="ff0e4-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff0e4-115">-ApiManagement</span></span>
<span data-ttu-id="ff0e4-116">Megadja a **PsApiManagement-példányt** egy meglévő telepítési régió frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="ff0e4-117">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="ff0e4-117">-Capacity</span></span>
<span data-ttu-id="ff0e4-118">A telepítési régió új termékváltozat-kapacitási értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-118">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff0e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0e4-119">-DefaultProfile</span></span>
<span data-ttu-id="ff0e4-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff0e4-121">-Location</span><span class="sxs-lookup"><span data-stu-id="ff0e4-121">-Location</span></span>
<span data-ttu-id="ff0e4-122">Megadja a frissíteni szükséges telepítési régió helyét.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="ff0e4-123">Megadja az új telepítési régió helyét az Api Management szolgáltatás támogatott régiója között.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="ff0e4-124">Érvényes helyek beszerzéséhez használja a Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | ahol {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="ff0e4-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff0e4-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="ff0e4-125">-Sku</span></span>
<span data-ttu-id="ff0e4-126">Az üzembe helyezési régió új rétegértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="ff0e4-127">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="ff0e4-127">Valid values are:</span></span>
- <span data-ttu-id="ff0e4-128">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="ff0e4-128">Developer</span></span>
- <span data-ttu-id="ff0e4-129">Normál</span><span class="sxs-lookup"><span data-stu-id="ff0e4-129">Standard</span></span>
- <span data-ttu-id="ff0e4-130">Prémium</span><span class="sxs-lookup"><span data-stu-id="ff0e4-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff0e4-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff0e4-131">-VirtualNetwork</span></span>
<span data-ttu-id="ff0e4-132">Virtuális hálózati konfigurációt ad meg az üzembe helyezési régióhoz.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="ff0e4-133">A $null eltávolítja a virtuális hálózat konfigurációját a régióhoz.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-133">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff0e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0e4-134">CommonParameters</span></span>
<span data-ttu-id="ff0e4-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0e4-136">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff0e4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0e4-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff0e4-137">INPUTS</span></span>

### <span data-ttu-id="ff0e4-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff0e4-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="ff0e4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ff0e4-139">System.String</span></span>

### <span data-ttu-id="ff0e4-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="ff0e4-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="ff0e4-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ff0e4-141">System.Int32</span></span>

### <span data-ttu-id="ff0e4-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff0e4-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="ff0e4-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff0e4-143">OUTPUTS</span></span>

### <span data-ttu-id="ff0e4-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff0e4-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ff0e4-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ff0e4-145">NOTES</span></span>

## <span data-ttu-id="ff0e4-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff0e4-146">RELATED LINKS</span></span>

[<span data-ttu-id="ff0e4-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ff0e4-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="ff0e4-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ff0e4-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="ff0e4-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff0e4-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
