---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187095"
---
# <span data-ttu-id="45b30-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="45b30-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="45b30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45b30-102">SYNOPSIS</span></span>
<span data-ttu-id="45b30-103">Létrehozza a PsApiManagementRegion példányát.</span><span class="sxs-lookup"><span data-stu-id="45b30-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="45b30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45b30-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45b30-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45b30-105">DESCRIPTION</span></span>
<span data-ttu-id="45b30-106">A segítő parancs a PsApiManagementRegion példányának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="45b30-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="45b30-107">Ezt a parancsot New-AzApiManagement paranccsal kell használni.</span><span class="sxs-lookup"><span data-stu-id="45b30-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="45b30-108">Példák</span><span class="sxs-lookup"><span data-stu-id="45b30-108">EXAMPLES</span></span>

### <span data-ttu-id="45b30-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45b30-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="45b30-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="45b30-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="45b30-111">A West US region külső VpnType ApiManagement szolgáltatását hozza létre egy további Közép-amerikai régióval.</span><span class="sxs-lookup"><span data-stu-id="45b30-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="45b30-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45b30-112">PARAMETERS</span></span>

### <span data-ttu-id="45b30-113">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="45b30-113">-Capacity</span></span>
<span data-ttu-id="45b30-114">Az Azure API-kezelési szolgáltatás további régiójának SKU-kapacitása.</span><span class="sxs-lookup"><span data-stu-id="45b30-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="45b30-115">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="45b30-115">Default value is 1.</span></span>

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

### <span data-ttu-id="45b30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b30-116">-DefaultProfile</span></span>
<span data-ttu-id="45b30-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45b30-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b30-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="45b30-118">-Location</span></span>
<span data-ttu-id="45b30-119">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="45b30-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="45b30-120">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="45b30-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="45b30-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="45b30-121">-VirtualNetwork</span></span>
<span data-ttu-id="45b30-122">A virtuális hálózat konfigurációja az Azure API felügyeleti közterjesztési területről</span><span class="sxs-lookup"><span data-stu-id="45b30-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="45b30-123">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="45b30-123">Default value is $null.</span></span>

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

### <span data-ttu-id="45b30-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b30-124">CommonParameters</span></span>
<span data-ttu-id="45b30-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45b30-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b30-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45b30-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b30-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45b30-127">INPUTS</span></span>

### <span data-ttu-id="45b30-128">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="45b30-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="45b30-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45b30-129">OUTPUTS</span></span>

### <span data-ttu-id="45b30-130">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="45b30-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="45b30-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45b30-131">NOTES</span></span>

## <span data-ttu-id="45b30-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45b30-132">RELATED LINKS</span></span>