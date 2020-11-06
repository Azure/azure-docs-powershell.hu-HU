---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503320"
---
# <span data-ttu-id="9fa80-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9fa80-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="9fa80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fa80-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa80-103">Új központi terjesztési régiók felvétele egy PsApiManagement-példányba.</span><span class="sxs-lookup"><span data-stu-id="9fa80-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fa80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fa80-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fa80-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fa80-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa80-106">Az **Add-AzureRmApiManagementRegion** parancsmag a **PsApiManagementRegion** új példányát adja a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagement** **AdditionalRegions** példányának.</span><span class="sxs-lookup"><span data-stu-id="9fa80-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="9fa80-107">Ez a parancsmag nem telepíti magát semmit, de a memória **PsApiManagement** példányát frissíti.</span><span class="sxs-lookup"><span data-stu-id="9fa80-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="9fa80-108">Az API-menedzsment telepített példányának frissítéséhez a módosított **PsApiManagement** -példányt a Update-AzureRmApiManagementDeployment-ra kell átadni.</span><span class="sxs-lookup"><span data-stu-id="9fa80-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="9fa80-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9fa80-109">EXAMPLES</span></span>

### <span data-ttu-id="9fa80-110">1. példa: új központi terjesztési régiók felvétele PsApiManagement-példányba</span><span class="sxs-lookup"><span data-stu-id="9fa80-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="9fa80-111">Ez a parancs két prémium SKU-egységet és a kelet-amerikai régiót a **PsApiManagement** -példányra helyezi.</span><span class="sxs-lookup"><span data-stu-id="9fa80-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="9fa80-112">2. példa: új üzembe állítási régiók felvétele PsApiManagement-példányba, majd a központi telepítő frissítése</span><span class="sxs-lookup"><span data-stu-id="9fa80-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="9fa80-113">Ez a parancs **PsApiManagement** objektumot kap, és két prémium SKU-egységet ad hozzá a kelet-amerikai régióhoz, majd frissíti a központi üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="9fa80-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="9fa80-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fa80-114">PARAMETERS</span></span>

### <span data-ttu-id="9fa80-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fa80-115">-ApiManagement</span></span>
<span data-ttu-id="9fa80-116">Azt a **PsApiManagement** -példányt adja meg, amelyre a parancsmag további központi terjesztési területeket ad.</span><span class="sxs-lookup"><span data-stu-id="9fa80-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="9fa80-117">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="9fa80-117">-Capacity</span></span>
<span data-ttu-id="9fa80-118">A központi telepítő terület SKU-kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fa80-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="9fa80-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="9fa80-119">-Location</span></span>
<span data-ttu-id="9fa80-120">Az új központi terjesztési terület helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fa80-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="9fa80-121">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="9fa80-121">Valid values are:</span></span> 

- <span data-ttu-id="9fa80-122">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="9fa80-122">North Central US</span></span>
- <span data-ttu-id="9fa80-123">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="9fa80-123">South Central US</span></span>
- <span data-ttu-id="9fa80-124">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="9fa80-124">Central US</span></span>
- <span data-ttu-id="9fa80-125">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="9fa80-125">West Europe</span></span>
- <span data-ttu-id="9fa80-126">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="9fa80-126">North Europe</span></span>
- <span data-ttu-id="9fa80-127">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="9fa80-127">West US</span></span>
- <span data-ttu-id="9fa80-128">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="9fa80-128">East US</span></span>
- <span data-ttu-id="9fa80-129">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="9fa80-129">East US 2</span></span>
- <span data-ttu-id="9fa80-130">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="9fa80-130">Japan East</span></span>
- <span data-ttu-id="9fa80-131">Japán West</span><span class="sxs-lookup"><span data-stu-id="9fa80-131">Japan West</span></span>
- <span data-ttu-id="9fa80-132">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="9fa80-132">Brazil South</span></span>
- <span data-ttu-id="9fa80-133">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="9fa80-133">Southeast Asia</span></span>
- <span data-ttu-id="9fa80-134">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="9fa80-134">East Asia</span></span>
- <span data-ttu-id="9fa80-135">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="9fa80-135">Australia East</span></span>
- <span data-ttu-id="9fa80-136">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="9fa80-136">Australia Southeast</span></span>

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

### <span data-ttu-id="9fa80-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="9fa80-137">-Sku</span></span>
<span data-ttu-id="9fa80-138">A központi telepítő terület küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fa80-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="9fa80-139">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="9fa80-139">Valid values are:</span></span> 

- <span data-ttu-id="9fa80-140">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="9fa80-140">Developer</span></span>
- <span data-ttu-id="9fa80-141">Standard</span><span class="sxs-lookup"><span data-stu-id="9fa80-141">Standard</span></span>
- <span data-ttu-id="9fa80-142">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="9fa80-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa80-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fa80-143">-VirtualNetwork</span></span>
<span data-ttu-id="9fa80-144">Virtuális hálózati konfigurációt ad meg.</span><span class="sxs-lookup"><span data-stu-id="9fa80-144">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="9fa80-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa80-145">-DefaultProfile</span></span>
<span data-ttu-id="9fa80-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fa80-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fa80-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa80-147">CommonParameters</span></span>
<span data-ttu-id="9fa80-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fa80-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa80-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa80-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa80-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fa80-150">INPUTS</span></span>

### <span data-ttu-id="9fa80-151">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fa80-151">PsApiManagement</span></span>
<span data-ttu-id="9fa80-152">A ' ApiManagement ' paraméter az "PsApiManagement" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9fa80-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="9fa80-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fa80-153">OUTPUTS</span></span>

### <span data-ttu-id="9fa80-154">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fa80-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9fa80-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fa80-155">NOTES</span></span>
* <span data-ttu-id="9fa80-156">A parancsmag frissített **PsApiManagement** -példányt ír a pipeline-ra.</span><span class="sxs-lookup"><span data-stu-id="9fa80-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="9fa80-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fa80-157">RELATED LINKS</span></span>

[<span data-ttu-id="9fa80-158">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9fa80-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9fa80-159">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9fa80-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9fa80-160">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="9fa80-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


