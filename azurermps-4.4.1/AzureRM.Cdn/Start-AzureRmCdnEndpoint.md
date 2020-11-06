---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: 742fe2795f16ed0a626e071520977ead66a491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497859"
---
# <span data-ttu-id="e975b-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e975b-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="e975b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e975b-102">SYNOPSIS</span></span>
<span data-ttu-id="e975b-103">Beindít egy CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="e975b-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e975b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e975b-104">SYNTAX</span></span>

### <span data-ttu-id="e975b-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e975b-105">Parameter Set for fields parameters (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e975b-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="e975b-106">Parameter Set for object parameters</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e975b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e975b-107">DESCRIPTION</span></span>
<span data-ttu-id="e975b-108">A **Start-AzureRmCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját indítja el.</span><span class="sxs-lookup"><span data-stu-id="e975b-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e975b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e975b-109">EXAMPLES</span></span>

## <span data-ttu-id="e975b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e975b-110">PARAMETERS</span></span>

### <span data-ttu-id="e975b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e975b-111">-CdnEndpoint</span></span>
<span data-ttu-id="e975b-112">A parancsmag kezdetét megadó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e975b-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e975b-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e975b-113">-EndpointName</span></span>
<span data-ttu-id="e975b-114">Annak a végpontnak a nevét adja meg, amelyre a parancsmag indul.</span><span class="sxs-lookup"><span data-stu-id="e975b-114">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e975b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e975b-115">-PassThru</span></span>
<span data-ttu-id="e975b-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e975b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e975b-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e975b-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e975b-118">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="e975b-118">-ProfileName</span></span>
<span data-ttu-id="e975b-119">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="e975b-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e975b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e975b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e975b-121">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="e975b-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e975b-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e975b-122">-Confirm</span></span>
<span data-ttu-id="e975b-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e975b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e975b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e975b-124">-WhatIf</span></span>
<span data-ttu-id="e975b-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e975b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e975b-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e975b-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e975b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e975b-127">-DefaultProfile</span></span>
<span data-ttu-id="e975b-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e975b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e975b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e975b-129">CommonParameters</span></span>
<span data-ttu-id="e975b-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e975b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e975b-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e975b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e975b-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e975b-132">INPUTS</span></span>

### <span data-ttu-id="e975b-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e975b-133">PSEndpoint</span></span>
<span data-ttu-id="e975b-134">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e975b-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e975b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e975b-135">OUTPUTS</span></span>

### <span data-ttu-id="e975b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e975b-136">System.Boolean</span></span>

## <span data-ttu-id="e975b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e975b-137">NOTES</span></span>

## <span data-ttu-id="e975b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e975b-138">RELATED LINKS</span></span>

[<span data-ttu-id="e975b-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e975b-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e975b-140">Új – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e975b-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e975b-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e975b-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e975b-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e975b-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e975b-143">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e975b-143">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


