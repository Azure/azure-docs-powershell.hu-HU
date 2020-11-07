---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 61cae1140ef0c46eee5857c15d0b6032a65caeb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837848"
---
# <span data-ttu-id="53105-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53105-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="53105-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53105-102">SYNOPSIS</span></span>
<span data-ttu-id="53105-103">Eltávolít egy hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="53105-103">Removes a network interface.</span></span>

## <span data-ttu-id="53105-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53105-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53105-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="53105-105">DESCRIPTION</span></span>
<span data-ttu-id="53105-106">A **Remove-AzNetworkInterface** parancsmag eltávolítja az Azure-hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="53105-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="53105-107">Példák</span><span class="sxs-lookup"><span data-stu-id="53105-107">EXAMPLES</span></span>

### <span data-ttu-id="53105-108">1. példa: hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="53105-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="53105-109">Ez a parancs eltávolítja a hálózati felület NetworkInterface1 az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="53105-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="53105-110">Mivel az *erő* paraméter nem használható, a rendszer kérni fogja a felhasználót, hogy erősítse meg ezt a lépést.</span><span class="sxs-lookup"><span data-stu-id="53105-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="53105-111">2. példa: hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="53105-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="53105-112">Ez a parancs eltávolítja az összes hálózati felületet az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="53105-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="53105-113">Mivel az *erő* paramétert használja, a rendszer nem kéri a felhasználó megerősítését.</span><span class="sxs-lookup"><span data-stu-id="53105-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="53105-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53105-114">PARAMETERS</span></span>

### <span data-ttu-id="53105-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53105-115">-AsJob</span></span>
<span data-ttu-id="53105-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="53105-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53105-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53105-117">-DefaultProfile</span></span>
<span data-ttu-id="53105-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53105-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53105-119">-Force</span><span class="sxs-lookup"><span data-stu-id="53105-119">-Force</span></span>
<span data-ttu-id="53105-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="53105-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53105-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53105-121">-Name</span></span>
<span data-ttu-id="53105-122">Annak a hálózati kapcsolatnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="53105-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="53105-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53105-123">-PassThru</span></span>
<span data-ttu-id="53105-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="53105-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="53105-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="53105-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="53105-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53105-126">-ResourceGroupName</span></span>
<span data-ttu-id="53105-127">Annak a csoportnak a neve, amely a parancsmag által eltávolított hálózati felületet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="53105-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="53105-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53105-128">-Confirm</span></span>
<span data-ttu-id="53105-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53105-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53105-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53105-130">-WhatIf</span></span>
<span data-ttu-id="53105-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53105-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53105-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53105-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53105-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53105-133">CommonParameters</span></span>
<span data-ttu-id="53105-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53105-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53105-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53105-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53105-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53105-136">INPUTS</span></span>

### <span data-ttu-id="53105-137">System. String</span><span class="sxs-lookup"><span data-stu-id="53105-137">System.String</span></span>

## <span data-ttu-id="53105-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53105-138">OUTPUTS</span></span>

### <span data-ttu-id="53105-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53105-139">System.Boolean</span></span>

## <span data-ttu-id="53105-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53105-140">NOTES</span></span>

## <span data-ttu-id="53105-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53105-141">RELATED LINKS</span></span>

[<span data-ttu-id="53105-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53105-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="53105-143">Új – AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53105-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="53105-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53105-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


