---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 9635031d6eaea5a7920a6862fb8cf20ce536c1db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012832"
---
# <span data-ttu-id="fa188-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fa188-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="fa188-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa188-102">SYNOPSIS</span></span>
<span data-ttu-id="fa188-103">Egy CDN-származási kiszolgáló frissítése</span><span class="sxs-lookup"><span data-stu-id="fa188-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="fa188-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa188-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa188-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa188-105">DESCRIPTION</span></span>
<span data-ttu-id="fa188-106">A **set-AzCdnOrigin** parancsmag frissíti az Azure Content Delivery Network (CDN) Origin kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="fa188-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="fa188-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fa188-107">EXAMPLES</span></span>

## <span data-ttu-id="fa188-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa188-108">PARAMETERS</span></span>

### <span data-ttu-id="fa188-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fa188-109">-CdnOrigin</span></span>
<span data-ttu-id="fa188-110">A parancsmag által frissített forráskiszolgálón adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa188-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa188-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa188-111">-DefaultProfile</span></span>
<span data-ttu-id="fa188-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fa188-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa188-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa188-113">CommonParameters</span></span>
<span data-ttu-id="fa188-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa188-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa188-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fa188-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa188-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa188-116">INPUTS</span></span>

### <span data-ttu-id="fa188-117">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="fa188-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="fa188-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa188-118">OUTPUTS</span></span>

### <span data-ttu-id="fa188-119">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="fa188-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="fa188-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa188-120">NOTES</span></span>

## <span data-ttu-id="fa188-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa188-121">RELATED LINKS</span></span>

[<span data-ttu-id="fa188-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fa188-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


