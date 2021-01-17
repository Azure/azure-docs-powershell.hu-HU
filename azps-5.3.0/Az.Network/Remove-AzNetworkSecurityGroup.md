---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468858"
---
# <span data-ttu-id="5a6f8-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a6f8-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="5a6f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a6f8-102">SYNOPSIS</span></span>
<span data-ttu-id="5a6f8-103">Eltávolít egy hálózati biztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-103">Removes a network security group.</span></span>

## <span data-ttu-id="5a6f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a6f8-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a6f8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a6f8-105">DESCRIPTION</span></span>
<span data-ttu-id="5a6f8-106">A **Remove-AzNetworkSecurityGroup** parancsmag eltávolít egy Azure-hálózati biztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="5a6f8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a6f8-107">EXAMPLES</span></span>

### <span data-ttu-id="5a6f8-108">1. példa: Hálózati biztonsági csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5a6f8-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="5a6f8-109">Ez a parancs eltávolítja a TestRG nevű NSG-FrontEnd nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="5a6f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a6f8-110">PARAMETERS</span></span>

### <span data-ttu-id="5a6f8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a6f8-111">-AsJob</span></span>
<span data-ttu-id="5a6f8-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5a6f8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a6f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a6f8-113">-DefaultProfile</span></span>
<span data-ttu-id="5a6f8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a6f8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5a6f8-115">-Force</span></span>
<span data-ttu-id="5a6f8-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a6f8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5a6f8-117">-Name</span></span>
<span data-ttu-id="5a6f8-118">Annak a hálózati biztonsági csoportnak a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5a6f8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a6f8-119">-PassThru</span></span>
<span data-ttu-id="5a6f8-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a6f8-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5a6f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a6f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a6f8-123">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag eltávolít egy hálózati biztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="5a6f8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a6f8-124">-Confirm</span></span>
<span data-ttu-id="5a6f8-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a6f8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a6f8-126">-WhatIf</span></span>
<span data-ttu-id="5a6f8-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a6f8-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a6f8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6f8-129">CommonParameters</span></span>
<span data-ttu-id="5a6f8-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a6f8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6f8-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a6f8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6f8-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a6f8-132">INPUTS</span></span>

### <span data-ttu-id="5a6f8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5a6f8-133">System.String</span></span>

## <span data-ttu-id="5a6f8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a6f8-134">OUTPUTS</span></span>

### <span data-ttu-id="5a6f8-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a6f8-135">System.Boolean</span></span>

## <span data-ttu-id="5a6f8-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a6f8-136">NOTES</span></span>

## <span data-ttu-id="5a6f8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a6f8-137">RELATED LINKS</span></span>

[<span data-ttu-id="5a6f8-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a6f8-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5a6f8-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a6f8-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5a6f8-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a6f8-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


