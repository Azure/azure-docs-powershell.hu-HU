---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 38a7f8ee32f02db10dc971d5be2016d5dea0b538
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492181"
---
# <span data-ttu-id="91f05-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="91f05-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="91f05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91f05-102">SYNOPSIS</span></span>
<span data-ttu-id="91f05-103">Azure-webhely-helyreállítási szövetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="91f05-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91f05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91f05-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91f05-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91f05-105">DESCRIPTION</span></span>
<span data-ttu-id="91f05-106">A **New-AzureRmSiteRecoveryFabric** parancsmag a megadott típusú Azure webhely-helyreállítási szerkezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="91f05-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="91f05-107">Példák</span><span class="sxs-lookup"><span data-stu-id="91f05-107">EXAMPLES</span></span>

## <span data-ttu-id="91f05-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91f05-108">PARAMETERS</span></span>

### <span data-ttu-id="91f05-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f05-109">-DefaultProfile</span></span>
<span data-ttu-id="91f05-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91f05-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91f05-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91f05-111">-Name</span></span>
<span data-ttu-id="91f05-112">Az Azure webhely-helyreállítási anyag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91f05-112">Specifies the name of the Azure Site Recovery Fabric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f05-113">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="91f05-113">-Type</span></span>
<span data-ttu-id="91f05-114">Az Azure webhely-helyreállítási anyag típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91f05-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f05-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f05-115">CommonParameters</span></span>
<span data-ttu-id="91f05-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91f05-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f05-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f05-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f05-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91f05-118">INPUTS</span></span>

### <span data-ttu-id="91f05-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="91f05-119">None</span></span>
<span data-ttu-id="91f05-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="91f05-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91f05-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91f05-121">OUTPUTS</span></span>

### <span data-ttu-id="91f05-122">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="91f05-122">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="91f05-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91f05-123">NOTES</span></span>

## <span data-ttu-id="91f05-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91f05-124">RELATED LINKS</span></span>

[<span data-ttu-id="91f05-125">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="91f05-125">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="91f05-126">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="91f05-126">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
