---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: e3b3b0a0990f8c72fcd18d8828ae97d5c1a8a5aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015045"
---
# <span data-ttu-id="ba93f-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ba93f-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="ba93f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba93f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba93f-103">Létrehoz egy Azure ExpressRoutePortIdentity-t.</span><span class="sxs-lookup"><span data-stu-id="ba93f-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="ba93f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba93f-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba93f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba93f-105">DESCRIPTION</span></span>
<span data-ttu-id="ba93f-106">A **New-AzExpressRoutePortIdentity** parancsmag helyi Azure ExpressRoutePort-identitásobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ba93f-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="ba93f-107">A **New-AzExpressRoutePort** vagy a **Set-AzExpressRoutePort** segítségével rendelje hozzá az Azure ExpressRoutePorthoz.</span><span class="sxs-lookup"><span data-stu-id="ba93f-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="ba93f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba93f-108">EXAMPLES</span></span>

### <span data-ttu-id="ba93f-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="ba93f-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="ba93f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba93f-110">PARAMETERS</span></span>

### <span data-ttu-id="ba93f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba93f-111">-DefaultProfile</span></span>
<span data-ttu-id="ba93f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba93f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba93f-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="ba93f-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="ba93f-114">Az ExpressRoutePorthoz hozzárendelni szükséges felhasználó által hozzárendelt identitás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="ba93f-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="ba93f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba93f-115">-Confirm</span></span>
<span data-ttu-id="ba93f-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ba93f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba93f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba93f-117">-WhatIf</span></span>
<span data-ttu-id="ba93f-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ba93f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba93f-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba93f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba93f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba93f-120">CommonParameters</span></span>
<span data-ttu-id="ba93f-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba93f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba93f-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba93f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba93f-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba93f-123">INPUTS</span></span>

### <span data-ttu-id="ba93f-124">System.String</span><span class="sxs-lookup"><span data-stu-id="ba93f-124">System.String</span></span>

## <span data-ttu-id="ba93f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba93f-125">OUTPUTS</span></span>

### <span data-ttu-id="ba93f-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="ba93f-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="ba93f-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba93f-127">NOTES</span></span>

## <span data-ttu-id="ba93f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba93f-128">RELATED LINKS</span></span>
[<span data-ttu-id="ba93f-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ba93f-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="ba93f-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ba93f-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="ba93f-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ba93f-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)