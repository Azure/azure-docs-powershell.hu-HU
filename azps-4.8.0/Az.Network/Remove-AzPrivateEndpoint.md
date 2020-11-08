---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172893"
---
# <span data-ttu-id="3cf1b-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cf1b-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="3cf1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3cf1b-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf1b-103">Privát végpont eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="3cf1b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3cf1b-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf1b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3cf1b-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf1b-106">A **Remove-AzPrivateEndpoint** parancsmag eltávolítja a privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="3cf1b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3cf1b-107">EXAMPLES</span></span>

### <span data-ttu-id="3cf1b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3cf1b-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="3cf1b-109">Ez a példa eltávolítja a MyPrivateEndpoint1 nevű privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="3cf1b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3cf1b-110">PARAMETERS</span></span>

### <span data-ttu-id="3cf1b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cf1b-111">-AsJob</span></span>
<span data-ttu-id="3cf1b-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3cf1b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cf1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf1b-113">-DefaultProfile</span></span>
<span data-ttu-id="3cf1b-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf1b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3cf1b-115">-Force</span></span>
<span data-ttu-id="3cf1b-116">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="3cf1b-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="3cf1b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3cf1b-117">-Name</span></span>
<span data-ttu-id="3cf1b-118">A privát végpont neve.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="3cf1b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cf1b-119">-PassThru</span></span>
<span data-ttu-id="3cf1b-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3cf1b-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3cf1b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf1b-122">-ResourceGroupName</span></span>
<span data-ttu-id="3cf1b-123">A privát végpont erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="3cf1b-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3cf1b-124">-Confirm</span></span>
<span data-ttu-id="3cf1b-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf1b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf1b-126">-WhatIf</span></span>
<span data-ttu-id="3cf1b-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf1b-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf1b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf1b-129">CommonParameters</span></span>
<span data-ttu-id="3cf1b-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3cf1b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf1b-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf1b-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cf1b-132">INPUTS</span></span>

### <span data-ttu-id="3cf1b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf1b-133">System.String</span></span>

## <span data-ttu-id="3cf1b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cf1b-134">OUTPUTS</span></span>

### <span data-ttu-id="3cf1b-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cf1b-135">System.Boolean</span></span>

## <span data-ttu-id="3cf1b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3cf1b-136">NOTES</span></span>

## <span data-ttu-id="3cf1b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cf1b-137">RELATED LINKS</span></span>

[<span data-ttu-id="3cf1b-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cf1b-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="3cf1b-139">Új – AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cf1b-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)