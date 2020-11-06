---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 1df36c7816894f8ccfc642eac307a84b485ba7ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500907"
---
# <span data-ttu-id="2a169-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="2a169-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="2a169-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a169-102">SYNOPSIS</span></span>
<span data-ttu-id="2a169-103">Tartalmat tölt be egy végpontra.</span><span class="sxs-lookup"><span data-stu-id="2a169-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a169-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a169-104">SYNTAX</span></span>

### <span data-ttu-id="2a169-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a169-105">Parameter Set for fields parameters (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a169-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="2a169-106">Parameter Set for object parameters</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a169-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a169-107">DESCRIPTION</span></span>
<span data-ttu-id="2a169-108">A **Közzététel – AzureRmCdnEndpointContent** parancsmag az Azure Content Delivery Network (CDN) végpontjának tartalmát betölti a forrás-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="2a169-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2a169-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2a169-109">EXAMPLES</span></span>

## <span data-ttu-id="2a169-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a169-110">PARAMETERS</span></span>

### <span data-ttu-id="2a169-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2a169-111">-CdnEndpoint</span></span>
<span data-ttu-id="2a169-112">Sepcifies a CDN végpontot.</span><span class="sxs-lookup"><span data-stu-id="2a169-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="2a169-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2a169-113">-EndpointName</span></span>
<span data-ttu-id="2a169-114">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a169-114">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="2a169-115">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="2a169-115">-LoadContent</span></span>
<span data-ttu-id="2a169-116">A forráskiszolgáló által közzétett tartalom relatív elérési útjának tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a169-116">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="2a169-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a169-117">-PassThru</span></span>
<span data-ttu-id="2a169-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2a169-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a169-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2a169-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a169-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="2a169-120">-ProfileName</span></span>
<span data-ttu-id="2a169-121">Annak a profilnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="2a169-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2a169-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a169-122">-ResourceGroupName</span></span>
<span data-ttu-id="2a169-123">Annak az erőforrás-csoportnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="2a169-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2a169-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a169-124">-DefaultProfile</span></span>
<span data-ttu-id="2a169-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a169-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a169-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a169-126">CommonParameters</span></span>
<span data-ttu-id="2a169-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a169-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a169-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a169-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a169-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a169-129">INPUTS</span></span>

### <span data-ttu-id="2a169-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2a169-130">PSEndpoint</span></span>
<span data-ttu-id="2a169-131">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2a169-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="2a169-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a169-132">OUTPUTS</span></span>

### <span data-ttu-id="2a169-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a169-133">System.Boolean</span></span>

## <span data-ttu-id="2a169-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a169-134">NOTES</span></span>

## <span data-ttu-id="2a169-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a169-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a169-136">Közzététel megszüntetése – AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="2a169-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


