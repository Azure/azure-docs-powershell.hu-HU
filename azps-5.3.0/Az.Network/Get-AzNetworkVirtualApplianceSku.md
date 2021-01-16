---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379916"
---
# <span data-ttu-id="a3737-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="a3737-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="a3737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3737-102">SYNOPSIS</span></span>
<span data-ttu-id="a3737-103">Szerezze be vagy sorolja fel a rendelkezésre álló hálózati virtuális eszköz-termék termékét a készletben.</span><span class="sxs-lookup"><span data-stu-id="a3737-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="a3737-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3737-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3737-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3737-105">DESCRIPTION</span></span>
<span data-ttu-id="a3737-106">A Get-AzNetworkVirtualApplianceSku a Microsoft Azure készletében elérhető Hálózati virtuális eszköz terméksok listáját.</span><span class="sxs-lookup"><span data-stu-id="a3737-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="a3737-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3737-107">EXAMPLES</span></span>

### <span data-ttu-id="a3737-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a3737-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="a3737-109">Termékváltozat lekérte név szerint.</span><span class="sxs-lookup"><span data-stu-id="a3737-109">Get a sku by name.</span></span>

### <span data-ttu-id="a3737-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="a3737-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="a3737-111">Sorolja fel a hálózati virtuális eszköz összes elérhető termékét.</span><span class="sxs-lookup"><span data-stu-id="a3737-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="a3737-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3737-112">PARAMETERS</span></span>

### <span data-ttu-id="a3737-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3737-113">-DefaultProfile</span></span>
<span data-ttu-id="a3737-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3737-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3737-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a3737-115">-SkuName</span></span>
<span data-ttu-id="a3737-116">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="a3737-116">The Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3737-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3737-117">CommonParameters</span></span>
<span data-ttu-id="a3737-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3737-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3737-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3737-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3737-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3737-120">INPUTS</span></span>

### <span data-ttu-id="a3737-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="a3737-121">None</span></span>

## <span data-ttu-id="a3737-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3737-122">OUTPUTS</span></span>

### <span data-ttu-id="a3737-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="a3737-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="a3737-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3737-124">NOTES</span></span>

## <span data-ttu-id="a3737-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3737-125">RELATED LINKS</span></span>
