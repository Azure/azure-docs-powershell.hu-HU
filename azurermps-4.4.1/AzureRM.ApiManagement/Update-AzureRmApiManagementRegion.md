---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492585"
---
# <span data-ttu-id="285d9-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="285d9-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="285d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="285d9-102">SYNOPSIS</span></span>
<span data-ttu-id="285d9-103">Frissíti a meglévő központi terjesztési területet a PsApiManagement-példányban.</span><span class="sxs-lookup"><span data-stu-id="285d9-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="285d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="285d9-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="285d9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="285d9-105">DESCRIPTION</span></span>
<span data-ttu-id="285d9-106">Az **Update-AzureRmApiManagementRegion** parancsmag a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion** egy meglévő példányát frissíti a Microsoft. **Azure. commands**. ApiManagement. modellek. PsApiManagement **AdditionalRegions** -példányban.</span><span class="sxs-lookup"><span data-stu-id="285d9-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="285d9-107">Ez a parancsmag nem telepít semmit, de frissíti a **PsApiManagement** -példányokat a memóriában.</span><span class="sxs-lookup"><span data-stu-id="285d9-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="285d9-108">Ha frissíteni szeretné az API-kezelés telepített példányát, használja a módosított **PsApiManagementInstance** az Update-AzureRmApiManagementDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="285d9-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="285d9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="285d9-109">EXAMPLES</span></span>

## <span data-ttu-id="285d9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="285d9-110">PARAMETERS</span></span>

### <span data-ttu-id="285d9-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="285d9-111">-ApiManagement</span></span>
<span data-ttu-id="285d9-112">Annak a **PsApiManagement** a példányát adja meg, amely a meglévő központi terjesztési terület frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="285d9-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="285d9-113">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="285d9-113">-Capacity</span></span>
<span data-ttu-id="285d9-114">Az új SKU-kapacitás értékét adja meg a központi telepítő régióban.</span><span class="sxs-lookup"><span data-stu-id="285d9-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="285d9-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="285d9-115">-Location</span></span>
<span data-ttu-id="285d9-116">A frissítendő központi terjesztési terület helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="285d9-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="285d9-117">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="285d9-117">Valid values are:</span></span>

- <span data-ttu-id="285d9-118">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="285d9-118">North Central US</span></span>
- <span data-ttu-id="285d9-119">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="285d9-119">South Central US</span></span>
- <span data-ttu-id="285d9-120">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="285d9-120">Central US</span></span>
- <span data-ttu-id="285d9-121">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="285d9-121">West Europe</span></span>
- <span data-ttu-id="285d9-122">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="285d9-122">North Europe</span></span>
- <span data-ttu-id="285d9-123">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="285d9-123">West US</span></span>
- <span data-ttu-id="285d9-124">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="285d9-124">East US</span></span>
- <span data-ttu-id="285d9-125">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="285d9-125">East US 2</span></span>
- <span data-ttu-id="285d9-126">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="285d9-126">Japan East</span></span>
- <span data-ttu-id="285d9-127">Japán West</span><span class="sxs-lookup"><span data-stu-id="285d9-127">Japan West</span></span>
- <span data-ttu-id="285d9-128">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="285d9-128">Brazil South</span></span>
- <span data-ttu-id="285d9-129">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="285d9-129">Southeast Asia</span></span>
- <span data-ttu-id="285d9-130">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="285d9-130">East Asia</span></span>
- <span data-ttu-id="285d9-131">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="285d9-131">Australia East</span></span>
- <span data-ttu-id="285d9-132">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="285d9-132">Australia Southeast</span></span>

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

### <span data-ttu-id="285d9-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="285d9-133">-Sku</span></span>
<span data-ttu-id="285d9-134">A központi telepítő terület új Tier értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="285d9-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="285d9-135">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="285d9-135">Valid values are:</span></span>

- <span data-ttu-id="285d9-136">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="285d9-136">Developer</span></span>
- <span data-ttu-id="285d9-137">Standard</span><span class="sxs-lookup"><span data-stu-id="285d9-137">Standard</span></span>
- <span data-ttu-id="285d9-138">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="285d9-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285d9-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="285d9-139">-VirtualNetwork</span></span>
<span data-ttu-id="285d9-140">A központi telepítő terület virtuális hálózati konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="285d9-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="285d9-141">Az átadás $null eltávolítja a tartomány virtuális hálózati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="285d9-141">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="285d9-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285d9-142">-DefaultProfile</span></span>
<span data-ttu-id="285d9-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="285d9-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="285d9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285d9-144">CommonParameters</span></span>
<span data-ttu-id="285d9-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="285d9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285d9-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285d9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285d9-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="285d9-147">INPUTS</span></span>

### <span data-ttu-id="285d9-148">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="285d9-148">PsApiManagement</span></span>
<span data-ttu-id="285d9-149">A ' ApiManagement ' paraméter az "PsApiManagement" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="285d9-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="285d9-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="285d9-150">OUTPUTS</span></span>

### <span data-ttu-id="285d9-151">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="285d9-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="285d9-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="285d9-152">NOTES</span></span>

## <span data-ttu-id="285d9-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="285d9-153">RELATED LINKS</span></span>

[<span data-ttu-id="285d9-154">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="285d9-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="285d9-155">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="285d9-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="285d9-156">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="285d9-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
