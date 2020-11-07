---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 39bbf3a30f4334e35f58109da86b9b07208682af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849213"
---
# <span data-ttu-id="039c0-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="039c0-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="039c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="039c0-102">SYNOPSIS</span></span>
<span data-ttu-id="039c0-103">Terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="039c0-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="039c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="039c0-104">SYNTAX</span></span>

### <span data-ttu-id="039c0-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="039c0-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="039c0-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="039c0-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="039c0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="039c0-107">DESCRIPTION</span></span>
<span data-ttu-id="039c0-108">A **Get-AzureRmLoadBalancer** parancsmag egy vagy több, az erőforráscsoport által tartalmazott, az Azure rendszerhez tartozó terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="039c0-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="039c0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="039c0-109">EXAMPLES</span></span>

### <span data-ttu-id="039c0-110">Példa 1: terheléselosztó beszerzése</span><span class="sxs-lookup"><span data-stu-id="039c0-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="039c0-111">Ez a parancs a MyLoadBalancer nevű terheléselosztó parancsot kapja.</span><span class="sxs-lookup"><span data-stu-id="039c0-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="039c0-112">A parancsmag futtatásához a terheléselosztásnak léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="039c0-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="039c0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="039c0-113">PARAMETERS</span></span>

### <span data-ttu-id="039c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039c0-114">-DefaultProfile</span></span>
<span data-ttu-id="039c0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="039c0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="039c0-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="039c0-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039c0-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="039c0-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039c0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="039c0-118">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039c0-119">CommonParameters</span></span>
<span data-ttu-id="039c0-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="039c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039c0-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="039c0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039c0-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="039c0-122">INPUTS</span></span>

## <span data-ttu-id="039c0-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="039c0-123">OUTPUTS</span></span>

### <span data-ttu-id="039c0-124">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="039c0-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="039c0-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="039c0-125">NOTES</span></span>

## <span data-ttu-id="039c0-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="039c0-126">RELATED LINKS</span></span>

[<span data-ttu-id="039c0-127">Új – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="039c0-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="039c0-128">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="039c0-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="039c0-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="039c0-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


