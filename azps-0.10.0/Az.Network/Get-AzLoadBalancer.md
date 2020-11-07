---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841641"
---
# <span data-ttu-id="feb8b-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="feb8b-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="feb8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="feb8b-102">SYNOPSIS</span></span>
<span data-ttu-id="feb8b-103">Terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="feb8b-103">Gets a load balancer.</span></span>

## <span data-ttu-id="feb8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="feb8b-104">SYNTAX</span></span>

### <span data-ttu-id="feb8b-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="feb8b-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb8b-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="feb8b-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feb8b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="feb8b-107">DESCRIPTION</span></span>
<span data-ttu-id="feb8b-108">A **Get-AzLoadBalancer** parancsmag egy vagy több, az erőforráscsoport által tartalmazott, az Azure rendszerhez tartozó terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="feb8b-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="feb8b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="feb8b-109">EXAMPLES</span></span>

### <span data-ttu-id="feb8b-110">Példa 1: terheléselosztó beszerzése</span><span class="sxs-lookup"><span data-stu-id="feb8b-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="feb8b-111">Ez a parancs a MyLoadBalancer nevű terheléselosztó parancsot kapja.</span><span class="sxs-lookup"><span data-stu-id="feb8b-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="feb8b-112">A parancsmag futtatásához a terheléselosztásnak léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="feb8b-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="feb8b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="feb8b-113">PARAMETERS</span></span>

### <span data-ttu-id="feb8b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb8b-114">-DefaultProfile</span></span>
<span data-ttu-id="feb8b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="feb8b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feb8b-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="feb8b-116">-ExpandResource</span></span>
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

### <span data-ttu-id="feb8b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="feb8b-117">-Name</span></span>
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

### <span data-ttu-id="feb8b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb8b-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="feb8b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb8b-119">CommonParameters</span></span>
<span data-ttu-id="feb8b-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="feb8b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb8b-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb8b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb8b-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="feb8b-122">INPUTS</span></span>

## <span data-ttu-id="feb8b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="feb8b-123">OUTPUTS</span></span>

### <span data-ttu-id="feb8b-124">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="feb8b-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="feb8b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="feb8b-125">NOTES</span></span>

## <span data-ttu-id="feb8b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="feb8b-126">RELATED LINKS</span></span>

[<span data-ttu-id="feb8b-127">Új – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="feb8b-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="feb8b-128">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="feb8b-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="feb8b-129">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="feb8b-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


