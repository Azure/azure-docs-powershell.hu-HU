---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187252"
---
# <span data-ttu-id="dbe60-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbe60-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="dbe60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbe60-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe60-103">Egy hálózati biztonsági csoport eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="dbe60-103">Removes a network security group.</span></span>

## <span data-ttu-id="dbe60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbe60-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbe60-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbe60-105">DESCRIPTION</span></span>
<span data-ttu-id="dbe60-106">A **Remove-AzNetworkSecurityGroup** parancsmag eltávolítja az Azure hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="dbe60-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="dbe60-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dbe60-107">EXAMPLES</span></span>

### <span data-ttu-id="dbe60-108">1. példa: hálózati biztonsági csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dbe60-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="dbe60-109">Ez a parancs eltávolítja a NSG-FrontEnd nevű biztonsági csoportot a TestRG nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="dbe60-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="dbe60-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbe60-110">PARAMETERS</span></span>

### <span data-ttu-id="dbe60-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbe60-111">-AsJob</span></span>
<span data-ttu-id="dbe60-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dbe60-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbe60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe60-113">-DefaultProfile</span></span>
<span data-ttu-id="dbe60-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbe60-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbe60-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dbe60-115">-Force</span></span>
<span data-ttu-id="dbe60-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="dbe60-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dbe60-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbe60-117">-Name</span></span>
<span data-ttu-id="dbe60-118">A parancsmag által eltávolított hálózati biztonsági csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbe60-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dbe60-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbe60-119">-PassThru</span></span>
<span data-ttu-id="dbe60-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="dbe60-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dbe60-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="dbe60-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dbe60-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbe60-122">-ResourceGroupName</span></span>
<span data-ttu-id="dbe60-123">Annak a csoportnak a nevét adja meg, amelyre a parancsmag eltávolítja a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="dbe60-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="dbe60-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dbe60-124">-Confirm</span></span>
<span data-ttu-id="dbe60-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dbe60-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbe60-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbe60-126">-WhatIf</span></span>
<span data-ttu-id="dbe60-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dbe60-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbe60-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dbe60-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbe60-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe60-129">CommonParameters</span></span>
<span data-ttu-id="dbe60-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbe60-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe60-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe60-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe60-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbe60-132">INPUTS</span></span>

### <span data-ttu-id="dbe60-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dbe60-133">System.String</span></span>

## <span data-ttu-id="dbe60-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbe60-134">OUTPUTS</span></span>

### <span data-ttu-id="dbe60-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbe60-135">System.Boolean</span></span>

## <span data-ttu-id="dbe60-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbe60-136">NOTES</span></span>

## <span data-ttu-id="dbe60-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbe60-137">RELATED LINKS</span></span>

[<span data-ttu-id="dbe60-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbe60-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dbe60-139">Új – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbe60-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dbe60-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbe60-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)

