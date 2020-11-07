---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 3622b7ad87658091d4b54af62678d12a324ef56a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850618"
---
# <span data-ttu-id="2270e-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2270e-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="2270e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2270e-102">SYNOPSIS</span></span>
<span data-ttu-id="2270e-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="2270e-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2270e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2270e-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2270e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2270e-105">DESCRIPTION</span></span>
<span data-ttu-id="2270e-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="2270e-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2270e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2270e-107">EXAMPLES</span></span>

### <span data-ttu-id="2270e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2270e-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2270e-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="2270e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="2270e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2270e-110">PARAMETERS</span></span>

### <span data-ttu-id="2270e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2270e-111">-DefaultProfile</span></span>
<span data-ttu-id="2270e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2270e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2270e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2270e-113">-Force</span></span>
<span data-ttu-id="2270e-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2270e-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2270e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2270e-115">-Name</span></span>
<span data-ttu-id="2270e-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2270e-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2270e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2270e-117">-PassThru</span></span>
<span data-ttu-id="2270e-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2270e-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2270e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2270e-119">-ResourceGroupName</span></span>
<span data-ttu-id="2270e-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2270e-120">The resource group name.</span></span>

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

### <span data-ttu-id="2270e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2270e-121">-Confirm</span></span>
<span data-ttu-id="2270e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2270e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2270e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2270e-123">-WhatIf</span></span>
<span data-ttu-id="2270e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2270e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2270e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2270e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2270e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2270e-126">CommonParameters</span></span>
<span data-ttu-id="2270e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2270e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2270e-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2270e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2270e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2270e-129">INPUTS</span></span>

### <span data-ttu-id="2270e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2270e-130">System.String</span></span>

## <span data-ttu-id="2270e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2270e-131">OUTPUTS</span></span>

### <span data-ttu-id="2270e-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="2270e-132">System.Object</span></span>

## <span data-ttu-id="2270e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2270e-133">NOTES</span></span>

## <span data-ttu-id="2270e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2270e-134">RELATED LINKS</span></span>

