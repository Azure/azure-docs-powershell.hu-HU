---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024851"
---
# <span data-ttu-id="e5152-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e5152-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="e5152-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5152-102">SYNOPSIS</span></span>
<span data-ttu-id="e5152-103">Tartalmat tölt be egy végpontra.</span><span class="sxs-lookup"><span data-stu-id="e5152-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="e5152-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5152-104">SYNTAX</span></span>

### <span data-ttu-id="e5152-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5152-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5152-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5152-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5152-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5152-107">DESCRIPTION</span></span>
<span data-ttu-id="e5152-108">A **Közzététel – AzCdnEndpointContent** parancsmag az Azure Content Delivery Network (CDN) végpontjának tartalmát betölti a forrás-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="e5152-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e5152-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e5152-109">EXAMPLES</span></span>

## <span data-ttu-id="e5152-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5152-110">PARAMETERS</span></span>

### <span data-ttu-id="e5152-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5152-111">-CdnEndpoint</span></span>
<span data-ttu-id="e5152-112">A CDN-végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5152-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="e5152-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5152-113">-DefaultProfile</span></span>
<span data-ttu-id="e5152-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5152-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5152-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e5152-115">-EndpointName</span></span>
<span data-ttu-id="e5152-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5152-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="e5152-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="e5152-117">-LoadContent</span></span>
<span data-ttu-id="e5152-118">A forráskiszolgáló által közzétett tartalom relatív elérési útjának tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5152-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="e5152-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5152-119">-PassThru</span></span>
<span data-ttu-id="e5152-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e5152-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5152-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e5152-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5152-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="e5152-122">-ProfileName</span></span>
<span data-ttu-id="e5152-123">Annak a profilnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="e5152-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e5152-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5152-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5152-125">Annak az erőforrás-csoportnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="e5152-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e5152-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5152-126">CommonParameters</span></span>
<span data-ttu-id="e5152-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5152-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5152-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e5152-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5152-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5152-129">INPUTS</span></span>

### <span data-ttu-id="e5152-130">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5152-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="e5152-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e5152-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e5152-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5152-132">OUTPUTS</span></span>

### <span data-ttu-id="e5152-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5152-133">System.Boolean</span></span>

## <span data-ttu-id="e5152-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5152-134">NOTES</span></span>

## <span data-ttu-id="e5152-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5152-135">RELATED LINKS</span></span>

[<span data-ttu-id="e5152-136">Közzététel megszüntetése – AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e5152-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


