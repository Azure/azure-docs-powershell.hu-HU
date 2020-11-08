---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194254"
---
# <span data-ttu-id="17bbe-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="17bbe-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="17bbe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="17bbe-103">Azure-ExpressRoutePortIdentity hoz létre.</span><span class="sxs-lookup"><span data-stu-id="17bbe-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="17bbe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17bbe-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17bbe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17bbe-105">DESCRIPTION</span></span>
<span data-ttu-id="17bbe-106">A **New-AzExpressRoutePortIdentity** parancsmag létrehoz egy helyi Azure ExpressRoutePort-identitás objektumát.</span><span class="sxs-lookup"><span data-stu-id="17bbe-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="17bbe-107">A **New-AzExpressRoutePort** vagy a **set-AzExpressRoutePort** segítségével az Azure ExpressRoutePort rendelhető hozzá.</span><span class="sxs-lookup"><span data-stu-id="17bbe-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="17bbe-108">Példák</span><span class="sxs-lookup"><span data-stu-id="17bbe-108">EXAMPLES</span></span>

### <span data-ttu-id="17bbe-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="17bbe-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="17bbe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17bbe-110">PARAMETERS</span></span>

### <span data-ttu-id="17bbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bbe-111">-DefaultProfile</span></span>
<span data-ttu-id="17bbe-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17bbe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17bbe-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="17bbe-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="17bbe-114">A ExpressRoutePort-fiókhoz hozzárendelt ResourceId-azonosító.</span><span class="sxs-lookup"><span data-stu-id="17bbe-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="17bbe-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17bbe-115">-Confirm</span></span>
<span data-ttu-id="17bbe-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17bbe-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17bbe-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17bbe-117">-WhatIf</span></span>
<span data-ttu-id="17bbe-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17bbe-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17bbe-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17bbe-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17bbe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bbe-120">CommonParameters</span></span>
<span data-ttu-id="17bbe-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17bbe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bbe-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17bbe-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bbe-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17bbe-123">INPUTS</span></span>

### <span data-ttu-id="17bbe-124">System. String</span><span class="sxs-lookup"><span data-stu-id="17bbe-124">System.String</span></span>

## <span data-ttu-id="17bbe-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17bbe-125">OUTPUTS</span></span>

### <span data-ttu-id="17bbe-126">Microsoft. Azure. commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="17bbe-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="17bbe-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17bbe-127">NOTES</span></span>

## <span data-ttu-id="17bbe-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17bbe-128">RELATED LINKS</span></span>
[<span data-ttu-id="17bbe-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="17bbe-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="17bbe-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="17bbe-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="17bbe-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="17bbe-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)