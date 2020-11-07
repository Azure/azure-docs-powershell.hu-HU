---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: fce2d356b7da56d2b93fa8634e737f96f54da178
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836892"
---
# <span data-ttu-id="0b687-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0b687-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="0b687-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b687-102">SYNOPSIS</span></span>
<span data-ttu-id="0b687-103">Frissíti a meglévő központi terjesztési területet a PsApiManagement-példányban.</span><span class="sxs-lookup"><span data-stu-id="0b687-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="0b687-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b687-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b687-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b687-105">DESCRIPTION</span></span>
<span data-ttu-id="0b687-106">Az **Update-AzApiManagementRegion** parancsmag a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion** egy meglévő példányát frissíti a Microsoft. **Azure. commands**. ApiManagement. modellek. PsApiManagement **AdditionalRegions** -példányban.</span><span class="sxs-lookup"><span data-stu-id="0b687-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="0b687-107">Ez a parancsmag nem telepít semmit, de frissíti a **PsApiManagement** -példányokat a memóriában.</span><span class="sxs-lookup"><span data-stu-id="0b687-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="0b687-108">Ha frissíteni szeretné az API-kezelés telepített példányát, használja a módosított **PsApiManagementInstance** az Update-AzApiManagementDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0b687-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="0b687-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0b687-109">EXAMPLES</span></span>

### <span data-ttu-id="0b687-110">1. példa: növeli a további régiók kapacitását egy PsApiManagement-példányban</span><span class="sxs-lookup"><span data-stu-id="0b687-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="0b687-111">Ez a parancs beilleszti az API-menedzsment Premium SKU szolgáltatást, amely a dél-közép-amerikai és Észak-Közép-amerikai régiókat használja.</span><span class="sxs-lookup"><span data-stu-id="0b687-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="0b687-112">Ezt követően növeli az észak-közép-amerikai régió kapacitását az **Update-AzApiManagementRegion** segítségével.</span><span class="sxs-lookup"><span data-stu-id="0b687-112">It then increases the Capacity of the North Central US region to 2 using the **Update-AzApiManagementRegion**.</span></span> <span data-ttu-id="0b687-113">A következő parancsmag Set-AzApiManagement alkalmazza a konfigurációs módosítást az API-kezelési szolgáltatásra.</span><span class="sxs-lookup"><span data-stu-id="0b687-113">The next cmdlet Set-AzApiManagement applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="0b687-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b687-114">PARAMETERS</span></span>

### <span data-ttu-id="0b687-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b687-115">-ApiManagement</span></span>
<span data-ttu-id="0b687-116">Annak a **PsApiManagement** a példányát adja meg, amely a meglévő központi terjesztési terület frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="0b687-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="0b687-117">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="0b687-117">-Capacity</span></span>
<span data-ttu-id="0b687-118">Az új SKU-kapacitás értékét adja meg a központi telepítő régióban.</span><span class="sxs-lookup"><span data-stu-id="0b687-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="0b687-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b687-119">-DefaultProfile</span></span>
<span data-ttu-id="0b687-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b687-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b687-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="0b687-121">-Location</span></span>
<span data-ttu-id="0b687-122">A frissítendő központi terjesztési terület helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b687-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="0b687-123">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="0b687-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="0b687-124">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="0b687-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="0b687-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="0b687-125">-Sku</span></span>
<span data-ttu-id="0b687-126">A központi telepítő terület új Tier értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b687-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="0b687-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="0b687-127">Valid values are:</span></span>
- <span data-ttu-id="0b687-128">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="0b687-128">Developer</span></span>
- <span data-ttu-id="0b687-129">Standard</span><span class="sxs-lookup"><span data-stu-id="0b687-129">Standard</span></span>
- <span data-ttu-id="0b687-130">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="0b687-130">Premium</span></span>

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

### <span data-ttu-id="0b687-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0b687-131">-VirtualNetwork</span></span>
<span data-ttu-id="0b687-132">A központi telepítő terület virtuális hálózati konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b687-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="0b687-133">Az átadás $null eltávolítja a tartomány virtuális hálózati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0b687-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="0b687-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b687-134">CommonParameters</span></span>
<span data-ttu-id="0b687-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b687-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b687-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b687-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b687-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b687-137">INPUTS</span></span>

### <span data-ttu-id="0b687-138">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b687-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="0b687-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0b687-139">System.String</span></span>

### <span data-ttu-id="0b687-140">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="0b687-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="0b687-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0b687-141">System.Int32</span></span>

### <span data-ttu-id="0b687-142">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0b687-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="0b687-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b687-143">OUTPUTS</span></span>

### <span data-ttu-id="0b687-144">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b687-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0b687-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b687-145">NOTES</span></span>

## <span data-ttu-id="0b687-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b687-146">RELATED LINKS</span></span>

[<span data-ttu-id="0b687-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0b687-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="0b687-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0b687-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="0b687-149">Update-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="0b687-149">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)
