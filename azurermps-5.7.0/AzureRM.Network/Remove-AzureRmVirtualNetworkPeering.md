---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: a128f7c9e9440255ed01b32c4460ffd180655928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504523"
---
# <span data-ttu-id="0955c-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0955c-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="0955c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0955c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0955c-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0955c-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0955c-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="0955c-104">DESCRIPTION</span></span>

## <span data-ttu-id="0955c-105">Példák</span><span class="sxs-lookup"><span data-stu-id="0955c-105">EXAMPLES</span></span>

### <span data-ttu-id="0955c-106">Példa 1: virtuális hálózat társközi eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0955c-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="0955c-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0955c-107">PARAMETERS</span></span>

### <span data-ttu-id="0955c-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0955c-108">-AsJob</span></span>
<span data-ttu-id="0955c-109">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0955c-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0955c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0955c-110">-DefaultProfile</span></span>
<span data-ttu-id="0955c-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0955c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0955c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="0955c-112">-Force</span></span>
<span data-ttu-id="0955c-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0955c-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0955c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0955c-114">-Name</span></span>
<span data-ttu-id="0955c-115">A virtuális hálózat társközi neve.</span><span class="sxs-lookup"><span data-stu-id="0955c-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="0955c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0955c-116">-PassThru</span></span>
<span data-ttu-id="0955c-117">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0955c-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0955c-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0955c-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0955c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0955c-119">-ResourceGroupName</span></span>
<span data-ttu-id="0955c-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0955c-120">The resource group name</span></span>

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

### <span data-ttu-id="0955c-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0955c-121">-VirtualNetworkName</span></span>
<span data-ttu-id="0955c-122">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="0955c-122">The virtual network name.</span></span>

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

### <span data-ttu-id="0955c-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0955c-123">-Confirm</span></span>
<span data-ttu-id="0955c-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0955c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0955c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0955c-125">-WhatIf</span></span>
<span data-ttu-id="0955c-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0955c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0955c-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0955c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0955c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0955c-128">CommonParameters</span></span>
<span data-ttu-id="0955c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0955c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0955c-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0955c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0955c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0955c-131">INPUTS</span></span>

### <span data-ttu-id="0955c-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="0955c-132">None</span></span>
<span data-ttu-id="0955c-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0955c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0955c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0955c-134">OUTPUTS</span></span>

## <span data-ttu-id="0955c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0955c-135">NOTES</span></span>

## <span data-ttu-id="0955c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0955c-136">RELATED LINKS</span></span>

