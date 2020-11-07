---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: d6c97ac0fc948ba3ee4f86a2e657a1386c693f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679751"
---
# <span data-ttu-id="cf78c-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="cf78c-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="cf78c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf78c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf78c-103">Frissíti a meglévő központi terjesztési területet a PsApiManagement-példányban.</span><span class="sxs-lookup"><span data-stu-id="cf78c-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf78c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf78c-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf78c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf78c-105">DESCRIPTION</span></span>
<span data-ttu-id="cf78c-106">Az **Update-AzureRmApiManagementRegion** parancsmag a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion** egy meglévő példányát frissíti a Microsoft. **Azure. commands**. ApiManagement. modellek. PsApiManagement **AdditionalRegions** -példányban.</span><span class="sxs-lookup"><span data-stu-id="cf78c-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="cf78c-107">Ez a parancsmag nem telepít semmit, de frissíti a **PsApiManagement** -példányokat a memóriában.</span><span class="sxs-lookup"><span data-stu-id="cf78c-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="cf78c-108">Ha frissíteni szeretné az API-kezelés telepített példányát, használja a módosított **PsApiManagementInstance** az Update-AzureRmApiManagementDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cf78c-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="cf78c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cf78c-109">EXAMPLES</span></span>

## <span data-ttu-id="cf78c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf78c-110">PARAMETERS</span></span>

### <span data-ttu-id="cf78c-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cf78c-111">-ApiManagement</span></span>
<span data-ttu-id="cf78c-112">Annak a **PsApiManagement** a példányát adja meg, amely a meglévő központi terjesztési terület frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="cf78c-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="cf78c-113">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="cf78c-113">-Capacity</span></span>
<span data-ttu-id="cf78c-114">Az új SKU-kapacitás értékét adja meg a központi telepítő régióban.</span><span class="sxs-lookup"><span data-stu-id="cf78c-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf78c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf78c-115">-DefaultProfile</span></span>
<span data-ttu-id="cf78c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf78c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="cf78c-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="cf78c-117">-Location</span></span>
<span data-ttu-id="cf78c-118">A frissítendő központi terjesztési terület helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf78c-118">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="cf78c-119">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="cf78c-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="cf78c-120">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzureRmResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="cf78c-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf78c-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="cf78c-121">-Sku</span></span>
<span data-ttu-id="cf78c-122">A központi telepítő terület új Tier értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf78c-122">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="cf78c-123">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="cf78c-123">Valid values are:</span></span>

- <span data-ttu-id="cf78c-124">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="cf78c-124">Developer</span></span>
- <span data-ttu-id="cf78c-125">Standard</span><span class="sxs-lookup"><span data-stu-id="cf78c-125">Standard</span></span>
- <span data-ttu-id="cf78c-126">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="cf78c-126">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf78c-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf78c-127">-VirtualNetwork</span></span>
<span data-ttu-id="cf78c-128">A központi telepítő terület virtuális hálózati konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf78c-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="cf78c-129">Az átadás $null eltávolítja a tartomány virtuális hálózati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="cf78c-129">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf78c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf78c-130">CommonParameters</span></span>
<span data-ttu-id="cf78c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf78c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf78c-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf78c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf78c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf78c-133">INPUTS</span></span>

### <span data-ttu-id="cf78c-134">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="cf78c-134">PsApiManagement</span></span>
<span data-ttu-id="cf78c-135">A ' ApiManagement ' paraméter az "PsApiManagement" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cf78c-135">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="cf78c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf78c-136">OUTPUTS</span></span>

### <span data-ttu-id="cf78c-137">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="cf78c-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="cf78c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf78c-138">NOTES</span></span>

## <span data-ttu-id="cf78c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf78c-139">RELATED LINKS</span></span>

[<span data-ttu-id="cf78c-140">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="cf78c-140">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="cf78c-141">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="cf78c-141">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="cf78c-142">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="cf78c-142">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
