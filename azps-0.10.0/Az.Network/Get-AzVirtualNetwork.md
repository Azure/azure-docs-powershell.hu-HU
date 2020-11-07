---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841521"
---
# <span data-ttu-id="627d9-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="627d9-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="627d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="627d9-102">SYNOPSIS</span></span>
<span data-ttu-id="627d9-103">Virtuális hálózat beolvasása egy erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="627d9-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="627d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="627d9-104">SYNTAX</span></span>

### <span data-ttu-id="627d9-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="627d9-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627d9-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="627d9-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="627d9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="627d9-107">DESCRIPTION</span></span>
<span data-ttu-id="627d9-108">A **Get-AzVirtualNetwork** parancsmag egy vagy több virtuális hálózattal rendelkezik, és egy erőforráscsoport lesz.</span><span class="sxs-lookup"><span data-stu-id="627d9-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="627d9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="627d9-109">EXAMPLES</span></span>

### <span data-ttu-id="627d9-110">1: virtuális hálózat beolvasása</span><span class="sxs-lookup"><span data-stu-id="627d9-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="627d9-111">Ez a parancs a MyVirtualNetwork nevű virtuális hálózatot kapja az erőforráscsoport TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="627d9-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="627d9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="627d9-112">PARAMETERS</span></span>

### <span data-ttu-id="627d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627d9-113">-DefaultProfile</span></span>
<span data-ttu-id="627d9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="627d9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="627d9-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="627d9-115">-ExpandResource</span></span>
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

### <span data-ttu-id="627d9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="627d9-116">-Name</span></span>
<span data-ttu-id="627d9-117">Annak a virtuális hálózatnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="627d9-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="627d9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="627d9-118">-ResourceGroupName</span></span>
<span data-ttu-id="627d9-119">Annak a csoportnak a neve, amelyhez a virtuális hálózat tartozik.</span><span class="sxs-lookup"><span data-stu-id="627d9-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="627d9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627d9-120">CommonParameters</span></span>
<span data-ttu-id="627d9-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="627d9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627d9-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="627d9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627d9-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="627d9-123">INPUTS</span></span>

## <span data-ttu-id="627d9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="627d9-124">OUTPUTS</span></span>

### <span data-ttu-id="627d9-125">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="627d9-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="627d9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="627d9-126">NOTES</span></span>

## <span data-ttu-id="627d9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="627d9-127">RELATED LINKS</span></span>

[<span data-ttu-id="627d9-128">Új – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="627d9-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="627d9-129">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="627d9-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="627d9-130">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="627d9-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


