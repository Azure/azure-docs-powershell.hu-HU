---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: f7a2952bf466a0d964a8b9075832635d2560b6fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505556"
---
# <span data-ttu-id="921b8-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="921b8-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="921b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="921b8-102">SYNOPSIS</span></span>
<span data-ttu-id="921b8-103">Új központi terjesztési régiók felvétele egy PsApiManagement-példányba.</span><span class="sxs-lookup"><span data-stu-id="921b8-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="921b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="921b8-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="921b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="921b8-105">DESCRIPTION</span></span>
<span data-ttu-id="921b8-106">Az **Add-AzureRmApiManagementRegion** parancsmag a **PsApiManagementRegion** új példányát adja a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagement** **AdditionalRegions** példányának.</span><span class="sxs-lookup"><span data-stu-id="921b8-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="921b8-107">Ez a parancsmag nem telepíti magát semmit, de a memória **PsApiManagement** példányát frissíti.</span><span class="sxs-lookup"><span data-stu-id="921b8-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="921b8-108">Az API-menedzsment telepített példányának frissítéséhez a módosított **PsApiManagement** -példányt a Update-AzureRmApiManagementDeployment-ra kell átadni.</span><span class="sxs-lookup"><span data-stu-id="921b8-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="921b8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="921b8-109">EXAMPLES</span></span>

### <span data-ttu-id="921b8-110">1. példa: új központi terjesztési régiók felvétele PsApiManagement-példányba</span><span class="sxs-lookup"><span data-stu-id="921b8-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="921b8-111">Ez a parancs két prémium SKU-egységet és a kelet-amerikai régiót a **PsApiManagement** -példányra helyezi.</span><span class="sxs-lookup"><span data-stu-id="921b8-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="921b8-112">2. példa: új üzembe állítási régiók felvétele PsApiManagement-példányba, majd a központi telepítő frissítése</span><span class="sxs-lookup"><span data-stu-id="921b8-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="921b8-113">Ez a parancs **PsApiManagement** objektumot kap, és két prémium SKU-egységet ad hozzá a kelet-amerikai régióhoz, majd frissíti a központi üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="921b8-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="921b8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="921b8-114">PARAMETERS</span></span>

### <span data-ttu-id="921b8-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="921b8-115">-ApiManagement</span></span>
<span data-ttu-id="921b8-116">Azt a **PsApiManagement** -példányt adja meg, amelyre a parancsmag további központi terjesztési területeket ad.</span><span class="sxs-lookup"><span data-stu-id="921b8-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="921b8-117">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="921b8-117">-Capacity</span></span>
<span data-ttu-id="921b8-118">A központi telepítő terület SKU-kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="921b8-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921b8-119">-DefaultProfile</span></span>
<span data-ttu-id="921b8-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="921b8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="921b8-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="921b8-121">-Location</span></span>
<span data-ttu-id="921b8-122">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="921b8-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>

<span data-ttu-id="921b8-123">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzureRmResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="921b8-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="921b8-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="921b8-124">-Sku</span></span>
<span data-ttu-id="921b8-125">A központi telepítő terület küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="921b8-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="921b8-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="921b8-126">Valid values are:</span></span> 

- <span data-ttu-id="921b8-127">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="921b8-127">Developer</span></span>
- <span data-ttu-id="921b8-128">Standard</span><span class="sxs-lookup"><span data-stu-id="921b8-128">Standard</span></span>
- <span data-ttu-id="921b8-129">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="921b8-129">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921b8-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="921b8-130">-VirtualNetwork</span></span>
<span data-ttu-id="921b8-131">Virtuális hálózati konfigurációt ad meg.</span><span class="sxs-lookup"><span data-stu-id="921b8-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921b8-132">CommonParameters</span></span>
<span data-ttu-id="921b8-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="921b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921b8-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="921b8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921b8-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="921b8-135">INPUTS</span></span>

### <span data-ttu-id="921b8-136">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="921b8-136">PsApiManagement</span></span>
<span data-ttu-id="921b8-137">A ' ApiManagement ' paraméter az "PsApiManagement" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="921b8-137">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="921b8-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="921b8-138">OUTPUTS</span></span>

### <span data-ttu-id="921b8-139">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="921b8-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="921b8-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="921b8-140">NOTES</span></span>
* <span data-ttu-id="921b8-141">A parancsmag frissített **PsApiManagement** -példányt ír a pipeline-ra.</span><span class="sxs-lookup"><span data-stu-id="921b8-141">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="921b8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="921b8-142">RELATED LINKS</span></span>

[<span data-ttu-id="921b8-143">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="921b8-143">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="921b8-144">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="921b8-144">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="921b8-145">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="921b8-145">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


