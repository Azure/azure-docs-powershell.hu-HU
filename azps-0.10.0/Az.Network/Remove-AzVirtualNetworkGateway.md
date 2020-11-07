---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: bb63f9d56dc78943f9232107e39188ae3d29f43f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843765"
---
# <span data-ttu-id="ce49d-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ce49d-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="ce49d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce49d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce49d-103">Virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="ce49d-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="ce49d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce49d-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce49d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce49d-105">DESCRIPTION</span></span>
<span data-ttu-id="ce49d-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ce49d-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="ce49d-107">A **Get-AzVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="ce49d-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ce49d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ce49d-108">EXAMPLES</span></span>

### <span data-ttu-id="ce49d-109">1: virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="ce49d-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="ce49d-110">Törli a virtuális hálózati átjáró objektumát "myGateway" néven a "myRG" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="ce49d-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="ce49d-111">Megjegyzés: a **Remove-AzVirtualNetworkGatewayConnection** parancsmag használatával először törölnie kell minden kapcsolatot a virtuális hálózati átjáróval.</span><span class="sxs-lookup"><span data-stu-id="ce49d-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="ce49d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce49d-112">PARAMETERS</span></span>

### <span data-ttu-id="ce49d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce49d-113">-AsJob</span></span>
<span data-ttu-id="ce49d-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ce49d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce49d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce49d-115">-DefaultProfile</span></span>
<span data-ttu-id="ce49d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce49d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce49d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ce49d-117">-Force</span></span>
<span data-ttu-id="ce49d-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ce49d-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce49d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce49d-119">-Name</span></span>
<span data-ttu-id="ce49d-120">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ce49d-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce49d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce49d-121">-PassThru</span></span>
<span data-ttu-id="ce49d-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ce49d-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce49d-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ce49d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce49d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce49d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce49d-125">A virtuális hálózati átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce49d-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="ce49d-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce49d-126">-Confirm</span></span>
<span data-ttu-id="ce49d-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce49d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce49d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce49d-128">-WhatIf</span></span>
<span data-ttu-id="ce49d-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce49d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce49d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce49d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce49d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce49d-131">CommonParameters</span></span>
<span data-ttu-id="ce49d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce49d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce49d-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce49d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce49d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce49d-134">INPUTS</span></span>

## <span data-ttu-id="ce49d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce49d-135">OUTPUTS</span></span>

## <span data-ttu-id="ce49d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce49d-136">NOTES</span></span>

## <span data-ttu-id="ce49d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce49d-137">RELATED LINKS</span></span>

