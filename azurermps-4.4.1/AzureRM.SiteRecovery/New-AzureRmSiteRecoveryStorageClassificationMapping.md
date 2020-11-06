---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2520dd90eed1362f4d499eb88ce88dec33f1338c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493349"
---
# <span data-ttu-id="751e5-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="751e5-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="751e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="751e5-102">SYNOPSIS</span></span>
<span data-ttu-id="751e5-103">Tárolási besorolási megfeleltetést hoz létre a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="751e5-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="751e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="751e5-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="751e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="751e5-105">DESCRIPTION</span></span>
<span data-ttu-id="751e5-106">A **New-AzureRmSiteRecoveryStorageClassificationMapping** parancsmag létrehoz egy tárterület-osztályozási megfeleltetést az Azure webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="751e5-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="751e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="751e5-107">EXAMPLES</span></span>

## <span data-ttu-id="751e5-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="751e5-108">PARAMETERS</span></span>

### <span data-ttu-id="751e5-109">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="751e5-109">-Name</span></span>
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

### <span data-ttu-id="751e5-110">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="751e5-110">-PrimaryStorageClassification</span></span>
<span data-ttu-id="751e5-111">Az elsődleges tárterület-osztályozási megfeleltetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="751e5-111">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="751e5-112">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="751e5-112">-RecoveryStorageClassification</span></span>
<span data-ttu-id="751e5-113">A helyreállítási tárterület osztályozási megfeleltetését adja meg.</span><span class="sxs-lookup"><span data-stu-id="751e5-113">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="751e5-114">-DefaultProfile</span></span>
<span data-ttu-id="751e5-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="751e5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="751e5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="751e5-116">CommonParameters</span></span>
<span data-ttu-id="751e5-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="751e5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="751e5-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="751e5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="751e5-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="751e5-119">INPUTS</span></span>

### <span data-ttu-id="751e5-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="751e5-120">ASRStorageClassification</span></span>
<span data-ttu-id="751e5-121">A ' PrimaryStorageClassification ' paraméter az "ASRStorageClassification" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="751e5-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="751e5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="751e5-122">OUTPUTS</span></span>

### <span data-ttu-id="751e5-123">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="751e5-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="751e5-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="751e5-124">NOTES</span></span>

## <span data-ttu-id="751e5-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="751e5-125">RELATED LINKS</span></span>

[<span data-ttu-id="751e5-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="751e5-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="751e5-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="751e5-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
