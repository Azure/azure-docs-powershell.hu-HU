---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 8552592acb45702c866c8d918121b8dd61d126a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183740"
---
# <span data-ttu-id="530e2-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="530e2-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="530e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="530e2-102">SYNOPSIS</span></span>
<span data-ttu-id="530e2-103">Frissíti a meglévő központi terjesztési területet a PsApiManagement-példányban.</span><span class="sxs-lookup"><span data-stu-id="530e2-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="530e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="530e2-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="530e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="530e2-105">DESCRIPTION</span></span>
<span data-ttu-id="530e2-106">Az **Update-AzApiManagementRegion** parancsmag a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion** egy meglévő példányát frissíti a Microsoft. **Azure. commands**. ApiManagement. modellek. PsApiManagement **AdditionalRegions** -példányban.</span><span class="sxs-lookup"><span data-stu-id="530e2-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="530e2-107">Ez a parancsmag nem telepít semmit, de frissíti a **PsApiManagement** -példányokat a memóriában.</span><span class="sxs-lookup"><span data-stu-id="530e2-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="530e2-108">Ha frissíteni szeretné az API-kezelés telepített példányát, használja a módosított **PsApiManagementInstance** az Set-AzApiManagement parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="530e2-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="530e2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="530e2-109">EXAMPLES</span></span>

### <span data-ttu-id="530e2-110">1. példa: növeli a további régiók kapacitását egy PsApiManagement-példányban</span><span class="sxs-lookup"><span data-stu-id="530e2-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="530e2-111">Ez a parancs beilleszti az API-menedzsment Premium SKU szolgáltatást, amely a dél-közép-amerikai és Észak-Közép-amerikai régiókat használja.</span><span class="sxs-lookup"><span data-stu-id="530e2-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="530e2-112">Ezután az észak-közép-amerikai régió 2 kapacitását növeli a **set-AzApiManagement** segítségével.</span><span class="sxs-lookup"><span data-stu-id="530e2-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="530e2-113">A következő parancsmag **beállítása – a AzApiManagement** az API-kezelési szolgáltatásra alkalmazza a konfigurációs módosítást.</span><span class="sxs-lookup"><span data-stu-id="530e2-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

### <span data-ttu-id="530e2-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="530e2-114">Example 2</span></span>

<span data-ttu-id="530e2-115">Frissíti a meglévő központi terjesztési területet a PsApiManagement-példányban.</span><span class="sxs-lookup"><span data-stu-id="530e2-115">Updates existing deployment region in PsApiManagement instance.</span></span> <span data-ttu-id="530e2-116">autogenerated</span><span class="sxs-lookup"><span data-stu-id="530e2-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## <span data-ttu-id="530e2-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="530e2-117">PARAMETERS</span></span>

### <span data-ttu-id="530e2-118">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="530e2-118">-ApiManagement</span></span>
<span data-ttu-id="530e2-119">Annak a **PsApiManagement** a példányát adja meg, amely a meglévő központi terjesztési terület frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="530e2-119">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="530e2-120">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="530e2-120">-Capacity</span></span>
<span data-ttu-id="530e2-121">Az új SKU-kapacitás értékét adja meg a központi telepítő régióban.</span><span class="sxs-lookup"><span data-stu-id="530e2-121">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="530e2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="530e2-122">-DefaultProfile</span></span>
<span data-ttu-id="530e2-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="530e2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="530e2-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="530e2-124">-Location</span></span>
<span data-ttu-id="530e2-125">A frissítendő központi terjesztési terület helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="530e2-125">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="530e2-126">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="530e2-126">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="530e2-127">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="530e2-127">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="530e2-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="530e2-128">-Sku</span></span>
<span data-ttu-id="530e2-129">A központi telepítő terület új Tier értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="530e2-129">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="530e2-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="530e2-130">Valid values are:</span></span>
- <span data-ttu-id="530e2-131">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="530e2-131">Developer</span></span>
- <span data-ttu-id="530e2-132">Standard</span><span class="sxs-lookup"><span data-stu-id="530e2-132">Standard</span></span>
- <span data-ttu-id="530e2-133">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="530e2-133">Premium</span></span>

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

### <span data-ttu-id="530e2-134">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="530e2-134">-VirtualNetwork</span></span>
<span data-ttu-id="530e2-135">A központi telepítő terület virtuális hálózati konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="530e2-135">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="530e2-136">Az átadás $null eltávolítja a tartomány virtuális hálózati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="530e2-136">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="530e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="530e2-137">CommonParameters</span></span>
<span data-ttu-id="530e2-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="530e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="530e2-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="530e2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="530e2-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="530e2-140">INPUTS</span></span>

### <span data-ttu-id="530e2-141">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="530e2-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="530e2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="530e2-142">System.String</span></span>

### <span data-ttu-id="530e2-143">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="530e2-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="530e2-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="530e2-144">System.Int32</span></span>

### <span data-ttu-id="530e2-145">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="530e2-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="530e2-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="530e2-146">OUTPUTS</span></span>

### <span data-ttu-id="530e2-147">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="530e2-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="530e2-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="530e2-148">NOTES</span></span>

## <span data-ttu-id="530e2-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="530e2-149">RELATED LINKS</span></span>

[<span data-ttu-id="530e2-150">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="530e2-150">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="530e2-151">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="530e2-151">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="530e2-152">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="530e2-152">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
