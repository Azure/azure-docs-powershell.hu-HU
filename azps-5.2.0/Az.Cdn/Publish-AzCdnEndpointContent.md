---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346349"
---
# <span data-ttu-id="2f53f-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="2f53f-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="2f53f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f53f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f53f-103">Tartalmat tölt be egy végpontra.</span><span class="sxs-lookup"><span data-stu-id="2f53f-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="2f53f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2f53f-104">SYNTAX</span></span>

### <span data-ttu-id="2f53f-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f53f-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f53f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f53f-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f53f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2f53f-107">DESCRIPTION</span></span>
<span data-ttu-id="2f53f-108">A **Publish-AzCdnEndpointContent parancsmag** egy originkiszolgálóról tölt be tartalmat az Azure Content Delivery Network (CDN) végponthoz.</span><span class="sxs-lookup"><span data-stu-id="2f53f-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2f53f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2f53f-109">EXAMPLES</span></span>

## <span data-ttu-id="2f53f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f53f-110">PARAMETERS</span></span>

### <span data-ttu-id="2f53f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f53f-111">-CdnEndpoint</span></span>
<span data-ttu-id="2f53f-112">A CDN-végpontot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2f53f-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="2f53f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f53f-113">-DefaultProfile</span></span>
<span data-ttu-id="2f53f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2f53f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f53f-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2f53f-115">-EndpointName</span></span>
<span data-ttu-id="2f53f-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f53f-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="2f53f-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="2f53f-117">-LoadContent</span></span>
<span data-ttu-id="2f53f-118">Az adott parancsmag által közzétett forráskiszolgálón található tartalom relatív elérési útvonalának tömbje.</span><span class="sxs-lookup"><span data-stu-id="2f53f-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="2f53f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f53f-119">-PassThru</span></span>
<span data-ttu-id="2f53f-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="2f53f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2f53f-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2f53f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f53f-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2f53f-122">-ProfileName</span></span>
<span data-ttu-id="2f53f-123">Annak a profilnak a nevét adja meg, amelyhez az originkiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="2f53f-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2f53f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f53f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f53f-125">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az originkiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="2f53f-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2f53f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f53f-126">CommonParameters</span></span>
<span data-ttu-id="2f53f-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f53f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f53f-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f53f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f53f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f53f-129">INPUTS</span></span>

### <span data-ttu-id="2f53f-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f53f-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="2f53f-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2f53f-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f53f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f53f-132">OUTPUTS</span></span>

### <span data-ttu-id="2f53f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f53f-133">System.Boolean</span></span>

## <span data-ttu-id="2f53f-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2f53f-134">NOTES</span></span>

## <span data-ttu-id="2f53f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f53f-135">RELATED LINKS</span></span>

[<span data-ttu-id="2f53f-136">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="2f53f-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


