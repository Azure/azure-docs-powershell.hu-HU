---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 179b4b028c7dd9338e75d07f559a61052b3d2bcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493223"
---
# <span data-ttu-id="30ee7-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="30ee7-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="30ee7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="30ee7-103">Egy CDN-származási kiszolgáló frissítése</span><span class="sxs-lookup"><span data-stu-id="30ee7-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30ee7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30ee7-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30ee7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30ee7-105">DESCRIPTION</span></span>
<span data-ttu-id="30ee7-106">A **set-AzureRmCdnOrigin** parancsmag frissíti az Azure Content Delivery Network (CDN) Origin kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="30ee7-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="30ee7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30ee7-107">EXAMPLES</span></span>

## <span data-ttu-id="30ee7-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30ee7-108">PARAMETERS</span></span>

### <span data-ttu-id="30ee7-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="30ee7-109">-CdnOrigin</span></span>
<span data-ttu-id="30ee7-110">A parancsmag által frissített forráskiszolgálón adja meg.</span><span class="sxs-lookup"><span data-stu-id="30ee7-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: PSOrigin
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30ee7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ee7-111">-DefaultProfile</span></span>
<span data-ttu-id="30ee7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="30ee7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30ee7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ee7-113">CommonParameters</span></span>
<span data-ttu-id="30ee7-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30ee7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ee7-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ee7-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ee7-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30ee7-116">INPUTS</span></span>

### <span data-ttu-id="30ee7-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="30ee7-117">PSOrigin</span></span>
<span data-ttu-id="30ee7-118">A CdnOrigin' paraméter az "PSOrigin'" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="30ee7-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="30ee7-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30ee7-119">OUTPUTS</span></span>

### <span data-ttu-id="30ee7-120">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="30ee7-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="30ee7-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30ee7-121">NOTES</span></span>

## <span data-ttu-id="30ee7-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30ee7-122">RELATED LINKS</span></span>

[<span data-ttu-id="30ee7-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="30ee7-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


