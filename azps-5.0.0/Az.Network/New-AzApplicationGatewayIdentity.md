---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195386"
---
# <span data-ttu-id="e393e-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="e393e-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="e393e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e393e-102">SYNOPSIS</span></span>
<span data-ttu-id="e393e-103">Identitás-objektumot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e393e-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="e393e-104">Ez a hivatkozás a felhasználó által kiosztott identitásra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="e393e-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="e393e-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e393e-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e393e-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="e393e-106">DESCRIPTION</span></span>
<span data-ttu-id="e393e-107">A **New-AzApplicationGatewayIdentity** parancsmag egy alkalmazás-átjáró identitás-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e393e-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="e393e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e393e-108">EXAMPLES</span></span>

### <span data-ttu-id="e393e-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e393e-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="e393e-110">Ebben a példában egy felhasználó által kiosztott identitást hozunk létre, majd a hivatkozásokat az alkalmazás-átjáróval használt identitás objektumban.</span><span class="sxs-lookup"><span data-stu-id="e393e-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="e393e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e393e-111">PARAMETERS</span></span>

### <span data-ttu-id="e393e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e393e-112">-DefaultProfile</span></span>
<span data-ttu-id="e393e-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e393e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e393e-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="e393e-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="e393e-115">Az ResourceId hozzárendelendő felhasználó által hozzárendelt identitás.</span><span class="sxs-lookup"><span data-stu-id="e393e-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="e393e-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e393e-116">-Confirm</span></span>
<span data-ttu-id="e393e-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e393e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e393e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e393e-118">-WhatIf</span></span>
<span data-ttu-id="e393e-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e393e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e393e-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e393e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e393e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e393e-121">CommonParameters</span></span>
<span data-ttu-id="e393e-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e393e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e393e-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e393e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e393e-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e393e-124">INPUTS</span></span>

### <span data-ttu-id="e393e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e393e-125">System.String</span></span>

## <span data-ttu-id="e393e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e393e-126">OUTPUTS</span></span>

### <span data-ttu-id="e393e-127">Microsoft. Azure. commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e393e-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="e393e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e393e-128">NOTES</span></span>

## <span data-ttu-id="e393e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e393e-129">RELATED LINKS</span></span>