---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2d215afda7c2c26aa178421fb52ddaff8c6ac831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498779"
---
# <span data-ttu-id="c501e-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c501e-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="c501e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c501e-102">SYNOPSIS</span></span>
<span data-ttu-id="c501e-103">Eltávolít egy tárterület-osztályozási megfeleltetést a webhely-helyreállításból.</span><span class="sxs-lookup"><span data-stu-id="c501e-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c501e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c501e-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c501e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c501e-105">DESCRIPTION</span></span>
<span data-ttu-id="c501e-106">A **Remove-AzureRmSiteRecoveryStorageClassificationMapping** parancsmag eltávolítja az Azure webhely-helyreállításból származó tárterület-osztályozási megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="c501e-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="c501e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c501e-107">EXAMPLES</span></span>

## <span data-ttu-id="c501e-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c501e-108">PARAMETERS</span></span>

### <span data-ttu-id="c501e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c501e-109">-DefaultProfile</span></span>
<span data-ttu-id="c501e-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c501e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c501e-111">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c501e-111">-StorageClassificationMapping</span></span>
<span data-ttu-id="c501e-112">A parancsmag által eltávolított tárolási besorolási megfeleltetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="c501e-112">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c501e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c501e-113">CommonParameters</span></span>
<span data-ttu-id="c501e-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c501e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c501e-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c501e-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c501e-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c501e-116">INPUTS</span></span>

### <span data-ttu-id="c501e-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c501e-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="c501e-118">A ' StorageClassificationMapping ' paraméter az "ASRStorageClassificationMapping" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c501e-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="c501e-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c501e-119">OUTPUTS</span></span>

### <span data-ttu-id="c501e-120">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c501e-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c501e-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c501e-121">NOTES</span></span>

## <span data-ttu-id="c501e-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c501e-122">RELATED LINKS</span></span>

[<span data-ttu-id="c501e-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c501e-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="c501e-124">Új – AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c501e-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
