---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: de39828183f06f8435078ceffc8c303c376e6186
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850613"
---
# <span data-ttu-id="196d9-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="196d9-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="196d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="196d9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="196d9-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="196d9-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="196d9-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="196d9-104">DESCRIPTION</span></span>

## <span data-ttu-id="196d9-105">Példák</span><span class="sxs-lookup"><span data-stu-id="196d9-105">EXAMPLES</span></span>

### <span data-ttu-id="196d9-106">Példa 1: virtuális hálózat társközi eltávolítása</span><span class="sxs-lookup"><span data-stu-id="196d9-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="196d9-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="196d9-107">PARAMETERS</span></span>

### <span data-ttu-id="196d9-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="196d9-108">-AsJob</span></span>
<span data-ttu-id="196d9-109">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="196d9-109">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196d9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196d9-110">-DefaultProfile</span></span>
<span data-ttu-id="196d9-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="196d9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="196d9-112">-Force</span><span class="sxs-lookup"><span data-stu-id="196d9-112">-Force</span></span>
<span data-ttu-id="196d9-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="196d9-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196d9-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="196d9-114">-Name</span></span>
<span data-ttu-id="196d9-115">A virtuális hálózat társközi neve.</span><span class="sxs-lookup"><span data-stu-id="196d9-115">The virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="196d9-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="196d9-116">-PassThru</span></span>
<span data-ttu-id="196d9-117">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="196d9-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="196d9-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="196d9-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="196d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="196d9-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="196d9-120">The resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="196d9-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="196d9-121">-VirtualNetworkName</span></span>
<span data-ttu-id="196d9-122">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="196d9-122">The virtual network name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="196d9-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="196d9-123">-Confirm</span></span>
<span data-ttu-id="196d9-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="196d9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196d9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196d9-125">-WhatIf</span></span>
<span data-ttu-id="196d9-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="196d9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="196d9-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="196d9-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196d9-128">CommonParameters</span></span>
<span data-ttu-id="196d9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="196d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196d9-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="196d9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196d9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="196d9-131">INPUTS</span></span>

## <span data-ttu-id="196d9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="196d9-132">OUTPUTS</span></span>

## <span data-ttu-id="196d9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="196d9-133">NOTES</span></span>

## <span data-ttu-id="196d9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="196d9-134">RELATED LINKS</span></span>

