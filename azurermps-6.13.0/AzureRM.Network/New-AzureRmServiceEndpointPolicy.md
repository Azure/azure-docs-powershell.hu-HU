---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502007"
---
# <span data-ttu-id="084f5-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="084f5-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="084f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="084f5-102">SYNOPSIS</span></span>
<span data-ttu-id="084f5-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="084f5-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="084f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="084f5-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="084f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="084f5-105">DESCRIPTION</span></span>
<span data-ttu-id="084f5-106">A **New-AzureRmServiceEndpointPolicy** parancsmag létrehoz egy szolgáltatási végpont-házirendet.</span><span class="sxs-lookup"><span data-stu-id="084f5-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="084f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="084f5-107">EXAMPLES</span></span>

### <span data-ttu-id="084f5-108">Példa 1: szolgáltatás végpont-házirendjének létrehozása</span><span class="sxs-lookup"><span data-stu-id="084f5-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="084f5-109">Ez a parancs létrehoz egy Házirend1 nevű szolgáltatási végpont-házirendet az objektum által definiált definíciókkal $serviceEndpointDefinition és a $serviceEndpointPolicy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="084f5-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="084f5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="084f5-110">PARAMETERS</span></span>

### <span data-ttu-id="084f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084f5-111">-DefaultProfile</span></span>
<span data-ttu-id="084f5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="084f5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084f5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="084f5-113">-Force</span></span>
<span data-ttu-id="084f5-114">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="084f5-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084f5-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="084f5-115">-Name</span></span>
<span data-ttu-id="084f5-116">Az alhálózat neve</span><span class="sxs-lookup"><span data-stu-id="084f5-116">The name of the subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="084f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="084f5-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="084f5-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="084f5-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="084f5-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="084f5-120">A szolgáltatás végpont-definícióinak listája</span><span class="sxs-lookup"><span data-stu-id="084f5-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084f5-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="084f5-121">-Confirm</span></span>
<span data-ttu-id="084f5-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="084f5-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084f5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084f5-123">-WhatIf</span></span>
<span data-ttu-id="084f5-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="084f5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084f5-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="084f5-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084f5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084f5-126">CommonParameters</span></span>
<span data-ttu-id="084f5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="084f5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="084f5-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="084f5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084f5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="084f5-129">INPUTS</span></span>

### <span data-ttu-id="084f5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="084f5-130">System.String</span></span>


## <span data-ttu-id="084f5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="084f5-131">OUTPUTS</span></span>

### <span data-ttu-id="084f5-132">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="084f5-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="084f5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="084f5-133">NOTES</span></span>

## <span data-ttu-id="084f5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="084f5-134">RELATED LINKS</span></span>
