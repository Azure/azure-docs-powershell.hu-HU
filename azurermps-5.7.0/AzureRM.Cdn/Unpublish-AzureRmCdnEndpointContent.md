---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/unpublish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: bb55b858e4c2464cced362357ffbc91a3969b1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497759"
---
# <span data-ttu-id="8f5de-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="8f5de-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="8f5de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f5de-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5de-103">Törli a CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="8f5de-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f5de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f5de-104">SYNTAX</span></span>

### <span data-ttu-id="8f5de-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f5de-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f5de-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f5de-106">ByObjectParameterSet</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f5de-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f5de-107">DESCRIPTION</span></span>
<span data-ttu-id="8f5de-108">A **Közzététel nélküli AzureRmCdnEndpointContent** parancsmag kiüríti a tartalmat egy Azure Content Delivery Network (CDN) végpontról.</span><span class="sxs-lookup"><span data-stu-id="8f5de-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="8f5de-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8f5de-109">EXAMPLES</span></span>

## <span data-ttu-id="8f5de-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f5de-110">PARAMETERS</span></span>

### <span data-ttu-id="8f5de-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f5de-111">-CdnEndpoint</span></span>
<span data-ttu-id="8f5de-112">A parancsmagot tartalmazó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f5de-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="8f5de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5de-113">-DefaultProfile</span></span>
<span data-ttu-id="8f5de-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8f5de-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f5de-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8f5de-115">-EndpointName</span></span>
<span data-ttu-id="8f5de-116">Annak a végpontnak a nevét adja meg, amely a parancsmagot törli.</span><span class="sxs-lookup"><span data-stu-id="8f5de-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="8f5de-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f5de-117">-PassThru</span></span>
<span data-ttu-id="8f5de-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="8f5de-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8f5de-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8f5de-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8f5de-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="8f5de-120">-ProfileName</span></span>
<span data-ttu-id="8f5de-121">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="8f5de-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="8f5de-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="8f5de-122">-PurgeContent</span></span>
<span data-ttu-id="8f5de-123">A forrás-kiszolgálón található tartalom relatív elérési útjának tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f5de-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f5de-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f5de-125">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="8f5de-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="8f5de-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f5de-126">-Confirm</span></span>
<span data-ttu-id="8f5de-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f5de-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f5de-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f5de-128">-WhatIf</span></span>
<span data-ttu-id="8f5de-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f5de-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f5de-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f5de-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f5de-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5de-131">CommonParameters</span></span>
<span data-ttu-id="8f5de-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f5de-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5de-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f5de-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5de-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f5de-134">INPUTS</span></span>

### <span data-ttu-id="8f5de-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f5de-135">PSEndpoint</span></span>
<span data-ttu-id="8f5de-136">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8f5de-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="8f5de-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f5de-137">OUTPUTS</span></span>

### <span data-ttu-id="8f5de-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f5de-138">System.Boolean</span></span>

## <span data-ttu-id="8f5de-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f5de-139">NOTES</span></span>

## <span data-ttu-id="8f5de-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f5de-140">RELATED LINKS</span></span>

[<span data-ttu-id="8f5de-141">Közzététel – AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="8f5de-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


