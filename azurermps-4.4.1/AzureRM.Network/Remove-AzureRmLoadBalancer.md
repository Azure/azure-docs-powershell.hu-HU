---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 6757c9c0b9eeb0b3408a07713c62812d361d814a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504824"
---
# <span data-ttu-id="3f1a8-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f1a8-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="3f1a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1a8-103">A terheléselosztó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f1a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f1a8-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f1a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f1a8-105">DESCRIPTION</span></span>
<span data-ttu-id="3f1a8-106">A **Remove-AzureRmLoadBalancer** parancsmag eltávolítja az Azure terheléselosztó bővítményt.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="3f1a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3f1a8-107">EXAMPLES</span></span>

### <span data-ttu-id="3f1a8-108">1. példa: terheléselosztó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3f1a8-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="3f1a8-109">Ez a parancs törli a MyLoadBalancer nevű terheléselosztó nevű MyResourceGroup a nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="3f1a8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f1a8-110">PARAMETERS</span></span>

### <span data-ttu-id="3f1a8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3f1a8-111">-Force</span></span>
<span data-ttu-id="3f1a8-112">Azt jelzi, hogy ez a parancsmag eltávolítja a terheléselosztást függetlenül attól, hogy az erőforrásokat rendelte-e hozzá.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-112">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f1a8-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f1a8-113">-Name</span></span>
<span data-ttu-id="3f1a8-114">Az eltávolítandó terheléselosztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-114">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="3f1a8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f1a8-115">-PassThru</span></span>
<span data-ttu-id="3f1a8-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f1a8-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f1a8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1a8-118">-ResourceGroupName</span></span>
<span data-ttu-id="3f1a8-119">Annak a csoportnak a nevét adja meg, amely az eltávolítandó terheléselosztót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-119">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="3f1a8-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f1a8-120">-Confirm</span></span>
<span data-ttu-id="3f1a8-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f1a8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f1a8-122">-WhatIf</span></span>
<span data-ttu-id="3f1a8-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f1a8-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f1a8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1a8-125">-DefaultProfile</span></span>
<span data-ttu-id="3f1a8-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f1a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1a8-127">CommonParameters</span></span>
<span data-ttu-id="3f1a8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f1a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1a8-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f1a8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1a8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f1a8-130">INPUTS</span></span>

## <span data-ttu-id="3f1a8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f1a8-131">OUTPUTS</span></span>

## <span data-ttu-id="3f1a8-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f1a8-132">NOTES</span></span>

## <span data-ttu-id="3f1a8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f1a8-133">RELATED LINKS</span></span>

[<span data-ttu-id="3f1a8-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f1a8-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="3f1a8-135">Új – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f1a8-135">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="3f1a8-136">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f1a8-136">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


