---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 2b1e781a65eaa6a43c4f8571caf1850f0b04d6cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680764"
---
# <span data-ttu-id="4a205-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="4a205-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="4a205-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a205-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a205-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a205-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a205-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a205-104">DESCRIPTION</span></span>

## <span data-ttu-id="4a205-105">Példák</span><span class="sxs-lookup"><span data-stu-id="4a205-105">EXAMPLES</span></span>

### <span data-ttu-id="4a205-106">Példa 1: virtuális hálózat társközi eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4a205-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="4a205-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a205-107">PARAMETERS</span></span>

### <span data-ttu-id="4a205-108">-Force</span><span class="sxs-lookup"><span data-stu-id="4a205-108">-Force</span></span>
<span data-ttu-id="4a205-109">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4a205-109">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a205-110">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a205-110">-Name</span></span>
<span data-ttu-id="4a205-111">A virtuális hálózat társközi neve.</span><span class="sxs-lookup"><span data-stu-id="4a205-111">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a205-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a205-112">-PassThru</span></span>
<span data-ttu-id="4a205-113">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4a205-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4a205-114">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4a205-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a205-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a205-115">-ResourceGroupName</span></span>
<span data-ttu-id="4a205-116">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4a205-116">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a205-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4a205-117">-VirtualNetworkName</span></span>
<span data-ttu-id="4a205-118">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="4a205-118">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a205-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a205-119">-Confirm</span></span>
<span data-ttu-id="4a205-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a205-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a205-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a205-121">-WhatIf</span></span>
<span data-ttu-id="4a205-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a205-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a205-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a205-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a205-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a205-124">-DefaultProfile</span></span>
<span data-ttu-id="4a205-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a205-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a205-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a205-126">CommonParameters</span></span>
<span data-ttu-id="4a205-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a205-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a205-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a205-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a205-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a205-129">INPUTS</span></span>

## <span data-ttu-id="4a205-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a205-130">OUTPUTS</span></span>

## <span data-ttu-id="4a205-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a205-131">NOTES</span></span>

## <span data-ttu-id="4a205-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a205-132">RELATED LINKS</span></span>

