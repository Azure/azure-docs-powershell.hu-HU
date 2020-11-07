---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: b51aac195a6f0f4870b89894cce8f26c732077ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837216"
---
# <span data-ttu-id="133b5-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="133b5-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="133b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="133b5-102">SYNOPSIS</span></span>
<span data-ttu-id="133b5-103">Azure-ExpressRoutePortIdentity hoz létre.</span><span class="sxs-lookup"><span data-stu-id="133b5-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="133b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="133b5-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="133b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="133b5-105">DESCRIPTION</span></span>
<span data-ttu-id="133b5-106">A **New-AzExpressRoutePortIdentity** parancsmag létrehoz egy helyi Azure ExpressRoutePort-identitás objektumát.</span><span class="sxs-lookup"><span data-stu-id="133b5-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="133b5-107">A **New-AzExpressRoutePort** vagy a **set-AzExpressRoutePort** segítségével az Azure ExpressRoutePort rendelhető hozzá.</span><span class="sxs-lookup"><span data-stu-id="133b5-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="133b5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="133b5-108">EXAMPLES</span></span>

### <span data-ttu-id="133b5-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="133b5-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="133b5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="133b5-110">PARAMETERS</span></span>

### <span data-ttu-id="133b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133b5-111">-DefaultProfile</span></span>
<span data-ttu-id="133b5-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="133b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="133b5-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="133b5-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="133b5-114">A ExpressRoutePort-fiókhoz hozzárendelt ResourceId-azonosító.</span><span class="sxs-lookup"><span data-stu-id="133b5-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="133b5-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="133b5-115">-Confirm</span></span>
<span data-ttu-id="133b5-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="133b5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="133b5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="133b5-117">-WhatIf</span></span>
<span data-ttu-id="133b5-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="133b5-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="133b5-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="133b5-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="133b5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133b5-120">CommonParameters</span></span>
<span data-ttu-id="133b5-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="133b5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133b5-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="133b5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133b5-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="133b5-123">INPUTS</span></span>

### <span data-ttu-id="133b5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="133b5-124">System.String</span></span>

## <span data-ttu-id="133b5-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="133b5-125">OUTPUTS</span></span>

### <span data-ttu-id="133b5-126">Microsoft. Azure. commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="133b5-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="133b5-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="133b5-127">NOTES</span></span>

## <span data-ttu-id="133b5-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="133b5-128">RELATED LINKS</span></span>
[<span data-ttu-id="133b5-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="133b5-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="133b5-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="133b5-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="133b5-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="133b5-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)