---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378683"
---
# <span data-ttu-id="1c5fe-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="1c5fe-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="1c5fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5fe-103">Frissíti az alkalmazás-átjáróhoz rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="1c5fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c5fe-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c5fe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c5fe-105">DESCRIPTION</span></span>
<span data-ttu-id="1c5fe-106">A **Set-AzApplicationGatewayIdentity** parancsmag frissíti az alkalmazás-átjáróhoz rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="1c5fe-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c5fe-107">EXAMPLES</span></span>

### <span data-ttu-id="1c5fe-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1c5fe-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="1c5fe-109">Ebben a példában egy felhasználóhoz rendelt identitást rendelünk egy meglévő alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="1c5fe-110">Megjegyzés: Ennek az identitásnak hozzáféréssel kell lennie ahhoz a kulcshoz, amelyből a tanúsítványokra/titkosságokra hivatkozni fog.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="1c5fe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c5fe-111">PARAMETERS</span></span>

### <span data-ttu-id="1c5fe-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c5fe-112">-ApplicationGateway</span></span>
<span data-ttu-id="1c5fe-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c5fe-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c5fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5fe-114">-DefaultProfile</span></span>
<span data-ttu-id="1c5fe-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c5fe-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="1c5fe-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="1c5fe-117">Az Alkalmazás átjáróhoz hozzárendelni rendelt felhasználó identitásának Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="1c5fe-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c5fe-118">-Confirm</span></span>
<span data-ttu-id="1c5fe-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c5fe-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c5fe-120">-WhatIf</span></span>
<span data-ttu-id="1c5fe-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c5fe-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c5fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5fe-123">CommonParameters</span></span>
<span data-ttu-id="1c5fe-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c5fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5fe-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c5fe-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5fe-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c5fe-126">INPUTS</span></span>

### <span data-ttu-id="1c5fe-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c5fe-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="1c5fe-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1c5fe-128">System.String</span></span>

## <span data-ttu-id="1c5fe-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c5fe-129">OUTPUTS</span></span>

### <span data-ttu-id="1c5fe-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c5fe-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1c5fe-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c5fe-131">NOTES</span></span>

## <span data-ttu-id="1c5fe-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c5fe-132">RELATED LINKS</span></span>
