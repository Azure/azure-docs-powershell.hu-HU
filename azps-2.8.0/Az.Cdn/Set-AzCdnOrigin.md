---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 71f5732f7473a90af0509d2e3932ca5151ef870a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667570"
---
# <span data-ttu-id="f906f-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f906f-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="f906f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f906f-102">SYNOPSIS</span></span>
<span data-ttu-id="f906f-103">Egy CDN-származási kiszolgáló frissítése</span><span class="sxs-lookup"><span data-stu-id="f906f-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="f906f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f906f-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f906f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f906f-105">DESCRIPTION</span></span>
<span data-ttu-id="f906f-106">A **set-AzCdnOrigin** parancsmag frissíti az Azure Content Delivery Network (CDN) Origin kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="f906f-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="f906f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f906f-107">EXAMPLES</span></span>

## <span data-ttu-id="f906f-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f906f-108">PARAMETERS</span></span>

### <span data-ttu-id="f906f-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f906f-109">-CdnOrigin</span></span>
<span data-ttu-id="f906f-110">A parancsmag által frissített forráskiszolgálón adja meg.</span><span class="sxs-lookup"><span data-stu-id="f906f-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f906f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f906f-111">-DefaultProfile</span></span>
<span data-ttu-id="f906f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f906f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f906f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f906f-113">CommonParameters</span></span>
<span data-ttu-id="f906f-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f906f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f906f-115">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f906f-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f906f-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f906f-116">INPUTS</span></span>

### <span data-ttu-id="f906f-117">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="f906f-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="f906f-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f906f-118">OUTPUTS</span></span>

### <span data-ttu-id="f906f-119">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="f906f-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="f906f-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f906f-120">NOTES</span></span>

## <span data-ttu-id="f906f-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f906f-121">RELATED LINKS</span></span>

[<span data-ttu-id="f906f-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f906f-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


