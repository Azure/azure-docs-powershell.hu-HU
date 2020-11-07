---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 403c41de0359f2d857d2c86b772e4af419640f2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841133"
---
# <span data-ttu-id="e541e-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e541e-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="e541e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e541e-102">SYNOPSIS</span></span>
<span data-ttu-id="e541e-103">Eltávolít egy hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="e541e-103">Removes a network interface.</span></span>

## <span data-ttu-id="e541e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e541e-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e541e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e541e-105">DESCRIPTION</span></span>
<span data-ttu-id="e541e-106">A **Remove-AzNetworkInterface** parancsmag eltávolítja az Azure-hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="e541e-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="e541e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e541e-107">EXAMPLES</span></span>

### <span data-ttu-id="e541e-108">1. példa: hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e541e-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="e541e-109">Ez a parancs eltávolítja a hálózati felület NetworkInterface1 az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="e541e-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="e541e-110">Mivel az *erő* paraméter nem használható, a rendszer kérni fogja a felhasználót, hogy erősítse meg ezt a lépést.</span><span class="sxs-lookup"><span data-stu-id="e541e-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="e541e-111">2. példa: hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e541e-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="e541e-112">Ez a parancs eltávolítja az összes hálózati felületet az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="e541e-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="e541e-113">Mivel az *erő* paramétert használja, a rendszer nem kéri a felhasználó megerősítését.</span><span class="sxs-lookup"><span data-stu-id="e541e-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="e541e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e541e-114">PARAMETERS</span></span>

### <span data-ttu-id="e541e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e541e-115">-AsJob</span></span>
<span data-ttu-id="e541e-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e541e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e541e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e541e-117">-DefaultProfile</span></span>
<span data-ttu-id="e541e-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e541e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e541e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e541e-119">-Force</span></span>
<span data-ttu-id="e541e-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e541e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e541e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e541e-121">-Name</span></span>
<span data-ttu-id="e541e-122">Annak a hálózati kapcsolatnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="e541e-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e541e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e541e-123">-PassThru</span></span>
<span data-ttu-id="e541e-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e541e-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e541e-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e541e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e541e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e541e-126">-ResourceGroupName</span></span>
<span data-ttu-id="e541e-127">Annak a csoportnak a neve, amely a parancsmag által eltávolított hálózati felületet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e541e-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e541e-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e541e-128">-Confirm</span></span>
<span data-ttu-id="e541e-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e541e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e541e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e541e-130">-WhatIf</span></span>
<span data-ttu-id="e541e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e541e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e541e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e541e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e541e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e541e-133">CommonParameters</span></span>
<span data-ttu-id="e541e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e541e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e541e-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e541e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e541e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e541e-136">INPUTS</span></span>

## <span data-ttu-id="e541e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e541e-137">OUTPUTS</span></span>

## <span data-ttu-id="e541e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e541e-138">NOTES</span></span>

## <span data-ttu-id="e541e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e541e-139">RELATED LINKS</span></span>

[<span data-ttu-id="e541e-140">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e541e-140">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="e541e-141">Új – AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e541e-141">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="e541e-142">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e541e-142">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


