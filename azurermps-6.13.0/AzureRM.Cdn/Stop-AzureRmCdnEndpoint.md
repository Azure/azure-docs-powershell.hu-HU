---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 20206ebf99d597a2961804bf3062cd4c049f8017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679181"
---
# <span data-ttu-id="7d207-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d207-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="7d207-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d207-102">SYNOPSIS</span></span>
<span data-ttu-id="7d207-103">Leállítja a CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="7d207-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d207-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d207-104">SYNTAX</span></span>

### <span data-ttu-id="7d207-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d207-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d207-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d207-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d207-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d207-107">DESCRIPTION</span></span>
<span data-ttu-id="7d207-108">A **stop-AzureRmCdnEndpoint** parancsmag leállítja az Azure Content Delivery Network (CDN) végpontját.</span><span class="sxs-lookup"><span data-stu-id="7d207-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7d207-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7d207-109">EXAMPLES</span></span>

## <span data-ttu-id="7d207-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d207-110">PARAMETERS</span></span>

### <span data-ttu-id="7d207-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d207-111">-CdnEndpoint</span></span>
<span data-ttu-id="7d207-112">Azt a végpont-objektumot adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="7d207-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d207-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d207-113">-DefaultProfile</span></span>
<span data-ttu-id="7d207-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7d207-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d207-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7d207-115">-EndpointName</span></span>
<span data-ttu-id="7d207-116">Annak a végpontnak a nevét adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="7d207-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d207-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d207-117">-PassThru</span></span>
<span data-ttu-id="7d207-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7d207-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7d207-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7d207-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7d207-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="7d207-120">-ProfileName</span></span>
<span data-ttu-id="7d207-121">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="7d207-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d207-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d207-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d207-123">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="7d207-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d207-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d207-124">-Confirm</span></span>
<span data-ttu-id="7d207-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d207-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d207-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d207-126">-WhatIf</span></span>
<span data-ttu-id="7d207-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d207-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d207-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d207-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d207-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d207-129">CommonParameters</span></span>
<span data-ttu-id="7d207-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d207-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d207-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d207-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d207-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d207-132">INPUTS</span></span>

### <span data-ttu-id="7d207-133">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d207-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="7d207-134">Paraméterek: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d207-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="7d207-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7d207-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7d207-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d207-136">OUTPUTS</span></span>

### <span data-ttu-id="7d207-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d207-137">System.Boolean</span></span>

## <span data-ttu-id="7d207-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d207-138">NOTES</span></span>

## <span data-ttu-id="7d207-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d207-139">RELATED LINKS</span></span>

[<span data-ttu-id="7d207-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d207-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7d207-141">Új – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d207-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7d207-142">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d207-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7d207-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d207-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7d207-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d207-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


