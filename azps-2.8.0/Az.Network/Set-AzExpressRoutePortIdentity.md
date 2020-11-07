---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 330264eaaffd9d81da2ed8dbcc7c892477ffb7e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837784"
---
# <span data-ttu-id="fe19d-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fe19d-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="fe19d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe19d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe19d-103">Egy ExpressRoutePort rendelt identitás frissítése</span><span class="sxs-lookup"><span data-stu-id="fe19d-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="fe19d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe19d-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe19d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe19d-105">DESCRIPTION</span></span>
<span data-ttu-id="fe19d-106">A **set-AzExpressRoutePortIdentity** parancsmag frissíti egy helyi Azure ExpressRoutePort-objektumot.</span><span class="sxs-lookup"><span data-stu-id="fe19d-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="fe19d-107">A **set-AzExpressRoutePort** használatával társíthatja a ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="fe19d-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="fe19d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fe19d-108">EXAMPLES</span></span>

### <span data-ttu-id="fe19d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fe19d-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="fe19d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe19d-110">PARAMETERS</span></span>

### <span data-ttu-id="fe19d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe19d-111">-DefaultProfile</span></span>
<span data-ttu-id="fe19d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe19d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe19d-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fe19d-113">-ExpressRoutePort</span></span>
<span data-ttu-id="fe19d-114">A ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fe19d-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe19d-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="fe19d-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="fe19d-116">A ExpressRoutePort-fiókhoz hozzárendelt ResourceId-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fe19d-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe19d-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe19d-117">-Confirm</span></span>
<span data-ttu-id="fe19d-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe19d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe19d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe19d-119">-WhatIf</span></span>
<span data-ttu-id="fe19d-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe19d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe19d-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe19d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe19d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe19d-122">CommonParameters</span></span>
<span data-ttu-id="fe19d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe19d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe19d-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe19d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe19d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe19d-125">INPUTS</span></span>

### <span data-ttu-id="fe19d-126">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fe19d-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="fe19d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fe19d-127">System.String</span></span>

## <span data-ttu-id="fe19d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe19d-128">OUTPUTS</span></span>

### <span data-ttu-id="fe19d-129">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fe19d-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="fe19d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe19d-130">NOTES</span></span>

## <span data-ttu-id="fe19d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe19d-131">RELATED LINKS</span></span>
[<span data-ttu-id="fe19d-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fe19d-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="fe19d-133">Új – AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fe19d-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="fe19d-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fe19d-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
