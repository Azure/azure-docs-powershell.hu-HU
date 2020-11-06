---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a774aec8114883d3ba2a5edf189f115f99d3eb4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497836"
---
# <span data-ttu-id="bbcf8-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="bbcf8-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="bbcf8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbcf8-102">SYNOPSIS</span></span>
<span data-ttu-id="bbcf8-103">Törli a CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbcf8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbcf8-104">SYNTAX</span></span>

### <span data-ttu-id="bbcf8-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bbcf8-105">Parameter Set for fields parameters (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbcf8-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="bbcf8-106">Parameter Set for object parameters</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbcf8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbcf8-107">DESCRIPTION</span></span>
<span data-ttu-id="bbcf8-108">A **Közzététel nélküli AzureRmCdnEndpointContent** parancsmag kiüríti a tartalmat egy Azure Content Delivery Network (CDN) végpontról.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bbcf8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bbcf8-109">EXAMPLES</span></span>

## <span data-ttu-id="bbcf8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbcf8-110">PARAMETERS</span></span>

### <span data-ttu-id="bbcf8-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbcf8-111">-CdnEndpoint</span></span>
<span data-ttu-id="bbcf8-112">A parancsmagot tartalmazó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="bbcf8-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bbcf8-113">-EndpointName</span></span>
<span data-ttu-id="bbcf8-114">Annak a végpontnak a nevét adja meg, amely a parancsmagot törli.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-114">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="bbcf8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbcf8-115">-PassThru</span></span>
<span data-ttu-id="bbcf8-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bbcf8-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bbcf8-118">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="bbcf8-118">-ProfileName</span></span>
<span data-ttu-id="bbcf8-119">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="bbcf8-120">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="bbcf8-120">-PurgeContent</span></span>
<span data-ttu-id="bbcf8-121">A forrás-kiszolgálón található tartalom relatív elérési útjának tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-121">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbcf8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbcf8-122">-ResourceGroupName</span></span>
<span data-ttu-id="bbcf8-123">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="bbcf8-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bbcf8-124">-Confirm</span></span>
<span data-ttu-id="bbcf8-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbcf8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbcf8-126">-WhatIf</span></span>
<span data-ttu-id="bbcf8-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbcf8-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbcf8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbcf8-129">-DefaultProfile</span></span>
<span data-ttu-id="bbcf8-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbcf8-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbcf8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbcf8-131">CommonParameters</span></span>
<span data-ttu-id="bbcf8-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbcf8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbcf8-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbcf8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbcf8-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbcf8-134">INPUTS</span></span>

### <span data-ttu-id="bbcf8-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbcf8-135">PSEndpoint</span></span>
<span data-ttu-id="bbcf8-136">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bbcf8-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="bbcf8-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbcf8-137">OUTPUTS</span></span>

### <span data-ttu-id="bbcf8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbcf8-138">System.Boolean</span></span>

## <span data-ttu-id="bbcf8-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbcf8-139">NOTES</span></span>

## <span data-ttu-id="bbcf8-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbcf8-140">RELATED LINKS</span></span>

[<span data-ttu-id="bbcf8-141">Közzététel – AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="bbcf8-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


