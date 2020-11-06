---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: abfcbec55ba3f53986a63a8c0964320c10fc91ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501247"
---
# <span data-ttu-id="48251-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48251-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="48251-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48251-102">SYNOPSIS</span></span>
<span data-ttu-id="48251-103">Létrehozza a PsApiManagementVirtualNetwork példányát.</span><span class="sxs-lookup"><span data-stu-id="48251-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48251-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48251-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48251-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48251-105">DESCRIPTION</span></span>
<span data-ttu-id="48251-106">A **New-AzureRmApiManagementVirtualNetwork** parancsmag a **PsApiManagementVirtualNetwork** példányának létrehozására szolgáló segítő parancs.</span><span class="sxs-lookup"><span data-stu-id="48251-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="48251-107">Ez a parancs a **Update-AzureRmApiManagementDeployment** parancsmagtal használható.</span><span class="sxs-lookup"><span data-stu-id="48251-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="48251-108">Példák</span><span class="sxs-lookup"><span data-stu-id="48251-108">EXAMPLES</span></span>

### <span data-ttu-id="48251-109">Példa 1: virtuális hálózat létrehozása</span><span class="sxs-lookup"><span data-stu-id="48251-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="48251-110">Ez a példa virtuális hálózatot hoz létre, majd felhívja az **Update-AzureRmApiManagementDeployment** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="48251-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="48251-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48251-111">PARAMETERS</span></span>

### <span data-ttu-id="48251-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48251-112">-DefaultProfile</span></span>
<span data-ttu-id="48251-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48251-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48251-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="48251-114">-Location</span></span>
<span data-ttu-id="48251-115">Az API-kezelési szolgáltatás támogatott területe közötti helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="48251-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="48251-116">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzureRmResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="48251-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="48251-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="48251-117">-SubnetResourceId</span></span>
<span data-ttu-id="48251-118">A virtuális hálózat alhálózati erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="48251-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="48251-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48251-119">CommonParameters</span></span>
<span data-ttu-id="48251-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48251-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48251-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48251-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48251-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48251-122">INPUTS</span></span>

### <span data-ttu-id="48251-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="48251-123">None</span></span>

## <span data-ttu-id="48251-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48251-124">OUTPUTS</span></span>

### <span data-ttu-id="48251-125">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48251-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="48251-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48251-126">NOTES</span></span>

## <span data-ttu-id="48251-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48251-127">RELATED LINKS</span></span>

[<span data-ttu-id="48251-128">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="48251-128">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

