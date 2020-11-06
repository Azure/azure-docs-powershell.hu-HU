---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 86d8cc4b48342b49e807635e6fb51c5f4028b172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494330"
---
# <span data-ttu-id="c16c0-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c16c0-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="c16c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c16c0-102">SYNOPSIS</span></span>
<span data-ttu-id="c16c0-103">Tárolási besorolási megfeleltetést hoz létre a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="c16c0-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c16c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c16c0-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c16c0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c16c0-105">DESCRIPTION</span></span>
<span data-ttu-id="c16c0-106">A **New-AzureRmSiteRecoveryStorageClassificationMapping** parancsmag létrehoz egy tárterület-osztályozási megfeleltetést az Azure webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="c16c0-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="c16c0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c16c0-107">EXAMPLES</span></span>

## <span data-ttu-id="c16c0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c16c0-108">PARAMETERS</span></span>

### <span data-ttu-id="c16c0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16c0-109">-DefaultProfile</span></span>
<span data-ttu-id="c16c0-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c16c0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c16c0-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c16c0-111">-Name</span></span>
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

### <span data-ttu-id="c16c0-112">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c16c0-112">-PrimaryStorageClassification</span></span>
<span data-ttu-id="c16c0-113">Az elsődleges tárterület-osztályozási megfeleltetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="c16c0-113">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c16c0-114">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c16c0-114">-RecoveryStorageClassification</span></span>
<span data-ttu-id="c16c0-115">A helyreállítási tárterület osztályozási megfeleltetését adja meg.</span><span class="sxs-lookup"><span data-stu-id="c16c0-115">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16c0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16c0-116">CommonParameters</span></span>
<span data-ttu-id="c16c0-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c16c0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16c0-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16c0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16c0-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c16c0-119">INPUTS</span></span>

### <span data-ttu-id="c16c0-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c16c0-120">ASRStorageClassification</span></span>
<span data-ttu-id="c16c0-121">A ' PrimaryStorageClassification ' paraméter az "ASRStorageClassification" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c16c0-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="c16c0-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c16c0-122">OUTPUTS</span></span>

### <span data-ttu-id="c16c0-123">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c16c0-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c16c0-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c16c0-124">NOTES</span></span>

## <span data-ttu-id="c16c0-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c16c0-125">RELATED LINKS</span></span>

[<span data-ttu-id="c16c0-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c16c0-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="c16c0-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c16c0-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
