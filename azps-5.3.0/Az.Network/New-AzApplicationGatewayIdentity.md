---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385558"
---
# <span data-ttu-id="f6307-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="f6307-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="f6307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6307-102">SYNOPSIS</span></span>
<span data-ttu-id="f6307-103">Identitásobjektumot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="f6307-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="f6307-104">Ez a felhasználóhoz rendelt identitásra fog hivatkozni.</span><span class="sxs-lookup"><span data-stu-id="f6307-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="f6307-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6307-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6307-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6307-106">DESCRIPTION</span></span>
<span data-ttu-id="f6307-107">**A New-AzApplicationGatewayIdentity** parancsmag létrehoz egy alkalmazás-átjáró identitásobjektumát.</span><span class="sxs-lookup"><span data-stu-id="f6307-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="f6307-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6307-108">EXAMPLES</span></span>

### <span data-ttu-id="f6307-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="f6307-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="f6307-110">Ebben a példában létrehozunk egy felhasználóhoz rendelt identitást, majd hivatkozunk rá az Alkalmazás átjáróval használt identitásobjektumban.</span><span class="sxs-lookup"><span data-stu-id="f6307-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="f6307-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6307-111">PARAMETERS</span></span>

### <span data-ttu-id="f6307-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6307-112">-DefaultProfile</span></span>
<span data-ttu-id="f6307-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6307-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6307-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="f6307-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="f6307-115">Az Alkalmazás átjáróhoz hozzárendelni rendelt felhasználó identitásának Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="f6307-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="f6307-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6307-116">-Confirm</span></span>
<span data-ttu-id="f6307-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f6307-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6307-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6307-118">-WhatIf</span></span>
<span data-ttu-id="f6307-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f6307-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6307-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6307-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6307-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6307-121">CommonParameters</span></span>
<span data-ttu-id="f6307-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6307-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6307-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6307-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6307-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6307-124">INPUTS</span></span>

### <span data-ttu-id="f6307-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f6307-125">System.String</span></span>

## <span data-ttu-id="f6307-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6307-126">OUTPUTS</span></span>

### <span data-ttu-id="f6307-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f6307-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="f6307-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6307-128">NOTES</span></span>

## <span data-ttu-id="f6307-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6307-129">RELATED LINKS</span></span>
