---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8d292f6e03661ae55a63686a0282ce65292087f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492917"
---
# <span data-ttu-id="7eaa6-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="7eaa6-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="7eaa6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7eaa6-102">SYNOPSIS</span></span>
<span data-ttu-id="7eaa6-103">Létrehozza a PsApiManagementRegion példányát.</span><span class="sxs-lookup"><span data-stu-id="7eaa6-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eaa6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7eaa6-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eaa6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7eaa6-105">DESCRIPTION</span></span>
<span data-ttu-id="7eaa6-106">A segítő parancs a PsApiManagementRegion példányának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7eaa6-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="7eaa6-107">Ezt a parancsot New-AzureRmApiManagement paranccsal kell használni.</span><span class="sxs-lookup"><span data-stu-id="7eaa6-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="7eaa6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7eaa6-108">EXAMPLES</span></span>

### <span data-ttu-id="7eaa6-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7eaa6-109">Example 1</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="7eaa6-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="7eaa6-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="7eaa6-111">A West US region külső VpnType ApiManagement szolgáltatását hozza létre egy további Közép-amerikai régióval.</span><span class="sxs-lookup"><span data-stu-id="7eaa6-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="7eaa6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7eaa6-112">PARAMETERS</span></span>

### <span data-ttu-id="7eaa6-113">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="7eaa6-113">-Capacity</span></span>
<span data-ttu-id="7eaa6-114">Az Azure API-kezelési szolgáltatás további régiójának SKU-kapacitása.</span><span class="sxs-lookup"><span data-stu-id="7eaa6-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="7eaa6-115">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="7eaa6-115">Default value is 1.</span></span>

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

### <span data-ttu-id="7eaa6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eaa6-116">-DefaultProfile</span></span>
<span data-ttu-id="7eaa6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7eaa6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eaa6-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="7eaa6-118">-Location</span></span>
<span data-ttu-id="7eaa6-119">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="7eaa6-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="7eaa6-120">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzureRmResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="7eaa6-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="7eaa6-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7eaa6-121">-VirtualNetwork</span></span>
<span data-ttu-id="7eaa6-122">A virtuális hálózat konfigurációja az Azure API felügyeleti közterjesztési területről</span><span class="sxs-lookup"><span data-stu-id="7eaa6-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="7eaa6-123">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="7eaa6-123">Default value is $null.</span></span>

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

### <span data-ttu-id="7eaa6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eaa6-124">CommonParameters</span></span>
<span data-ttu-id="7eaa6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7eaa6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eaa6-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eaa6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eaa6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eaa6-127">INPUTS</span></span>

### <span data-ttu-id="7eaa6-128">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7eaa6-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="7eaa6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eaa6-129">OUTPUTS</span></span>

### <span data-ttu-id="7eaa6-130">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="7eaa6-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="7eaa6-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7eaa6-131">NOTES</span></span>

## <span data-ttu-id="7eaa6-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7eaa6-132">RELATED LINKS</span></span>
