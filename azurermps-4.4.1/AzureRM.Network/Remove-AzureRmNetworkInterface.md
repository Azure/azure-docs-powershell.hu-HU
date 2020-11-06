---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 3250aa7f9108436cadbf0f46ab0e36d3a9c094d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492462"
---
# <span data-ttu-id="1f1b1-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1f1b1-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="1f1b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="1f1b1-103">Eltávolít egy hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f1b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f1b1-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f1b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f1b1-105">DESCRIPTION</span></span>
<span data-ttu-id="1f1b1-106">A **Remove-AzureRmNetworkInterface** parancsmag eltávolítja az Azure-hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="1f1b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1f1b1-107">EXAMPLES</span></span>

### <span data-ttu-id="1f1b1-108">1. példa: hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1f1b1-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="1f1b1-109">Ez a parancs eltávolítja a hálózati felület NetworkInterface1 az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="1f1b1-110">Mivel az *erő* paraméter nem használható, a rendszer kérni fogja a felhasználót, hogy erősítse meg ezt a lépést.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="1f1b1-111">2. példa: hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1f1b1-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="1f1b1-112">Ez a parancs eltávolítja az összes hálózati felületet az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="1f1b1-113">Mivel az *erő* paramétert használja, a rendszer nem kéri a felhasználó megerősítését.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="1f1b1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f1b1-114">PARAMETERS</span></span>

### <span data-ttu-id="1f1b1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1f1b1-115">-Force</span></span>
<span data-ttu-id="1f1b1-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f1b1-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f1b1-117">-Name</span></span>
<span data-ttu-id="1f1b1-118">Annak a hálózati kapcsolatnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-118">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1f1b1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f1b1-119">-PassThru</span></span>
<span data-ttu-id="1f1b1-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f1b1-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f1b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f1b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f1b1-123">Annak a csoportnak a neve, amely a parancsmag által eltávolított hálózati felületet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-123">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1f1b1-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f1b1-124">-Confirm</span></span>
<span data-ttu-id="1f1b1-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f1b1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f1b1-126">-WhatIf</span></span>
<span data-ttu-id="1f1b1-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f1b1-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f1b1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f1b1-129">-DefaultProfile</span></span>
<span data-ttu-id="1f1b1-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f1b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f1b1-131">CommonParameters</span></span>
<span data-ttu-id="1f1b1-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f1b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f1b1-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f1b1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f1b1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f1b1-134">INPUTS</span></span>

## <span data-ttu-id="1f1b1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f1b1-135">OUTPUTS</span></span>

## <span data-ttu-id="1f1b1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f1b1-136">NOTES</span></span>

## <span data-ttu-id="1f1b1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f1b1-137">RELATED LINKS</span></span>

[<span data-ttu-id="1f1b1-138">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1f1b1-138">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="1f1b1-139">Új – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1f1b1-139">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="1f1b1-140">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1f1b1-140">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


