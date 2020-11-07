---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 434d70cbdce08750e69865e59197ebba5fb6e6fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843770"
---
# <span data-ttu-id="575e6-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="575e6-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="575e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="575e6-102">SYNOPSIS</span></span>
<span data-ttu-id="575e6-103">Egy útválasztási táblázat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="575e6-103">Removes a route table.</span></span>

## <span data-ttu-id="575e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="575e6-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="575e6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="575e6-105">DESCRIPTION</span></span>
<span data-ttu-id="575e6-106">A **Remove-AzRouteTable** parancsmag eltávolítja az Azure Route-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="575e6-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="575e6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="575e6-107">EXAMPLES</span></span>

### <span data-ttu-id="575e6-108">1. példa: a Route Table eltávolítása</span><span class="sxs-lookup"><span data-stu-id="575e6-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="575e6-109">Ez a parancs eltávolítja a RouteTable01 nevű útvonalkártya-táblázatot a ResourceGroup11 nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="575e6-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="575e6-110">A parancsmag a táblázat eltávolítása előtt kéri a megerősítés megerősítését.</span><span class="sxs-lookup"><span data-stu-id="575e6-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="575e6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="575e6-111">PARAMETERS</span></span>

### <span data-ttu-id="575e6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="575e6-112">-AsJob</span></span>
<span data-ttu-id="575e6-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="575e6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="575e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575e6-114">-DefaultProfile</span></span>
<span data-ttu-id="575e6-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="575e6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="575e6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="575e6-116">-Force</span></span>
<span data-ttu-id="575e6-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="575e6-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="575e6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="575e6-118">-Name</span></span>
<span data-ttu-id="575e6-119">A parancsmag által eltávolított útválasztási táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="575e6-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="575e6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="575e6-120">-PassThru</span></span>
<span data-ttu-id="575e6-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="575e6-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="575e6-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="575e6-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="575e6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="575e6-123">-ResourceGroupName</span></span>
<span data-ttu-id="575e6-124">Annak az erőforrás-csoportnak a neve, amely a parancsmag által eltávolított útválasztási táblát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="575e6-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="575e6-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="575e6-125">-Confirm</span></span>
<span data-ttu-id="575e6-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="575e6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="575e6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="575e6-127">-WhatIf</span></span>
<span data-ttu-id="575e6-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="575e6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="575e6-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="575e6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="575e6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575e6-130">CommonParameters</span></span>
<span data-ttu-id="575e6-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="575e6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575e6-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="575e6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575e6-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="575e6-133">INPUTS</span></span>

## <span data-ttu-id="575e6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="575e6-134">OUTPUTS</span></span>

## <span data-ttu-id="575e6-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="575e6-135">NOTES</span></span>

## <span data-ttu-id="575e6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="575e6-136">RELATED LINKS</span></span>

[<span data-ttu-id="575e6-137">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="575e6-137">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="575e6-138">Új – AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="575e6-138">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="575e6-139">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="575e6-139">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


