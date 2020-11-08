---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194915"
---
# <span data-ttu-id="f7b9f-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="f7b9f-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="f7b9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b9f-103">Törli a CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="f7b9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7b9f-104">SYNTAX</span></span>

### <span data-ttu-id="f7b9f-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7b9f-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7b9f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7b9f-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b9f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7b9f-107">DESCRIPTION</span></span>
<span data-ttu-id="f7b9f-108">A **Közzététel nélküli AzCdnEndpointContent** parancsmag kiüríti a tartalmat egy Azure Content Delivery Network (CDN) végpontról.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f7b9f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f7b9f-109">EXAMPLES</span></span>

## <span data-ttu-id="f7b9f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7b9f-110">PARAMETERS</span></span>

### <span data-ttu-id="f7b9f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7b9f-111">-CdnEndpoint</span></span>
<span data-ttu-id="f7b9f-112">A parancsmagot tartalmazó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="f7b9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b9f-113">-DefaultProfile</span></span>
<span data-ttu-id="f7b9f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f7b9f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7b9f-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f7b9f-115">-EndpointName</span></span>
<span data-ttu-id="f7b9f-116">Annak a végpontnak a nevét adja meg, amely a parancsmagot törli.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="f7b9f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7b9f-117">-PassThru</span></span>
<span data-ttu-id="f7b9f-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f7b9f-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f7b9f-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="f7b9f-120">-ProfileName</span></span>
<span data-ttu-id="f7b9f-121">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="f7b9f-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="f7b9f-122">-PurgeContent</span></span>
<span data-ttu-id="f7b9f-123">A forrás-kiszolgálón található tartalom relatív elérési útjának tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="f7b9f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b9f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7b9f-125">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="f7b9f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7b9f-126">-Confirm</span></span>
<span data-ttu-id="f7b9f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b9f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b9f-128">-WhatIf</span></span>
<span data-ttu-id="f7b9f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b9f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b9f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b9f-131">CommonParameters</span></span>
<span data-ttu-id="f7b9f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7b9f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b9f-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f7b9f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b9f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7b9f-134">INPUTS</span></span>

### <span data-ttu-id="f7b9f-135">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7b9f-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="f7b9f-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f7b9f-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7b9f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7b9f-137">OUTPUTS</span></span>

### <span data-ttu-id="f7b9f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7b9f-138">System.Boolean</span></span>

## <span data-ttu-id="f7b9f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7b9f-139">NOTES</span></span>

## <span data-ttu-id="f7b9f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7b9f-140">RELATED LINKS</span></span>

[<span data-ttu-id="f7b9f-141">Közzététel – AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="f7b9f-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


