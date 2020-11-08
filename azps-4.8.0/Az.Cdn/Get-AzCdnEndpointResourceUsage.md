---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181205"
---
# <span data-ttu-id="00720-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="00720-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="00720-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00720-102">SYNOPSIS</span></span>
<span data-ttu-id="00720-103">Egy CDN-végpont erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="00720-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="00720-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00720-104">SYNTAX</span></span>

### <span data-ttu-id="00720-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00720-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00720-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00720-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00720-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="00720-107">DESCRIPTION</span></span>
<span data-ttu-id="00720-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="00720-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="00720-109">Példák</span><span class="sxs-lookup"><span data-stu-id="00720-109">EXAMPLES</span></span>

### <span data-ttu-id="00720-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00720-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="00720-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="00720-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="00720-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00720-112">PARAMETERS</span></span>

### <span data-ttu-id="00720-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="00720-113">-CdnEndpoint</span></span>
<span data-ttu-id="00720-114">A CDN végpont objektuma.</span><span class="sxs-lookup"><span data-stu-id="00720-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="00720-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00720-115">-DefaultProfile</span></span>
<span data-ttu-id="00720-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="00720-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00720-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="00720-117">-EndpointName</span></span>
<span data-ttu-id="00720-118">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="00720-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="00720-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="00720-119">-ProfileName</span></span>
<span data-ttu-id="00720-120">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="00720-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="00720-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00720-121">-ResourceGroupName</span></span>
<span data-ttu-id="00720-122">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="00720-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="00720-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00720-123">CommonParameters</span></span>
<span data-ttu-id="00720-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00720-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00720-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="00720-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00720-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00720-126">INPUTS</span></span>

### <span data-ttu-id="00720-127">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="00720-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="00720-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00720-128">OUTPUTS</span></span>

### <span data-ttu-id="00720-129">Microsoft. Azure. Command. CDN. models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="00720-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="00720-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00720-130">NOTES</span></span>

## <span data-ttu-id="00720-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00720-131">RELATED LINKS</span></span>
