---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: f9d9d307959d53748afe7219ccb4cbce631c5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505636"
---
# <span data-ttu-id="04283-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="04283-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="04283-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04283-102">SYNOPSIS</span></span>
<span data-ttu-id="04283-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="04283-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04283-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04283-104">SYNTAX</span></span>

### <span data-ttu-id="04283-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04283-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04283-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="04283-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04283-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="04283-107">DESCRIPTION</span></span>
<span data-ttu-id="04283-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="04283-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="04283-109">Példák</span><span class="sxs-lookup"><span data-stu-id="04283-109">EXAMPLES</span></span>

### <span data-ttu-id="04283-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="04283-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="04283-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="04283-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="04283-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04283-112">PARAMETERS</span></span>

### <span data-ttu-id="04283-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="04283-113">-CdnEndpoint</span></span>
<span data-ttu-id="04283-114">A CDN végpont objektuma.</span><span class="sxs-lookup"><span data-stu-id="04283-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="04283-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="04283-115">-EndpointName</span></span>
<span data-ttu-id="04283-116">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="04283-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04283-117">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="04283-117">-ProfileName</span></span>
<span data-ttu-id="04283-118">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="04283-118">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="04283-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04283-119">-ResourceGroupName</span></span>
<span data-ttu-id="04283-120">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="04283-120">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="04283-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04283-121">-DefaultProfile</span></span>
<span data-ttu-id="04283-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04283-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04283-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04283-123">CommonParameters</span></span>
<span data-ttu-id="04283-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04283-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04283-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04283-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04283-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04283-126">INPUTS</span></span>

### <span data-ttu-id="04283-127">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="04283-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="04283-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04283-128">OUTPUTS</span></span>

### <span data-ttu-id="04283-129">Microsoft. Azure. Command. CDN. models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="04283-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="04283-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04283-130">NOTES</span></span>

## <span data-ttu-id="04283-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04283-131">RELATED LINKS</span></span>

