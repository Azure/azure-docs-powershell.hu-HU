---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 32709a1a0280604b784c9f094478858f8c4bc4ab
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848726"
---
# <span data-ttu-id="a6d3d-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a6d3d-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="a6d3d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d3d-103">Egy hálózati biztonsági csoport eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6d3d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6d3d-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6d3d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d3d-106">A **Remove-AzureRmNetworkSecurityGroup** parancsmag eltávolítja az Azure hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="a6d3d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a6d3d-107">EXAMPLES</span></span>

### <span data-ttu-id="a6d3d-108">1. példa: hálózati biztonsági csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a6d3d-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="a6d3d-109">Ez a parancs eltávolítja a NSG-FrontEnd nevű biztonsági csoportot a TestRG nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="a6d3d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6d3d-110">PARAMETERS</span></span>

### <span data-ttu-id="a6d3d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6d3d-111">-AsJob</span></span>
<span data-ttu-id="a6d3d-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a6d3d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6d3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d3d-113">-DefaultProfile</span></span>
<span data-ttu-id="a6d3d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6d3d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a6d3d-115">-Force</span></span>
<span data-ttu-id="a6d3d-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a6d3d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6d3d-117">-Name</span></span>
<span data-ttu-id="a6d3d-118">A parancsmag által eltávolított hálózati biztonsági csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6d3d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6d3d-119">-PassThru</span></span>
<span data-ttu-id="a6d3d-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a6d3d-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a6d3d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6d3d-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6d3d-123">Annak a csoportnak a nevét adja meg, amelyre a parancsmag eltávolítja a hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="a6d3d-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a6d3d-124">-Confirm</span></span>
<span data-ttu-id="a6d3d-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6d3d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6d3d-126">-WhatIf</span></span>
<span data-ttu-id="a6d3d-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6d3d-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6d3d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6d3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d3d-129">CommonParameters</span></span>
<span data-ttu-id="a6d3d-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6d3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d3d-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d3d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d3d-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6d3d-132">INPUTS</span></span>

## <span data-ttu-id="a6d3d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6d3d-133">OUTPUTS</span></span>

## <span data-ttu-id="a6d3d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6d3d-134">NOTES</span></span>

## <span data-ttu-id="a6d3d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6d3d-135">RELATED LINKS</span></span>

[<span data-ttu-id="a6d3d-136">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a6d3d-136">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="a6d3d-137">Új – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a6d3d-137">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="a6d3d-138">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a6d3d-138">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


