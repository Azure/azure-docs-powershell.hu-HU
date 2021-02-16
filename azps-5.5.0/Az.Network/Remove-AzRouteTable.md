---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160691"
---
# <span data-ttu-id="89af0-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="89af0-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="89af0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89af0-102">SYNOPSIS</span></span>
<span data-ttu-id="89af0-103">Eltávolít egy útvonaltáblát.</span><span class="sxs-lookup"><span data-stu-id="89af0-103">Removes a route table.</span></span>

## <span data-ttu-id="89af0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89af0-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89af0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89af0-105">DESCRIPTION</span></span>
<span data-ttu-id="89af0-106">Az **Remove-AzRouteTable** parancsmag eltávolít egy Azure-útválasztási táblát.</span><span class="sxs-lookup"><span data-stu-id="89af0-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="89af0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89af0-107">EXAMPLES</span></span>

### <span data-ttu-id="89af0-108">1. példa: Útvonaltábla eltávolítása</span><span class="sxs-lookup"><span data-stu-id="89af0-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="89af0-109">Ez a parancs eltávolítja a RouteTable01 nevű útválasztási táblát az Erőforráscsoport11 nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="89af0-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="89af0-110">A parancsmag megerősítést kér, mielőtt eltávolítja a táblát.</span><span class="sxs-lookup"><span data-stu-id="89af0-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="89af0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89af0-111">PARAMETERS</span></span>

### <span data-ttu-id="89af0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89af0-112">-AsJob</span></span>
<span data-ttu-id="89af0-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="89af0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89af0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89af0-114">-DefaultProfile</span></span>
<span data-ttu-id="89af0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89af0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89af0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="89af0-116">-Force</span></span>
<span data-ttu-id="89af0-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="89af0-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89af0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="89af0-118">-Name</span></span>
<span data-ttu-id="89af0-119">Annak az útvonaltáblának a neve, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="89af0-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89af0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89af0-120">-PassThru</span></span>
<span data-ttu-id="89af0-121">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="89af0-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89af0-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="89af0-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="89af0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89af0-123">-ResourceGroupName</span></span>
<span data-ttu-id="89af0-124">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által eltávolított útvonaltáblát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="89af0-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89af0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89af0-125">-Confirm</span></span>
<span data-ttu-id="89af0-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="89af0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89af0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89af0-127">-WhatIf</span></span>
<span data-ttu-id="89af0-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="89af0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89af0-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89af0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89af0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89af0-130">CommonParameters</span></span>
<span data-ttu-id="89af0-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89af0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89af0-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89af0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89af0-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89af0-133">INPUTS</span></span>

### <span data-ttu-id="89af0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="89af0-134">System.String</span></span>

## <span data-ttu-id="89af0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89af0-135">OUTPUTS</span></span>

### <span data-ttu-id="89af0-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89af0-136">System.Boolean</span></span>

## <span data-ttu-id="89af0-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89af0-137">NOTES</span></span>

## <span data-ttu-id="89af0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89af0-138">RELATED LINKS</span></span>

[<span data-ttu-id="89af0-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="89af0-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="89af0-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="89af0-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="89af0-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="89af0-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


