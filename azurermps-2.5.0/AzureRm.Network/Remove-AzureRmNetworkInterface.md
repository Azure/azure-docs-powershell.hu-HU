---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 955c5200b7c7b9716e096f1157f7179619ae4f5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848410"
---
# <span data-ttu-id="d7922-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7922-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="d7922-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7922-102">SYNOPSIS</span></span>
<span data-ttu-id="d7922-103">Eltávolít egy hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="d7922-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7922-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7922-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7922-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7922-105">DESCRIPTION</span></span>
<span data-ttu-id="d7922-106">A **Remove-AzureRmNetworkInterface** parancsmag eltávolítja az Azure-hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="d7922-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="d7922-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7922-107">EXAMPLES</span></span>

### <span data-ttu-id="d7922-108">1. példa: hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d7922-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="d7922-109">Ez a parancs eltávolítja a hálózati felület NetworkInterface1 az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="d7922-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d7922-110">Mivel az *erő* paraméter nem használható, a rendszer kérni fogja a felhasználót, hogy erősítse meg ezt a lépést.</span><span class="sxs-lookup"><span data-stu-id="d7922-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="d7922-111">2. példa: hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d7922-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="d7922-112">Ez a parancs eltávolítja az összes hálózati felületet az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="d7922-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d7922-113">Mivel az *erő* paramétert használja, a rendszer nem kéri a felhasználó megerősítését.</span><span class="sxs-lookup"><span data-stu-id="d7922-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="d7922-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7922-114">PARAMETERS</span></span>

### <span data-ttu-id="d7922-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7922-115">-AsJob</span></span>
<span data-ttu-id="d7922-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d7922-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7922-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7922-117">-DefaultProfile</span></span>
<span data-ttu-id="d7922-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7922-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7922-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d7922-119">-Force</span></span>
<span data-ttu-id="d7922-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d7922-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d7922-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7922-121">-Name</span></span>
<span data-ttu-id="d7922-122">Annak a hálózati kapcsolatnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d7922-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7922-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7922-123">-PassThru</span></span>
<span data-ttu-id="d7922-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d7922-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7922-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d7922-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7922-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7922-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7922-127">Annak a csoportnak a neve, amely a parancsmag által eltávolított hálózati felületet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d7922-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7922-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7922-128">-Confirm</span></span>
<span data-ttu-id="d7922-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7922-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7922-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7922-130">-WhatIf</span></span>
<span data-ttu-id="d7922-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7922-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7922-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7922-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7922-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7922-133">CommonParameters</span></span>
<span data-ttu-id="d7922-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7922-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7922-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7922-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7922-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7922-136">INPUTS</span></span>

## <span data-ttu-id="d7922-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7922-137">OUTPUTS</span></span>

## <span data-ttu-id="d7922-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7922-138">NOTES</span></span>

## <span data-ttu-id="d7922-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7922-139">RELATED LINKS</span></span>

[<span data-ttu-id="d7922-140">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7922-140">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="d7922-141">Új – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7922-141">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="d7922-142">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7922-142">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)

