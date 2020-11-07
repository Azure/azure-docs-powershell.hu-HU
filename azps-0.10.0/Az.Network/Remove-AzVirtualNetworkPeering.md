---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3bc816f690f39b534a134e80df1a86c7bbca5dc1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843741"
---
# <span data-ttu-id="7312a-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="7312a-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="7312a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7312a-102">SYNOPSIS</span></span>

## <span data-ttu-id="7312a-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7312a-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7312a-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="7312a-104">DESCRIPTION</span></span>

## <span data-ttu-id="7312a-105">Példák</span><span class="sxs-lookup"><span data-stu-id="7312a-105">EXAMPLES</span></span>

### <span data-ttu-id="7312a-106">Példa 1: virtuális hálózat társközi eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7312a-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="7312a-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7312a-107">PARAMETERS</span></span>

### <span data-ttu-id="7312a-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7312a-108">-AsJob</span></span>
<span data-ttu-id="7312a-109">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7312a-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7312a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7312a-110">-DefaultProfile</span></span>
<span data-ttu-id="7312a-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7312a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7312a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="7312a-112">-Force</span></span>
<span data-ttu-id="7312a-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7312a-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7312a-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7312a-114">-Name</span></span>
<span data-ttu-id="7312a-115">A virtuális hálózat társközi neve.</span><span class="sxs-lookup"><span data-stu-id="7312a-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="7312a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7312a-116">-PassThru</span></span>
<span data-ttu-id="7312a-117">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7312a-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7312a-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7312a-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7312a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7312a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7312a-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7312a-120">The resource group name</span></span>

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

### <span data-ttu-id="7312a-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7312a-121">-VirtualNetworkName</span></span>
<span data-ttu-id="7312a-122">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="7312a-122">The virtual network name.</span></span>

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

### <span data-ttu-id="7312a-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7312a-123">-Confirm</span></span>
<span data-ttu-id="7312a-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7312a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7312a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7312a-125">-WhatIf</span></span>
<span data-ttu-id="7312a-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7312a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7312a-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7312a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7312a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7312a-128">CommonParameters</span></span>
<span data-ttu-id="7312a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7312a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7312a-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7312a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7312a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7312a-131">INPUTS</span></span>

## <span data-ttu-id="7312a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7312a-132">OUTPUTS</span></span>

## <span data-ttu-id="7312a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7312a-133">NOTES</span></span>

## <span data-ttu-id="7312a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7312a-134">RELATED LINKS</span></span>

