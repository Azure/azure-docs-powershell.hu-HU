---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 3a5cd755718536170c3e6fb1f6dd5410e1acffc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505747"
---
# <span data-ttu-id="cbcf3-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cbcf3-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="cbcf3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbcf3-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcf3-103">Virtuális hálózat beolvasása egy erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="cbcf3-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbcf3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbcf3-104">SYNTAX</span></span>

### <span data-ttu-id="cbcf3-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="cbcf3-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbcf3-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="cbcf3-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbcf3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbcf3-107">DESCRIPTION</span></span>
<span data-ttu-id="cbcf3-108">A **Get-AzureRmVirtualNetwork** parancsmag egy vagy több virtuális hálózattal rendelkezik, és egy erőforráscsoport lesz.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="cbcf3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cbcf3-109">EXAMPLES</span></span>

### <span data-ttu-id="cbcf3-110">1: virtuális hálózat beolvasása</span><span class="sxs-lookup"><span data-stu-id="cbcf3-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="cbcf3-111">Ez a parancs a MyVirtualNetwork nevű virtuális hálózatot kapja az erőforráscsoport TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cbcf3-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="cbcf3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbcf3-112">PARAMETERS</span></span>

### <span data-ttu-id="cbcf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcf3-113">-DefaultProfile</span></span>
<span data-ttu-id="cbcf3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbcf3-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="cbcf3-115">-ExpandResource</span></span>
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

### <span data-ttu-id="cbcf3-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cbcf3-116">-Name</span></span>
<span data-ttu-id="cbcf3-117">Annak a virtuális hálózatnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cbcf3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcf3-118">-ResourceGroupName</span></span>
<span data-ttu-id="cbcf3-119">Annak a csoportnak a neve, amelyhez a virtuális hálózat tartozik.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="cbcf3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcf3-120">CommonParameters</span></span>
<span data-ttu-id="cbcf3-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbcf3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcf3-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbcf3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcf3-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbcf3-123">INPUTS</span></span>

### <span data-ttu-id="cbcf3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="cbcf3-124">System.String</span></span>

## <span data-ttu-id="cbcf3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbcf3-125">OUTPUTS</span></span>

### <span data-ttu-id="cbcf3-126">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cbcf3-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cbcf3-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbcf3-127">NOTES</span></span>

## <span data-ttu-id="cbcf3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbcf3-128">RELATED LINKS</span></span>

[<span data-ttu-id="cbcf3-129">Új – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cbcf3-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cbcf3-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cbcf3-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cbcf3-131">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cbcf3-131">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


