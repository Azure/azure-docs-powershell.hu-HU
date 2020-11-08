---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194288"
---
# <span data-ttu-id="ee532-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee532-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ee532-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee532-102">SYNOPSIS</span></span>
<span data-ttu-id="ee532-103">Az alkalmazás-átjáró automatikus méretarányos konfigurációjának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="ee532-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="ee532-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee532-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee532-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee532-105">DESCRIPTION</span></span>
<span data-ttu-id="ee532-106">A **New-AzApplicationGatewayAutoscaleConfiguration** parancsmag automatikus méretezési konfigurációt hoz létre az Azure Application Gateway rendszerhez.</span><span class="sxs-lookup"><span data-stu-id="ee532-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="ee532-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee532-107">EXAMPLES</span></span>

### <span data-ttu-id="ee532-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ee532-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="ee532-109">Az első parancs automatikusan létrehoz egy automatikus méretarányos konfigurációt, amelynek minimális kapacitása 3.</span><span class="sxs-lookup"><span data-stu-id="ee532-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="ee532-110">A második parancs az alkalmazás-átjárót az automatikus méretezési konfigurációval hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ee532-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="ee532-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee532-111">PARAMETERS</span></span>

### <span data-ttu-id="ee532-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee532-112">-DefaultProfile</span></span>
<span data-ttu-id="ee532-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee532-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee532-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="ee532-114">-MaxCapacity</span></span>
<span data-ttu-id="ee532-115">A maximális kapacitást tartalmazó egységek, amelyek mindig elérhetők [és felszámítva] az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="ee532-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee532-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="ee532-116">-MinCapacity</span></span>
<span data-ttu-id="ee532-117">Minimális kapacitású egységek, amelyek mindig elérhetők [és felszámítva] az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="ee532-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="ee532-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee532-118">-Confirm</span></span>
<span data-ttu-id="ee532-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee532-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee532-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee532-120">-WhatIf</span></span>
<span data-ttu-id="ee532-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee532-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee532-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee532-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee532-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee532-123">CommonParameters</span></span>
<span data-ttu-id="ee532-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee532-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee532-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee532-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee532-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee532-126">INPUTS</span></span>

### <span data-ttu-id="ee532-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee532-127">None</span></span>

## <span data-ttu-id="ee532-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee532-128">OUTPUTS</span></span>

### <span data-ttu-id="ee532-129">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee532-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ee532-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee532-130">NOTES</span></span>

## <span data-ttu-id="ee532-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee532-131">RELATED LINKS</span></span>

[<span data-ttu-id="ee532-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee532-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ee532-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee532-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ee532-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee532-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
