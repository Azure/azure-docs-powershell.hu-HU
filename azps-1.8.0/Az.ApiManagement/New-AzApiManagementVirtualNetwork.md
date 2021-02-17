---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 496e65438a2c0ef5f09bbf961535eaa842062f25
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400892"
---
# <span data-ttu-id="645ba-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="645ba-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="645ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="645ba-102">SYNOPSIS</span></span>
<span data-ttu-id="645ba-103">Létrehozza a PsApiManagementVirtualNetwork példányát.</span><span class="sxs-lookup"><span data-stu-id="645ba-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="645ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="645ba-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="645ba-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="645ba-105">DESCRIPTION</span></span>
<span data-ttu-id="645ba-106">A **New-AzApiManagementVirtualNetwork** parancsmag egy segítő parancs a **PsApiManagementVirtualNetwork** példányának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="645ba-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="645ba-107">Ez a parancs a **Set-AzApiManagement parancsmaggal** használható.</span><span class="sxs-lookup"><span data-stu-id="645ba-107">This command is used with **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="645ba-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="645ba-108">EXAMPLES</span></span>

### <span data-ttu-id="645ba-109">1. példa: Virtuális hálózat létrehozása</span><span class="sxs-lookup"><span data-stu-id="645ba-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Set-AzApiManagement -ApiManagement $service
```

<span data-ttu-id="645ba-110">Ez a példa létrehoz egy virtuális hálózatot, majd felhívja a **Set-AzApiManagement** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="645ba-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="645ba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="645ba-111">PARAMETERS</span></span>

### <span data-ttu-id="645ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645ba-112">-DefaultProfile</span></span>
<span data-ttu-id="645ba-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="645ba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="645ba-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="645ba-114">-SubnetResourceId</span></span>
<span data-ttu-id="645ba-115">A virtuális hálózat alhálózati erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="645ba-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="645ba-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645ba-116">CommonParameters</span></span>
<span data-ttu-id="645ba-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="645ba-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645ba-118">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="645ba-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645ba-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="645ba-119">INPUTS</span></span>

### <span data-ttu-id="645ba-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="645ba-120">None</span></span>

## <span data-ttu-id="645ba-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="645ba-121">OUTPUTS</span></span>

### <span data-ttu-id="645ba-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="645ba-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="645ba-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="645ba-123">NOTES</span></span>

## <span data-ttu-id="645ba-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="645ba-124">RELATED LINKS</span></span>

[<span data-ttu-id="645ba-125">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="645ba-125">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

