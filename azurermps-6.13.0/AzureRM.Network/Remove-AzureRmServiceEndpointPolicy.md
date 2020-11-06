---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503508"
---
# <span data-ttu-id="dae6e-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dae6e-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="dae6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dae6e-102">SYNOPSIS</span></span>
<span data-ttu-id="dae6e-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="dae6e-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dae6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dae6e-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dae6e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dae6e-105">DESCRIPTION</span></span>
<span data-ttu-id="dae6e-106">A **Remove-AzureRmServiceEndpointPolicy** parancsmag eltávolítja a szolgáltatási végpontok házirendjét.</span><span class="sxs-lookup"><span data-stu-id="dae6e-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="dae6e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dae6e-107">EXAMPLES</span></span>

### <span data-ttu-id="dae6e-108">1. példa: a szolgáltatás végpont-házirendjének eltávolítása név használatával</span><span class="sxs-lookup"><span data-stu-id="dae6e-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="dae6e-109">Ez a parancs eltávolítja a Service Endpoint Policy nevű Házirend1, amely a "resourcegroup1" nevű resourcegroup tartozik</span><span class="sxs-lookup"><span data-stu-id="dae6e-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="dae6e-110">2. példa: a szolgáltatási végpontok házirendjének eltávolítása a beviteli objektum használatával</span><span class="sxs-lookup"><span data-stu-id="dae6e-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="dae6e-111">Ez a parancs eltávolítja az "resourcegroup1" nevű resourcegroup-Házirend1 tartozó szolgáltatás-végpontok házirend-objektumát.</span><span class="sxs-lookup"><span data-stu-id="dae6e-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="dae6e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dae6e-112">PARAMETERS</span></span>

### <span data-ttu-id="dae6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae6e-113">-DefaultProfile</span></span>
<span data-ttu-id="dae6e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dae6e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dae6e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dae6e-115">-Force</span></span>
<span data-ttu-id="dae6e-116">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="dae6e-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="dae6e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dae6e-117">-Name</span></span>
<span data-ttu-id="dae6e-118">A szolgáltatás végpont-házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="dae6e-118">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="dae6e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dae6e-119">-PassThru</span></span>
<span data-ttu-id="dae6e-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="dae6e-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dae6e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae6e-121">-ResourceGroupName</span></span>
<span data-ttu-id="dae6e-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="dae6e-122">The resource group name.</span></span>

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

### <span data-ttu-id="dae6e-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dae6e-123">-Confirm</span></span>
<span data-ttu-id="dae6e-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dae6e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae6e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae6e-125">-WhatIf</span></span>
<span data-ttu-id="dae6e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dae6e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dae6e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dae6e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae6e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae6e-128">CommonParameters</span></span>
<span data-ttu-id="dae6e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dae6e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dae6e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dae6e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae6e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dae6e-131">INPUTS</span></span>

### <span data-ttu-id="dae6e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dae6e-132">System.String</span></span>


## <span data-ttu-id="dae6e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dae6e-133">OUTPUTS</span></span>

### <span data-ttu-id="dae6e-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="dae6e-134">System.Object</span></span>

## <span data-ttu-id="dae6e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dae6e-135">NOTES</span></span>

## <span data-ttu-id="dae6e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dae6e-136">RELATED LINKS</span></span>
