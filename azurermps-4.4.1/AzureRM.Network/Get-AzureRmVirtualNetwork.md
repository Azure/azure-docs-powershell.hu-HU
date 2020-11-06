---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: d955cb51d92d9d0f3c156900d847e903d642e9af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497800"
---
# <span data-ttu-id="7a50a-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a50a-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="7a50a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a50a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a50a-103">Virtuális hálózat beolvasása egy erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="7a50a-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a50a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a50a-104">SYNTAX</span></span>

### <span data-ttu-id="7a50a-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="7a50a-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a50a-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="7a50a-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a50a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a50a-107">DESCRIPTION</span></span>
<span data-ttu-id="7a50a-108">A **Get-AzureRmVirtualNetwork** parancsmag egy vagy több virtuális hálózattal rendelkezik, és egy erőforráscsoport lesz.</span><span class="sxs-lookup"><span data-stu-id="7a50a-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="7a50a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7a50a-109">EXAMPLES</span></span>

### <span data-ttu-id="7a50a-110">1: virtuális hálózat beolvasása</span><span class="sxs-lookup"><span data-stu-id="7a50a-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="7a50a-111">Ez a parancs a MyVirtualNetwork nevű virtuális hálózatot kapja az erőforráscsoport TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7a50a-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="7a50a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a50a-112">PARAMETERS</span></span>

### <span data-ttu-id="7a50a-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="7a50a-113">-ExpandResource</span></span>
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

### <span data-ttu-id="7a50a-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a50a-114">-Name</span></span>
<span data-ttu-id="7a50a-115">Annak a virtuális hálózatnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="7a50a-115">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7a50a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a50a-116">-ResourceGroupName</span></span>
<span data-ttu-id="7a50a-117">Annak a csoportnak a neve, amelyhez a virtuális hálózat tartozik.</span><span class="sxs-lookup"><span data-stu-id="7a50a-117">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="7a50a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a50a-118">-DefaultProfile</span></span>
<span data-ttu-id="7a50a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a50a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a50a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a50a-120">CommonParameters</span></span>
<span data-ttu-id="7a50a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a50a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a50a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a50a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a50a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a50a-123">INPUTS</span></span>

## <span data-ttu-id="7a50a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a50a-124">OUTPUTS</span></span>

### <span data-ttu-id="7a50a-125">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a50a-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7a50a-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a50a-126">NOTES</span></span>

## <span data-ttu-id="7a50a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a50a-127">RELATED LINKS</span></span>

[<span data-ttu-id="7a50a-128">Új – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a50a-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="7a50a-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a50a-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="7a50a-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a50a-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


