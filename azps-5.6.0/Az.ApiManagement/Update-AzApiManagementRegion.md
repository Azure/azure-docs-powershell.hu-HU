---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: c2e01d4a3f6ee3466151202a1c1d681c9f4e5486
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001910"
---
# <span data-ttu-id="3bbb6-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3bbb6-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="3bbb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bbb6-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbb6-103">A PsApiManagement-példány meglévő telepítési régiójának frissítése.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="3bbb6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3bbb6-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bbb6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3bbb6-105">DESCRIPTION</span></span>
<span data-ttu-id="3bbb6-106">Az **Update-AzApiManagementRegion** parancsmag egy **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** típusú meglévő példányt frissít Egy **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement** típusú megadott példány **AdditionalRegions** objektumgyűjteményében.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="3bbb6-107">Ez a parancsmag nem telepít semmit, csak frissíti a **PsApiManagement** egy példányát a memóriában.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="3bbb6-108">Az API-kezelés telepítésének frissítéséhez használja a **módosított PsApiManagementInstance** Set-AzApiManagement parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="3bbb6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3bbb6-109">EXAMPLES</span></span>

### <span data-ttu-id="3bbb6-110">1. példa: A További régió kapacitásának növelése egy PsApiManagement-példányban</span><span class="sxs-lookup"><span data-stu-id="3bbb6-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="3bbb6-111">Ez a parancs az API Management Premium termékváltozat szolgáltatást kapja, amely az Usa déli részén és észak-közép amerikai régióiban található.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="3bbb6-112">Ezután a **Set-AzApiManagement használatával 2-re növeli az észak-közép-amerikai régió kapacitását.**</span><span class="sxs-lookup"><span data-stu-id="3bbb6-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="3bbb6-113">A következő **Set-AzApiManagement parancsmag** a konfigurációs változást alkalmazza az Api Management szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

### <span data-ttu-id="3bbb6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3bbb6-114">Example 2</span></span>

<span data-ttu-id="3bbb6-115">A PsApiManagement-példány meglévő telepítési régiójának frissítése.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-115">Updates existing deployment region in PsApiManagement instance.</span></span> <span data-ttu-id="3bbb6-116">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="3bbb6-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## <span data-ttu-id="3bbb6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bbb6-117">PARAMETERS</span></span>

### <span data-ttu-id="3bbb6-118">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3bbb6-118">-ApiManagement</span></span>
<span data-ttu-id="3bbb6-119">Megadja a **PsApiManagement-példányt** egy meglévő telepítési régió frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-119">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="3bbb6-120">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="3bbb6-120">-Capacity</span></span>
<span data-ttu-id="3bbb6-121">A telepítési régió új termékváltozat-kapacitási értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-121">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="3bbb6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbb6-122">-DefaultProfile</span></span>
<span data-ttu-id="3bbb6-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bbb6-124">-Location</span><span class="sxs-lookup"><span data-stu-id="3bbb6-124">-Location</span></span>
<span data-ttu-id="3bbb6-125">Megadja a frissíteni szükséges telepítési régió helyét.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-125">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="3bbb6-126">Megadja az új telepítési régió helyét az Api Management szolgáltatás támogatott régiója között.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-126">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="3bbb6-127">Érvényes helyek beszerzéséhez használja a Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | ahol {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="3bbb6-127">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="3bbb6-128">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="3bbb6-128">-Sku</span></span>
<span data-ttu-id="3bbb6-129">Az üzembe helyezési régió új rétegértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-129">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="3bbb6-130">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="3bbb6-130">Valid values are:</span></span>
- <span data-ttu-id="3bbb6-131">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="3bbb6-131">Developer</span></span>
- <span data-ttu-id="3bbb6-132">Normál</span><span class="sxs-lookup"><span data-stu-id="3bbb6-132">Standard</span></span>
- <span data-ttu-id="3bbb6-133">Prémium</span><span class="sxs-lookup"><span data-stu-id="3bbb6-133">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbb6-134">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3bbb6-134">-VirtualNetwork</span></span>
<span data-ttu-id="3bbb6-135">Virtuális hálózati konfigurációt ad meg az üzembe helyezési régióhoz.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-135">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="3bbb6-136">A $null eltávolítja a virtuális hálózat konfigurációját a régióhoz.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-136">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="3bbb6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbb6-137">CommonParameters</span></span>
<span data-ttu-id="3bbb6-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bbb6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbb6-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bbb6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbb6-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bbb6-140">INPUTS</span></span>

### <span data-ttu-id="3bbb6-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3bbb6-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="3bbb6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3bbb6-142">System.String</span></span>

### <span data-ttu-id="3bbb6-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="3bbb6-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="3bbb6-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3bbb6-144">System.Int32</span></span>

### <span data-ttu-id="3bbb6-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3bbb6-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="3bbb6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bbb6-146">OUTPUTS</span></span>

### <span data-ttu-id="3bbb6-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3bbb6-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3bbb6-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3bbb6-148">NOTES</span></span>

## <span data-ttu-id="3bbb6-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bbb6-149">RELATED LINKS</span></span>

[<span data-ttu-id="3bbb6-150">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3bbb6-150">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="3bbb6-151">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3bbb6-151">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="3bbb6-152">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3bbb6-152">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
