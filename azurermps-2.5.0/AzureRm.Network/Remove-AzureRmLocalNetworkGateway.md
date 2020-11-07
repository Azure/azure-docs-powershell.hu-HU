---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 7b3fde5feb5dae1ca064b8f5e31bbdfe03e12c7a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850341"
---
# <span data-ttu-id="ac11a-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac11a-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="ac11a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac11a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac11a-103">Helyi hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="ac11a-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac11a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac11a-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac11a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac11a-105">DESCRIPTION</span></span>
<span data-ttu-id="ac11a-106">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="ac11a-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="ac11a-107">A **Remove-AzureRmLocalNetworkGateway** parancsmag a helyszíni átjáró név és erőforrás csoport neve alapján történő törlésére szolgáló objektumot törli.</span><span class="sxs-lookup"><span data-stu-id="ac11a-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ac11a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ac11a-108">EXAMPLES</span></span>

### <span data-ttu-id="ac11a-109">1: helyi hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="ac11a-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="ac11a-110">Törli a helyi hálózati átjáró objektumát "myLocalGW" néven a "myRG" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="ac11a-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="ac11a-111">Megjegyzés: a **Remove-AzureRmVirtualNetworkGatewayConnection** parancsmag segítségével először törölnie kell minden kapcsolatot a helyi hálózati átjáróval.</span><span class="sxs-lookup"><span data-stu-id="ac11a-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="ac11a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac11a-112">PARAMETERS</span></span>

### <span data-ttu-id="ac11a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac11a-113">-AsJob</span></span>
<span data-ttu-id="ac11a-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ac11a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac11a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac11a-115">-DefaultProfile</span></span>
<span data-ttu-id="ac11a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac11a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac11a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ac11a-117">-Force</span></span>
<span data-ttu-id="ac11a-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ac11a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac11a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac11a-119">-Name</span></span>
<span data-ttu-id="ac11a-120">A parancsmag által eltávolított helyi hálózati átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac11a-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ac11a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac11a-121">-PassThru</span></span>
<span data-ttu-id="ac11a-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ac11a-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac11a-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ac11a-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac11a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac11a-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac11a-125">A helyi hálózati átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac11a-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="ac11a-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac11a-126">-Confirm</span></span>
<span data-ttu-id="ac11a-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac11a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac11a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac11a-128">-WhatIf</span></span>
<span data-ttu-id="ac11a-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac11a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac11a-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac11a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac11a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac11a-131">CommonParameters</span></span>
<span data-ttu-id="ac11a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac11a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac11a-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac11a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac11a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac11a-134">INPUTS</span></span>

## <span data-ttu-id="ac11a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac11a-135">OUTPUTS</span></span>

## <span data-ttu-id="ac11a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac11a-136">NOTES</span></span>

## <span data-ttu-id="ac11a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac11a-137">RELATED LINKS</span></span>

[<span data-ttu-id="ac11a-138">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac11a-138">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="ac11a-139">Új – AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac11a-139">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="ac11a-140">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac11a-140">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


