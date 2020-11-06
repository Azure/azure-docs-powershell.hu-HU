---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 508465250489f2bcd0b031627258f11370fccfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493216"
---
# <span data-ttu-id="e5914-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5914-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="e5914-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5914-102">SYNOPSIS</span></span>
<span data-ttu-id="e5914-103">Leállítja a CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="e5914-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5914-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5914-104">SYNTAX</span></span>

### <span data-ttu-id="e5914-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5914-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5914-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5914-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5914-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5914-107">DESCRIPTION</span></span>
<span data-ttu-id="e5914-108">A **stop-AzureRmCdnEndpoint** parancsmag leállítja az Azure Content Delivery Network (CDN) végpontját.</span><span class="sxs-lookup"><span data-stu-id="e5914-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e5914-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e5914-109">EXAMPLES</span></span>

## <span data-ttu-id="e5914-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5914-110">PARAMETERS</span></span>

### <span data-ttu-id="e5914-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5914-111">-CdnEndpoint</span></span>
<span data-ttu-id="e5914-112">Azt a végpont-objektumot adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="e5914-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5914-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5914-113">-DefaultProfile</span></span>
<span data-ttu-id="e5914-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5914-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5914-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e5914-115">-EndpointName</span></span>
<span data-ttu-id="e5914-116">Annak a végpontnak a nevét adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="e5914-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5914-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5914-117">-PassThru</span></span>
<span data-ttu-id="e5914-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e5914-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5914-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e5914-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5914-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="e5914-120">-ProfileName</span></span>
<span data-ttu-id="e5914-121">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="e5914-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5914-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5914-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5914-123">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="e5914-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5914-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5914-124">-Confirm</span></span>
<span data-ttu-id="e5914-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5914-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5914-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5914-126">-WhatIf</span></span>
<span data-ttu-id="e5914-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5914-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5914-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5914-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5914-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5914-129">CommonParameters</span></span>
<span data-ttu-id="e5914-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5914-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5914-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5914-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5914-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5914-132">INPUTS</span></span>

### <span data-ttu-id="e5914-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5914-133">PSEndpoint</span></span>
<span data-ttu-id="e5914-134">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e5914-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e5914-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5914-135">OUTPUTS</span></span>

### <span data-ttu-id="e5914-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5914-136">System.Boolean</span></span>

## <span data-ttu-id="e5914-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5914-137">NOTES</span></span>

## <span data-ttu-id="e5914-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5914-138">RELATED LINKS</span></span>

[<span data-ttu-id="e5914-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5914-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e5914-140">Új – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5914-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e5914-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5914-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e5914-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5914-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e5914-143">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5914-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


