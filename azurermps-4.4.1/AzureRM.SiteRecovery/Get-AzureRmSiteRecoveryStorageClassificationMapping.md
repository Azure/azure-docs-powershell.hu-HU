---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 1c8d061dae3d2334b422e6f9e4e3c2b7bb75abcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503175"
---
# <span data-ttu-id="d289a-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d289a-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="d289a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d289a-102">SYNOPSIS</span></span>
<span data-ttu-id="d289a-103">Tároló besorolási megfeleltetést kap a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="d289a-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d289a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d289a-104">SYNTAX</span></span>

### <span data-ttu-id="d289a-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d289a-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d289a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d289a-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d289a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d289a-107">DESCRIPTION</span></span>
<span data-ttu-id="d289a-108">A **Get-AzureRmSiteRecoveryStorageClassificationMapping** parancsmag az Azure webhely-helyreállítási szolgáltatásban kapja meg a tárolási osztályozási megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="d289a-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="d289a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d289a-109">EXAMPLES</span></span>

## <span data-ttu-id="d289a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d289a-110">PARAMETERS</span></span>

### <span data-ttu-id="d289a-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d289a-111">-Name</span></span>
<span data-ttu-id="d289a-112">Itt adhatja meg annak a tárolási besorolási megfeleltetésnek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d289a-112">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d289a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d289a-113">-DefaultProfile</span></span>
<span data-ttu-id="d289a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d289a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d289a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d289a-115">CommonParameters</span></span>
<span data-ttu-id="d289a-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d289a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d289a-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d289a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d289a-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d289a-118">INPUTS</span></span>

## <span data-ttu-id="d289a-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d289a-119">OUTPUTS</span></span>

### <span data-ttu-id="d289a-120">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="d289a-120">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="d289a-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d289a-121">NOTES</span></span>

## <span data-ttu-id="d289a-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d289a-122">RELATED LINKS</span></span>

[<span data-ttu-id="d289a-123">Új – AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d289a-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="d289a-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d289a-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
