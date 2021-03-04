---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: c8e0e5a3d503b4fa587f2a0bdb284b059bff4eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940106"
---
# <span data-ttu-id="246ba-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="246ba-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="246ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="246ba-102">SYNOPSIS</span></span>
<span data-ttu-id="246ba-103">Helyi hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="246ba-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="246ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="246ba-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="246ba-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="246ba-105">DESCRIPTION</span></span>
<span data-ttu-id="246ba-106">A helyi hálózati átjáró a virtuális magánhálózati eszköz helyszíni objektumának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="246ba-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="246ba-107">A **Remove-AzLocalNetworkGateway** parancsmag a név és az erőforráscsoport neve alapján törli a helyi átjárót képviselő objektumot.</span><span class="sxs-lookup"><span data-stu-id="246ba-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="246ba-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="246ba-108">EXAMPLES</span></span>

### <span data-ttu-id="246ba-109">1. példa: Helyi hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="246ba-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="246ba-110">Törli a helyi hálózati átjáró "myLocalGW" nevű objektumát a "myRG" erőforráscsoportban. A **Remove-AzVirtualNetworkGatewayConnection** parancsmaggal először törölnie kell a helyi hálózati átjáróval létesített összes kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="246ba-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="246ba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="246ba-111">PARAMETERS</span></span>

### <span data-ttu-id="246ba-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="246ba-112">-AsJob</span></span>
<span data-ttu-id="246ba-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="246ba-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="246ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246ba-114">-DefaultProfile</span></span>
<span data-ttu-id="246ba-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="246ba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="246ba-116">-Force</span><span class="sxs-lookup"><span data-stu-id="246ba-116">-Force</span></span>
<span data-ttu-id="246ba-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="246ba-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="246ba-118">-Name</span><span class="sxs-lookup"><span data-stu-id="246ba-118">-Name</span></span>
<span data-ttu-id="246ba-119">Annak a helyi hálózati átjárónak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="246ba-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="246ba-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="246ba-120">-PassThru</span></span>
<span data-ttu-id="246ba-121">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="246ba-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="246ba-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="246ba-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="246ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="246ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="246ba-124">A helyi hálózati átjárót tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="246ba-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="246ba-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="246ba-125">-Confirm</span></span>
<span data-ttu-id="246ba-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="246ba-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="246ba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="246ba-127">-WhatIf</span></span>
<span data-ttu-id="246ba-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="246ba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="246ba-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="246ba-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="246ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246ba-130">CommonParameters</span></span>
<span data-ttu-id="246ba-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="246ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246ba-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="246ba-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246ba-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="246ba-133">INPUTS</span></span>

### <span data-ttu-id="246ba-134">System.String</span><span class="sxs-lookup"><span data-stu-id="246ba-134">System.String</span></span>

## <span data-ttu-id="246ba-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="246ba-135">OUTPUTS</span></span>

### <span data-ttu-id="246ba-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="246ba-136">System.Boolean</span></span>

## <span data-ttu-id="246ba-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="246ba-137">NOTES</span></span>

## <span data-ttu-id="246ba-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="246ba-138">RELATED LINKS</span></span>

[<span data-ttu-id="246ba-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="246ba-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="246ba-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="246ba-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="246ba-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="246ba-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
