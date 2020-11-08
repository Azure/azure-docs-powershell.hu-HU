---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186883"
---
# <span data-ttu-id="ca981-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca981-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="ca981-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca981-102">SYNOPSIS</span></span>
<span data-ttu-id="ca981-103">Egy útválasztási táblázat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ca981-103">Removes a route table.</span></span>

## <span data-ttu-id="ca981-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca981-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca981-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca981-105">DESCRIPTION</span></span>
<span data-ttu-id="ca981-106">A **Remove-AzRouteTable** parancsmag eltávolítja az Azure Route-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ca981-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="ca981-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca981-107">EXAMPLES</span></span>

### <span data-ttu-id="ca981-108">1. példa: a Route Table eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ca981-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="ca981-109">Ez a parancs eltávolítja a RouteTable01 nevű útvonalkártya-táblázatot a ResourceGroup11 nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="ca981-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="ca981-110">A parancsmag a táblázat eltávolítása előtt kéri a megerősítés megerősítését.</span><span class="sxs-lookup"><span data-stu-id="ca981-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="ca981-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca981-111">PARAMETERS</span></span>

### <span data-ttu-id="ca981-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca981-112">-AsJob</span></span>
<span data-ttu-id="ca981-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ca981-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca981-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca981-114">-DefaultProfile</span></span>
<span data-ttu-id="ca981-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca981-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca981-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ca981-116">-Force</span></span>
<span data-ttu-id="ca981-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ca981-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca981-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca981-118">-Name</span></span>
<span data-ttu-id="ca981-119">A parancsmag által eltávolított útválasztási táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca981-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ca981-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca981-120">-PassThru</span></span>
<span data-ttu-id="ca981-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ca981-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca981-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ca981-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca981-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca981-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca981-124">Annak az erőforrás-csoportnak a neve, amely a parancsmag által eltávolított útválasztási táblát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ca981-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ca981-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca981-125">-Confirm</span></span>
<span data-ttu-id="ca981-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca981-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca981-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca981-127">-WhatIf</span></span>
<span data-ttu-id="ca981-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca981-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca981-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca981-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca981-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca981-130">CommonParameters</span></span>
<span data-ttu-id="ca981-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca981-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca981-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca981-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca981-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca981-133">INPUTS</span></span>

### <span data-ttu-id="ca981-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ca981-134">System.String</span></span>

## <span data-ttu-id="ca981-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca981-135">OUTPUTS</span></span>

### <span data-ttu-id="ca981-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca981-136">System.Boolean</span></span>

## <span data-ttu-id="ca981-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca981-137">NOTES</span></span>

## <span data-ttu-id="ca981-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca981-138">RELATED LINKS</span></span>

[<span data-ttu-id="ca981-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca981-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="ca981-140">Új – AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca981-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="ca981-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca981-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)

