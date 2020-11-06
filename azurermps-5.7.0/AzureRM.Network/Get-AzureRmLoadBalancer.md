---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: b57d228ca6b31f84797baa7b2b41073edfa6c3ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493764"
---
# <span data-ttu-id="d7631-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7631-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="d7631-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7631-102">SYNOPSIS</span></span>
<span data-ttu-id="d7631-103">Terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="d7631-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7631-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7631-104">SYNTAX</span></span>

### <span data-ttu-id="d7631-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="d7631-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7631-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="d7631-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7631-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7631-107">DESCRIPTION</span></span>
<span data-ttu-id="d7631-108">A **Get-AzureRmLoadBalancer** parancsmag egy vagy több, az erőforráscsoport által tartalmazott, az Azure rendszerhez tartozó terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="d7631-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="d7631-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d7631-109">EXAMPLES</span></span>

### <span data-ttu-id="d7631-110">Példa 1: terheléselosztó beszerzése</span><span class="sxs-lookup"><span data-stu-id="d7631-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d7631-111">Ez a parancs a MyLoadBalancer nevű terheléselosztó parancsot kapja.</span><span class="sxs-lookup"><span data-stu-id="d7631-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="d7631-112">A parancsmag futtatásához a terheléselosztásnak léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="d7631-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="d7631-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7631-113">PARAMETERS</span></span>

### <span data-ttu-id="d7631-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7631-114">-DefaultProfile</span></span>
<span data-ttu-id="d7631-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7631-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7631-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d7631-116">-ExpandResource</span></span>
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

### <span data-ttu-id="d7631-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7631-117">-Name</span></span>
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

### <span data-ttu-id="d7631-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7631-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d7631-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7631-119">CommonParameters</span></span>
<span data-ttu-id="d7631-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7631-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7631-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7631-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7631-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7631-122">INPUTS</span></span>

### <span data-ttu-id="d7631-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7631-123">None</span></span>
<span data-ttu-id="d7631-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d7631-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7631-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7631-125">OUTPUTS</span></span>

### <span data-ttu-id="d7631-126">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7631-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d7631-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7631-127">NOTES</span></span>

## <span data-ttu-id="d7631-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7631-128">RELATED LINKS</span></span>

[<span data-ttu-id="d7631-129">Új – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7631-129">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="d7631-130">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7631-130">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="d7631-131">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7631-131">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


