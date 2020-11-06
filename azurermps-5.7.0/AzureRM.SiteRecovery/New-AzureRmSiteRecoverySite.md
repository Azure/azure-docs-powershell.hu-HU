---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 053cd7695768be44cf3cecc5964e037f12f0b84e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498783"
---
# <span data-ttu-id="346ca-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="346ca-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="346ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="346ca-102">SYNOPSIS</span></span>
<span data-ttu-id="346ca-103">Webhely-helyreállítási webhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="346ca-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="346ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="346ca-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="346ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="346ca-105">DESCRIPTION</span></span>
<span data-ttu-id="346ca-106">A **New-AzureRmSiteRecoverySite** parancsmag létrehoz egy Azure webhely-helyreállítási webhelyet az aktuális boltívben.</span><span class="sxs-lookup"><span data-stu-id="346ca-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="346ca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="346ca-107">EXAMPLES</span></span>

## <span data-ttu-id="346ca-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="346ca-108">PARAMETERS</span></span>

### <span data-ttu-id="346ca-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="346ca-109">-DefaultProfile</span></span>
<span data-ttu-id="346ca-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="346ca-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="346ca-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="346ca-111">-Name</span></span>
<span data-ttu-id="346ca-112">A webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="346ca-112">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="346ca-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="346ca-113">CommonParameters</span></span>
<span data-ttu-id="346ca-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="346ca-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="346ca-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="346ca-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="346ca-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="346ca-116">INPUTS</span></span>

### <span data-ttu-id="346ca-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="346ca-117">None</span></span>
<span data-ttu-id="346ca-118">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="346ca-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="346ca-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="346ca-119">OUTPUTS</span></span>

## <span data-ttu-id="346ca-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="346ca-120">NOTES</span></span>

## <span data-ttu-id="346ca-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="346ca-121">RELATED LINKS</span></span>

[<span data-ttu-id="346ca-122">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="346ca-122">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="346ca-123">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="346ca-123">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
