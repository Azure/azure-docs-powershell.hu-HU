---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494658"
---
# <span data-ttu-id="40aa7-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="40aa7-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="40aa7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="40aa7-103">Az Azure webhely-helyreállítási anyag tulajdonságainak beszerzése.</span><span class="sxs-lookup"><span data-stu-id="40aa7-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40aa7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40aa7-104">SYNTAX</span></span>

### <span data-ttu-id="40aa7-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40aa7-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40aa7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="40aa7-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40aa7-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="40aa7-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40aa7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="40aa7-108">DESCRIPTION</span></span>
<span data-ttu-id="40aa7-109">A **Get-AzureRmSiteRecoveryFabric** parancsmag egy megadott Azure-webhely helyreállítási szövetének vagy minden Azure webhely-helyreállítási szövetnek a tulajdonságait adja meg helyreállítási szolgáltatás-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="40aa7-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="40aa7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="40aa7-110">EXAMPLES</span></span>

## <span data-ttu-id="40aa7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40aa7-111">PARAMETERS</span></span>

### <span data-ttu-id="40aa7-112">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="40aa7-112">-FriendlyName</span></span>
<span data-ttu-id="40aa7-113">Az Azure webhely-helyreállítási anyag rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40aa7-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40aa7-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40aa7-114">-Name</span></span>
<span data-ttu-id="40aa7-115">Az Azure webhely-helyreállítási anyag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40aa7-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40aa7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40aa7-116">-DefaultProfile</span></span>
<span data-ttu-id="40aa7-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40aa7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40aa7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40aa7-118">CommonParameters</span></span>
<span data-ttu-id="40aa7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40aa7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40aa7-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40aa7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40aa7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40aa7-121">INPUTS</span></span>

## <span data-ttu-id="40aa7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40aa7-122">OUTPUTS</span></span>

### <span data-ttu-id="40aa7-123">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRFabric, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="40aa7-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="40aa7-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40aa7-124">NOTES</span></span>

## <span data-ttu-id="40aa7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40aa7-125">RELATED LINKS</span></span>

[<span data-ttu-id="40aa7-126">Új – AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="40aa7-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="40aa7-127">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="40aa7-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
