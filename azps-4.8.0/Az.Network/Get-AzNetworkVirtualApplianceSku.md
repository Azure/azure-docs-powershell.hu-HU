---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181089"
---
# <span data-ttu-id="b3c06-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="b3c06-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="b3c06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3c06-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c06-103">A leltárban elérhető hálózat virtuális készülék-SKU beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="b3c06-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="b3c06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3c06-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3c06-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3c06-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c06-106">A Get-AzNetworkVirtualApplianceSku a Microsoft Azure Inventory szolgáltatásban elérhető hálózati virtuális készülék-SKU-t kapja vagy listázza.</span><span class="sxs-lookup"><span data-stu-id="b3c06-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="b3c06-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b3c06-107">EXAMPLES</span></span>

### <span data-ttu-id="b3c06-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b3c06-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="b3c06-109">SKU kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="b3c06-109">Get a sku by name.</span></span>

### <span data-ttu-id="b3c06-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="b3c06-110">Example 2</span></span>
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

<span data-ttu-id="b3c06-111">A hálózati virtuális készülék összes elérhető SKU-je listázása</span><span class="sxs-lookup"><span data-stu-id="b3c06-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="b3c06-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3c06-112">PARAMETERS</span></span>

### <span data-ttu-id="b3c06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c06-113">-DefaultProfile</span></span>
<span data-ttu-id="b3c06-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3c06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3c06-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b3c06-115">-SkuName</span></span>
<span data-ttu-id="b3c06-116">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="b3c06-116">The Sku name.</span></span>

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

### <span data-ttu-id="b3c06-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c06-117">CommonParameters</span></span>
<span data-ttu-id="b3c06-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3c06-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c06-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b3c06-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c06-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3c06-120">INPUTS</span></span>

### <span data-ttu-id="b3c06-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="b3c06-121">None</span></span>

## <span data-ttu-id="b3c06-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3c06-122">OUTPUTS</span></span>

### <span data-ttu-id="b3c06-123">Microsoft. Azure. commands. Network. models. PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="b3c06-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="b3c06-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3c06-124">NOTES</span></span>

## <span data-ttu-id="b3c06-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3c06-125">RELATED LINKS</span></span>
