---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 28f285ef55acbca3c4226f198f69fb9a70b62364
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667608"
---
# <span data-ttu-id="9eeb7-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="9eeb7-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="9eeb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9eeb7-102">SYNOPSIS</span></span>
<span data-ttu-id="9eeb7-103">Egy CDN-végpont erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9eeb7-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="9eeb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9eeb7-104">SYNTAX</span></span>

### <span data-ttu-id="9eeb7-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9eeb7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eeb7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eeb7-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eeb7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9eeb7-107">DESCRIPTION</span></span>
<span data-ttu-id="9eeb7-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="9eeb7-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9eeb7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9eeb7-109">EXAMPLES</span></span>

### <span data-ttu-id="9eeb7-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9eeb7-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9eeb7-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="9eeb7-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="9eeb7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9eeb7-112">PARAMETERS</span></span>

### <span data-ttu-id="9eeb7-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9eeb7-113">-CdnEndpoint</span></span>
<span data-ttu-id="9eeb7-114">A CDN végpont objektuma.</span><span class="sxs-lookup"><span data-stu-id="9eeb7-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="9eeb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eeb7-115">-DefaultProfile</span></span>
<span data-ttu-id="9eeb7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9eeb7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eeb7-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9eeb7-117">-EndpointName</span></span>
<span data-ttu-id="9eeb7-118">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="9eeb7-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="9eeb7-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="9eeb7-119">-ProfileName</span></span>
<span data-ttu-id="9eeb7-120">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="9eeb7-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="9eeb7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eeb7-121">-ResourceGroupName</span></span>
<span data-ttu-id="9eeb7-122">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="9eeb7-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="9eeb7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eeb7-123">CommonParameters</span></span>
<span data-ttu-id="9eeb7-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9eeb7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eeb7-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9eeb7-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eeb7-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eeb7-126">INPUTS</span></span>

### <span data-ttu-id="9eeb7-127">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9eeb7-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9eeb7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eeb7-128">OUTPUTS</span></span>

### <span data-ttu-id="9eeb7-129">Microsoft. Azure. Command. CDN. models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="9eeb7-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="9eeb7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9eeb7-130">NOTES</span></span>

## <span data-ttu-id="9eeb7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9eeb7-131">RELATED LINKS</span></span>
