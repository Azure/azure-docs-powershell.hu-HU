---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 90cafc66857ee2ec94806628b41960eaafaf6e15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495951"
---
# <span data-ttu-id="6d15c-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d15c-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="6d15c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d15c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d15c-103">Terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="6d15c-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d15c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d15c-104">SYNTAX</span></span>

### <span data-ttu-id="6d15c-105">Kibontott (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d15c-105">NoExpand (Default)</span></span>
```
Get-AzureRmLoadBalancer [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d15c-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="6d15c-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d15c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d15c-107">DESCRIPTION</span></span>
<span data-ttu-id="6d15c-108">A **Get-AzureRmLoadBalancer** parancsmag egy vagy több, az erőforráscsoport által tartalmazott, az Azure rendszerhez tartozó terheléselosztást kap.</span><span class="sxs-lookup"><span data-stu-id="6d15c-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="6d15c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6d15c-109">EXAMPLES</span></span>

### <span data-ttu-id="6d15c-110">Példa 1: terheléselosztó beszerzése</span><span class="sxs-lookup"><span data-stu-id="6d15c-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="6d15c-111">Ez a parancs a MyLoadBalancer nevű terheléselosztó parancsot kapja.</span><span class="sxs-lookup"><span data-stu-id="6d15c-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="6d15c-112">A parancsmag futtatásához a terheléselosztásnak léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="6d15c-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="6d15c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d15c-113">PARAMETERS</span></span>

### <span data-ttu-id="6d15c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d15c-114">-DefaultProfile</span></span>
<span data-ttu-id="6d15c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d15c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d15c-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6d15c-116">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d15c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6d15c-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d15c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d15c-118">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d15c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d15c-119">CommonParameters</span></span>
<span data-ttu-id="6d15c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d15c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d15c-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d15c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d15c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d15c-122">INPUTS</span></span>

### <span data-ttu-id="6d15c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6d15c-123">System.String</span></span>

## <span data-ttu-id="6d15c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d15c-124">OUTPUTS</span></span>

### <span data-ttu-id="6d15c-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d15c-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6d15c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d15c-126">NOTES</span></span>

## <span data-ttu-id="6d15c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d15c-127">RELATED LINKS</span></span>

[<span data-ttu-id="6d15c-128">Új – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d15c-128">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="6d15c-129">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d15c-129">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="6d15c-130">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d15c-130">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


