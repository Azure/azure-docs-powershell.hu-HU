---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 82daa7f202dce698a84d17292a199fbd8f85bca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503876"
---
# <span data-ttu-id="dafe4-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="dafe4-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="dafe4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dafe4-102">SYNOPSIS</span></span>
<span data-ttu-id="dafe4-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="dafe4-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dafe4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dafe4-104">SYNTAX</span></span>

### <span data-ttu-id="dafe4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dafe4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dafe4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dafe4-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dafe4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dafe4-107">DESCRIPTION</span></span>
<span data-ttu-id="dafe4-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="dafe4-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="dafe4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dafe4-109">EXAMPLES</span></span>

### <span data-ttu-id="dafe4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dafe4-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="dafe4-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="dafe4-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="dafe4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dafe4-112">PARAMETERS</span></span>

### <span data-ttu-id="dafe4-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dafe4-113">-CdnEndpoint</span></span>
<span data-ttu-id="dafe4-114">A CDN végpont objektuma.</span><span class="sxs-lookup"><span data-stu-id="dafe4-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="dafe4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafe4-115">-DefaultProfile</span></span>
<span data-ttu-id="dafe4-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dafe4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dafe4-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dafe4-117">-EndpointName</span></span>
<span data-ttu-id="dafe4-118">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="dafe4-118">Azure CDN endpoint name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dafe4-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="dafe4-119">-ProfileName</span></span>
<span data-ttu-id="dafe4-120">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="dafe4-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="dafe4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dafe4-121">-ResourceGroupName</span></span>
<span data-ttu-id="dafe4-122">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="dafe4-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="dafe4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafe4-123">CommonParameters</span></span>
<span data-ttu-id="dafe4-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dafe4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafe4-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dafe4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafe4-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dafe4-126">INPUTS</span></span>

### <span data-ttu-id="dafe4-127">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dafe4-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="dafe4-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dafe4-128">OUTPUTS</span></span>

### <span data-ttu-id="dafe4-129">Microsoft. Azure. Command. CDN. models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="dafe4-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="dafe4-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dafe4-130">NOTES</span></span>

## <span data-ttu-id="dafe4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dafe4-131">RELATED LINKS</span></span>

