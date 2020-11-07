---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: a851722d02fa37c085649894f41f6273abf4372d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836850"
---
# <span data-ttu-id="1cb83-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="1cb83-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="1cb83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cb83-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb83-103">Tartalmat tölt be egy végpontra.</span><span class="sxs-lookup"><span data-stu-id="1cb83-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="1cb83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cb83-104">SYNTAX</span></span>

### <span data-ttu-id="1cb83-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1cb83-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cb83-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb83-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cb83-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cb83-107">DESCRIPTION</span></span>
<span data-ttu-id="1cb83-108">A **Közzététel – AzCdnEndpointContent** parancsmag az Azure Content Delivery Network (CDN) végpontjának tartalmát betölti a forrás-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="1cb83-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1cb83-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1cb83-109">EXAMPLES</span></span>

## <span data-ttu-id="1cb83-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cb83-110">PARAMETERS</span></span>

### <span data-ttu-id="1cb83-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1cb83-111">-CdnEndpoint</span></span>
<span data-ttu-id="1cb83-112">Sepcifies a CDN végpontot.</span><span class="sxs-lookup"><span data-stu-id="1cb83-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="1cb83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb83-113">-DefaultProfile</span></span>
<span data-ttu-id="1cb83-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1cb83-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cb83-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1cb83-115">-EndpointName</span></span>
<span data-ttu-id="1cb83-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1cb83-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="1cb83-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="1cb83-117">-LoadContent</span></span>
<span data-ttu-id="1cb83-118">A forráskiszolgáló által közzétett tartalom relatív elérési útjának tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1cb83-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="1cb83-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cb83-119">-PassThru</span></span>
<span data-ttu-id="1cb83-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1cb83-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1cb83-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1cb83-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1cb83-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="1cb83-122">-ProfileName</span></span>
<span data-ttu-id="1cb83-123">Annak a profilnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="1cb83-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="1cb83-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb83-124">-ResourceGroupName</span></span>
<span data-ttu-id="1cb83-125">Annak az erőforrás-csoportnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="1cb83-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="1cb83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb83-126">CommonParameters</span></span>
<span data-ttu-id="1cb83-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cb83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb83-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cb83-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb83-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cb83-129">INPUTS</span></span>

### <span data-ttu-id="1cb83-130">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1cb83-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="1cb83-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1cb83-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1cb83-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cb83-132">OUTPUTS</span></span>

### <span data-ttu-id="1cb83-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1cb83-133">System.Boolean</span></span>

## <span data-ttu-id="1cb83-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cb83-134">NOTES</span></span>

## <span data-ttu-id="1cb83-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cb83-135">RELATED LINKS</span></span>

[<span data-ttu-id="1cb83-136">Közzététel megszüntetése – AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="1cb83-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


