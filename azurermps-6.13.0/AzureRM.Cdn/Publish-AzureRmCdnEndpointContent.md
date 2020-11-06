---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/publish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a4a2479c6dc7c116ff7da9151fcd5dea5ec26660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498384"
---
# <span data-ttu-id="2e449-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="2e449-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="2e449-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e449-102">SYNOPSIS</span></span>
<span data-ttu-id="2e449-103">Tartalmat tölt be egy végpontra.</span><span class="sxs-lookup"><span data-stu-id="2e449-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e449-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e449-104">SYNTAX</span></span>

### <span data-ttu-id="2e449-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e449-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e449-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e449-106">ByObjectParameterSet</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e449-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e449-107">DESCRIPTION</span></span>
<span data-ttu-id="2e449-108">A **Közzététel – AzureRmCdnEndpointContent** parancsmag az Azure Content Delivery Network (CDN) végpontjának tartalmát betölti a forrás-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="2e449-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2e449-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2e449-109">EXAMPLES</span></span>

## <span data-ttu-id="2e449-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e449-110">PARAMETERS</span></span>

### <span data-ttu-id="2e449-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e449-111">-CdnEndpoint</span></span>
<span data-ttu-id="2e449-112">Sepcifies a CDN végpontot.</span><span class="sxs-lookup"><span data-stu-id="2e449-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="2e449-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e449-113">-DefaultProfile</span></span>
<span data-ttu-id="2e449-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2e449-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e449-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2e449-115">-EndpointName</span></span>
<span data-ttu-id="2e449-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e449-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="2e449-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="2e449-117">-LoadContent</span></span>
<span data-ttu-id="2e449-118">A forráskiszolgáló által közzétett tartalom relatív elérési útjának tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e449-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="2e449-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e449-119">-PassThru</span></span>
<span data-ttu-id="2e449-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2e449-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e449-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2e449-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e449-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="2e449-122">-ProfileName</span></span>
<span data-ttu-id="2e449-123">Annak a profilnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="2e449-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2e449-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e449-124">-ResourceGroupName</span></span>
<span data-ttu-id="2e449-125">Annak az erőforrás-csoportnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="2e449-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2e449-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e449-126">CommonParameters</span></span>
<span data-ttu-id="2e449-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e449-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e449-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e449-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e449-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e449-129">INPUTS</span></span>

### <span data-ttu-id="2e449-130">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e449-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="2e449-131">Paraméterek: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e449-131">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="2e449-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e449-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e449-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e449-133">OUTPUTS</span></span>

### <span data-ttu-id="2e449-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e449-134">System.Boolean</span></span>

## <span data-ttu-id="2e449-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e449-135">NOTES</span></span>

## <span data-ttu-id="2e449-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e449-136">RELATED LINKS</span></span>

[<span data-ttu-id="2e449-137">Közzététel megszüntetése – AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="2e449-137">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


