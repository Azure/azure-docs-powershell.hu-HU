---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502019"
---
# <span data-ttu-id="189ae-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="189ae-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="189ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="189ae-102">SYNOPSIS</span></span>
<span data-ttu-id="189ae-103">Az alkalmazás-átjáró automatikus méretarányos konfigurációjának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="189ae-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="189ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="189ae-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="189ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="189ae-105">DESCRIPTION</span></span>
<span data-ttu-id="189ae-106">A **New-AzureRmApplicationGatewayAutoscaleConfiguration** parancsmag automatikus méretezési konfigurációt hoz létre az Azure Application Gateway rendszerhez.</span><span class="sxs-lookup"><span data-stu-id="189ae-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="189ae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="189ae-107">EXAMPLES</span></span>

### <span data-ttu-id="189ae-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="189ae-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="189ae-109">Az első parancs automatikusan létrehoz egy automatikus méretarányos konfigurációt, amelynek minimális kapacitása 3.</span><span class="sxs-lookup"><span data-stu-id="189ae-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="189ae-110">A második parancs az alkalmazás-átjárót az automatikus méretezési konfigurációval hozza létre.</span><span class="sxs-lookup"><span data-stu-id="189ae-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="189ae-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="189ae-111">PARAMETERS</span></span>

### <span data-ttu-id="189ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189ae-112">-DefaultProfile</span></span>
<span data-ttu-id="189ae-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="189ae-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="189ae-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="189ae-114">-MinCapacity</span></span>
<span data-ttu-id="189ae-115">Minimális kapacitású egységek, amelyek mindig elérhetők [és felszámítva] az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="189ae-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="189ae-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="189ae-116">-Confirm</span></span>
<span data-ttu-id="189ae-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="189ae-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="189ae-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="189ae-118">-WhatIf</span></span>
<span data-ttu-id="189ae-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="189ae-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="189ae-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="189ae-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="189ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189ae-121">CommonParameters</span></span>
<span data-ttu-id="189ae-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="189ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189ae-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="189ae-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189ae-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="189ae-124">INPUTS</span></span>

### <span data-ttu-id="189ae-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="189ae-125">None</span></span>

## <span data-ttu-id="189ae-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="189ae-126">OUTPUTS</span></span>

### <span data-ttu-id="189ae-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="189ae-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="189ae-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="189ae-128">NOTES</span></span>

## <span data-ttu-id="189ae-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="189ae-129">RELATED LINKS</span></span>
