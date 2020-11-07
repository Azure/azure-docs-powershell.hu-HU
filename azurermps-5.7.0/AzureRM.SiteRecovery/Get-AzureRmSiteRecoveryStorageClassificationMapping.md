---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: e04f5b71fe0cc5d6872c3bdf9cd18790f4e09f7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679683"
---
# <span data-ttu-id="76472-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="76472-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="76472-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76472-102">SYNOPSIS</span></span>
<span data-ttu-id="76472-103">Tároló besorolási megfeleltetést kap a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="76472-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76472-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76472-104">SYNTAX</span></span>

### <span data-ttu-id="76472-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76472-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76472-106">ByName</span><span class="sxs-lookup"><span data-stu-id="76472-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76472-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="76472-107">DESCRIPTION</span></span>
<span data-ttu-id="76472-108">A **Get-AzureRmSiteRecoveryStorageClassificationMapping** parancsmag az Azure webhely-helyreállítási szolgáltatásban kapja meg a tárolási osztályozási megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="76472-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="76472-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76472-109">EXAMPLES</span></span>

## <span data-ttu-id="76472-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76472-110">PARAMETERS</span></span>

### <span data-ttu-id="76472-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76472-111">-DefaultProfile</span></span>
<span data-ttu-id="76472-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76472-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76472-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76472-113">-Name</span></span>
<span data-ttu-id="76472-114">Itt adhatja meg annak a tárolási besorolási megfeleltetésnek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="76472-114">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76472-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76472-115">CommonParameters</span></span>
<span data-ttu-id="76472-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76472-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76472-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76472-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76472-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76472-118">INPUTS</span></span>

### <span data-ttu-id="76472-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="76472-119">None</span></span>
<span data-ttu-id="76472-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="76472-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76472-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76472-121">OUTPUTS</span></span>

### <span data-ttu-id="76472-122">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="76472-122">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="76472-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76472-123">NOTES</span></span>

## <span data-ttu-id="76472-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76472-124">RELATED LINKS</span></span>

[<span data-ttu-id="76472-125">Új – AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="76472-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="76472-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="76472-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
