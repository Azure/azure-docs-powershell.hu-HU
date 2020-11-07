---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: f78b888e75db758f254924dee9fbf501050717b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850614"
---
# <span data-ttu-id="0f21a-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0f21a-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="0f21a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f21a-102">SYNOPSIS</span></span>
<span data-ttu-id="0f21a-103">Egy útválasztási táblázat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0f21a-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f21a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f21a-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f21a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f21a-105">DESCRIPTION</span></span>
<span data-ttu-id="0f21a-106">A **Remove-AzureRmRouteTable** parancsmag eltávolítja az Azure Route-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0f21a-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="0f21a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0f21a-107">EXAMPLES</span></span>

### <span data-ttu-id="0f21a-108">1. példa: a Route Table eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0f21a-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="0f21a-109">Ez a parancs eltávolítja a RouteTable01 nevű útvonalkártya-táblázatot a ResourceGroup11 nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="0f21a-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="0f21a-110">A parancsmag a táblázat eltávolítása előtt kéri a megerősítés megerősítését.</span><span class="sxs-lookup"><span data-stu-id="0f21a-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="0f21a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f21a-111">PARAMETERS</span></span>

### <span data-ttu-id="0f21a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f21a-112">-AsJob</span></span>
<span data-ttu-id="0f21a-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f21a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f21a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f21a-114">-DefaultProfile</span></span>
<span data-ttu-id="0f21a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f21a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f21a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0f21a-116">-Force</span></span>
<span data-ttu-id="0f21a-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0f21a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f21a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f21a-118">-Name</span></span>
<span data-ttu-id="0f21a-119">A parancsmag által eltávolított útválasztási táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f21a-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f21a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f21a-120">-PassThru</span></span>
<span data-ttu-id="0f21a-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0f21a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f21a-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0f21a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f21a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f21a-123">-ResourceGroupName</span></span>
<span data-ttu-id="0f21a-124">Annak az erőforrás-csoportnak a neve, amely a parancsmag által eltávolított útválasztási táblát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0f21a-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f21a-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f21a-125">-Confirm</span></span>
<span data-ttu-id="0f21a-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f21a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f21a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f21a-127">-WhatIf</span></span>
<span data-ttu-id="0f21a-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f21a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f21a-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f21a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f21a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f21a-130">CommonParameters</span></span>
<span data-ttu-id="0f21a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f21a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f21a-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f21a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f21a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f21a-133">INPUTS</span></span>

## <span data-ttu-id="0f21a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f21a-134">OUTPUTS</span></span>

## <span data-ttu-id="0f21a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f21a-135">NOTES</span></span>

## <span data-ttu-id="0f21a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f21a-136">RELATED LINKS</span></span>

[<span data-ttu-id="0f21a-137">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0f21a-137">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="0f21a-138">Új – AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0f21a-138">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="0f21a-139">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0f21a-139">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


