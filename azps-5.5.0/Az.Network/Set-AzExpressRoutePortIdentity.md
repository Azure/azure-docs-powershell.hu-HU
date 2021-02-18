---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206510"
---
# <span data-ttu-id="446ed-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="446ed-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="446ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="446ed-102">SYNOPSIS</span></span>
<span data-ttu-id="446ed-103">Frissíti az ExpressRoutePorthoz rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="446ed-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="446ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="446ed-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="446ed-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="446ed-105">DESCRIPTION</span></span>
<span data-ttu-id="446ed-106">A **Set-AzExpressRoutePortIdentity** parancsmag frissíti a helyi Azure ExpressRoutePort-objektumot.</span><span class="sxs-lookup"><span data-stu-id="446ed-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="446ed-107">A **Set-AzExpressRoutePort segítségével** rendelje hozzá az ExpressRoutePorthoz.</span><span class="sxs-lookup"><span data-stu-id="446ed-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="446ed-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="446ed-108">EXAMPLES</span></span>

### <span data-ttu-id="446ed-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="446ed-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="446ed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="446ed-110">PARAMETERS</span></span>

### <span data-ttu-id="446ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="446ed-111">-DefaultProfile</span></span>
<span data-ttu-id="446ed-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="446ed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="446ed-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="446ed-113">-ExpressRoutePort</span></span>
<span data-ttu-id="446ed-114">Az ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="446ed-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="446ed-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="446ed-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="446ed-116">Az ExpressRoutePort-hoz hozzárendelni szükséges felhasználó által hozzárendelt identitás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="446ed-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="446ed-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="446ed-117">-Confirm</span></span>
<span data-ttu-id="446ed-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="446ed-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="446ed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="446ed-119">-WhatIf</span></span>
<span data-ttu-id="446ed-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="446ed-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="446ed-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="446ed-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="446ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="446ed-122">CommonParameters</span></span>
<span data-ttu-id="446ed-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="446ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="446ed-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="446ed-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="446ed-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="446ed-125">INPUTS</span></span>

### <span data-ttu-id="446ed-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="446ed-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="446ed-127">System.String</span><span class="sxs-lookup"><span data-stu-id="446ed-127">System.String</span></span>

## <span data-ttu-id="446ed-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="446ed-128">OUTPUTS</span></span>

### <span data-ttu-id="446ed-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="446ed-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="446ed-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="446ed-130">NOTES</span></span>

## <span data-ttu-id="446ed-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="446ed-131">RELATED LINKS</span></span>
[<span data-ttu-id="446ed-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="446ed-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="446ed-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="446ed-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="446ed-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="446ed-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
