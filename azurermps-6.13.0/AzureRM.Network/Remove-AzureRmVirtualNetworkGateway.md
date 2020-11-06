---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 65e4259b7b530c7ea003860ab30c9f0c0baa7250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503495"
---
# <span data-ttu-id="b4aa4-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4aa4-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b4aa4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="b4aa4-103">Virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="b4aa4-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4aa4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4aa4-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4aa4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="b4aa4-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="b4aa4-107">A **Get-AzureRmVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b4aa4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b4aa4-108">EXAMPLES</span></span>

### <span data-ttu-id="b4aa4-109">1: virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="b4aa4-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b4aa4-110">Törli a virtuális hálózati átjáró objektumát a "myGateway" nevű erőforrás-csoport "myRG" Megjegyzés: először törölnie kell a virtuális hálózati átjáróval való összes kapcsolatot a **Remove-AzureRmVirtualNetworkGatewayConnection** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="b4aa4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4aa4-111">PARAMETERS</span></span>

### <span data-ttu-id="b4aa4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4aa4-112">-AsJob</span></span>
<span data-ttu-id="b4aa4-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b4aa4-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4aa4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4aa4-114">-DefaultProfile</span></span>
<span data-ttu-id="b4aa4-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4aa4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b4aa4-116">-Force</span></span>
<span data-ttu-id="b4aa4-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4aa4-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4aa4-118">-Name</span></span>
<span data-ttu-id="b4aa4-119">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4aa4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4aa4-120">-PassThru</span></span>
<span data-ttu-id="b4aa4-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b4aa4-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4aa4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4aa4-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4aa4-124">A virtuális hálózati átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="b4aa4-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4aa4-125">-Confirm</span></span>
<span data-ttu-id="b4aa4-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4aa4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4aa4-127">-WhatIf</span></span>
<span data-ttu-id="b4aa4-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4aa4-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4aa4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4aa4-130">CommonParameters</span></span>
<span data-ttu-id="b4aa4-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4aa4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4aa4-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4aa4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4aa4-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4aa4-133">INPUTS</span></span>

### <span data-ttu-id="b4aa4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b4aa4-134">System.String</span></span>

## <span data-ttu-id="b4aa4-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4aa4-135">OUTPUTS</span></span>

### <span data-ttu-id="b4aa4-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4aa4-136">System.Boolean</span></span>

## <span data-ttu-id="b4aa4-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4aa4-137">NOTES</span></span>

## <span data-ttu-id="b4aa4-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4aa4-138">RELATED LINKS</span></span>
