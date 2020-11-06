---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 401fcbd5fca9fc0251e4de0fb7843fb95c1c122d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502647"
---
# <span data-ttu-id="5979e-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5979e-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="5979e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5979e-102">SYNOPSIS</span></span>
<span data-ttu-id="5979e-103">Virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="5979e-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5979e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5979e-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5979e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5979e-105">DESCRIPTION</span></span>
<span data-ttu-id="5979e-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5979e-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="5979e-107">A **Get-AzureRmVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="5979e-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="5979e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5979e-108">EXAMPLES</span></span>

### <span data-ttu-id="5979e-109">1: virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="5979e-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="5979e-110">Törli a virtuális hálózati átjáró objektumát "myGateway" néven a "myRG" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5979e-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="5979e-111">Megjegyzés: a **Remove-AzureRmVirtualNetworkGatewayConnection** parancsmag használatával először törölnie kell minden kapcsolatot a virtuális hálózati átjáróval.</span><span class="sxs-lookup"><span data-stu-id="5979e-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="5979e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5979e-112">PARAMETERS</span></span>

### <span data-ttu-id="5979e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5979e-113">-Force</span></span>
<span data-ttu-id="5979e-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="5979e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5979e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5979e-115">-Name</span></span>
<span data-ttu-id="5979e-116">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="5979e-116">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5979e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5979e-117">-PassThru</span></span>
<span data-ttu-id="5979e-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5979e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5979e-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5979e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5979e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5979e-120">-ResourceGroupName</span></span>
<span data-ttu-id="5979e-121">A virtuális hálózati átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5979e-121">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="5979e-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5979e-122">-Confirm</span></span>
<span data-ttu-id="5979e-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5979e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5979e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5979e-124">-WhatIf</span></span>
<span data-ttu-id="5979e-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5979e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5979e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5979e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5979e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5979e-127">-DefaultProfile</span></span>
<span data-ttu-id="5979e-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5979e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5979e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5979e-129">CommonParameters</span></span>
<span data-ttu-id="5979e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5979e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5979e-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5979e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5979e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5979e-132">INPUTS</span></span>

## <span data-ttu-id="5979e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5979e-133">OUTPUTS</span></span>

## <span data-ttu-id="5979e-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5979e-134">NOTES</span></span>

## <span data-ttu-id="5979e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5979e-135">RELATED LINKS</span></span>

