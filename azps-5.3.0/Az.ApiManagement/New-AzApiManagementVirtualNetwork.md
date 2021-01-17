---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: c7cf4783c7f374f16a51de9ac4794d5fef441e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382295"
---
# <span data-ttu-id="1b988-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1b988-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="1b988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b988-102">SYNOPSIS</span></span>
<span data-ttu-id="1b988-103">Létrehozza a PsApiManagementVirtualNetwork példányát.</span><span class="sxs-lookup"><span data-stu-id="1b988-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="1b988-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b988-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b988-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b988-105">DESCRIPTION</span></span>
<span data-ttu-id="1b988-106">A **New-AzApiManagementVirtualNetwork** parancsmag egy segítő parancs a **PsApiManagementVirtualNetwork** példányának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="1b988-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="1b988-107">Ez a parancs a **Set-AzApiManagement és** a **New-AzApiManagement** parancsmaggal használható.</span><span class="sxs-lookup"><span data-stu-id="1b988-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="1b988-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b988-108">EXAMPLES</span></span>

### <span data-ttu-id="1b988-109">1. példa: Virtuális hálózat létrehozása és meglévő APIM-szolgáltatás frissítése a VNET-be</span><span class="sxs-lookup"><span data-stu-id="1b988-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="1b988-110">Ez a példa létrehoz egy virtuális hálózatot, majd felhívja a **Set-AzApiManagement** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1b988-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="1b988-111">2. példa: API-kezelési szolgáltatás létrehozása külső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="1b988-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="1b988-112">Ez a példa egy új APIM-szolgáltatást hoz létre virtuális hálózat `External` módban</span><span class="sxs-lookup"><span data-stu-id="1b988-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="1b988-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b988-113">PARAMETERS</span></span>

### <span data-ttu-id="1b988-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b988-114">-DefaultProfile</span></span>
<span data-ttu-id="1b988-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b988-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b988-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="1b988-116">-SubnetResourceId</span></span>
<span data-ttu-id="1b988-117">A virtuális hálózat alhálózati erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b988-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="1b988-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b988-118">CommonParameters</span></span>
<span data-ttu-id="1b988-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b988-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b988-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b988-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b988-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b988-121">INPUTS</span></span>

### <span data-ttu-id="1b988-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="1b988-122">None</span></span>

## <span data-ttu-id="1b988-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b988-123">OUTPUTS</span></span>

### <span data-ttu-id="1b988-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1b988-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="1b988-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b988-125">NOTES</span></span>

## <span data-ttu-id="1b988-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b988-126">RELATED LINKS</span></span>

<span data-ttu-id="1b988-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="1b988-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

