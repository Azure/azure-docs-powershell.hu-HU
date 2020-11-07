---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 83a44e97e01e846cec568227514177babd76d30a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670049"
---
# <span data-ttu-id="79543-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="79543-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="79543-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79543-102">SYNOPSIS</span></span>
<span data-ttu-id="79543-103">Az alkalmazás-átjáróhoz rendelt identitás frissítése</span><span class="sxs-lookup"><span data-stu-id="79543-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="79543-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79543-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79543-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79543-105">DESCRIPTION</span></span>
<span data-ttu-id="79543-106">A **set-AzApplicationGatewayIdentity** parancsmag frissíti az Application Gateway-nek rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="79543-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="79543-107">Példák</span><span class="sxs-lookup"><span data-stu-id="79543-107">EXAMPLES</span></span>

### <span data-ttu-id="79543-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="79543-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="79543-109">Ebben a példában egy felhasználóhoz rendelt identitást rendel egy meglévő alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="79543-109">In this example, we assign a user assigned identity to an existing applicaiton gateway.</span></span>
<span data-ttu-id="79543-110">Megjegyzés: ennek az identitásnak hozzáférést kell biztosítani ahhoz a kulcshoz, amelyből a tanúsítványokat/titkokat hivatkozni kell.</span><span class="sxs-lookup"><span data-stu-id="79543-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="79543-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79543-111">PARAMETERS</span></span>

### <span data-ttu-id="79543-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79543-112">-ApplicationGateway</span></span>
<span data-ttu-id="79543-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="79543-113">The applicationGateway</span></span>

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

### <span data-ttu-id="79543-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79543-114">-DefaultProfile</span></span>
<span data-ttu-id="79543-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79543-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79543-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="79543-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="79543-117">Az ResourceId hozzárendelendő felhasználó által hozzárendelt identitás.</span><span class="sxs-lookup"><span data-stu-id="79543-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="79543-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="79543-118">-Confirm</span></span>
<span data-ttu-id="79543-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="79543-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79543-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79543-120">-WhatIf</span></span>
<span data-ttu-id="79543-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="79543-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79543-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79543-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79543-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79543-123">CommonParameters</span></span>
<span data-ttu-id="79543-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79543-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79543-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79543-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79543-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79543-126">INPUTS</span></span>

### <span data-ttu-id="79543-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79543-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="79543-128">System. String</span><span class="sxs-lookup"><span data-stu-id="79543-128">System.String</span></span>

## <span data-ttu-id="79543-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79543-129">OUTPUTS</span></span>

### <span data-ttu-id="79543-130">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79543-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79543-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79543-131">NOTES</span></span>

## <span data-ttu-id="79543-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79543-132">RELATED LINKS</span></span>
