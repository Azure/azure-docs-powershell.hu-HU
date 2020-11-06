---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 7f8dfed861abd9d426a72c5d66f7c41b4efc947e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493352"
---
# <span data-ttu-id="6d6e2-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="6d6e2-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="6d6e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6d6e2-103">Webhely-helyreállítási webhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d6e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d6e2-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d6e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d6e2-105">DESCRIPTION</span></span>
<span data-ttu-id="6d6e2-106">A **New-AzureRmSiteRecoverySite** parancsmag létrehoz egy Azure webhely-helyreállítási webhelyet az aktuális boltívben.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="6d6e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6d6e2-107">EXAMPLES</span></span>

## <span data-ttu-id="6d6e2-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d6e2-108">PARAMETERS</span></span>

### <span data-ttu-id="6d6e2-109">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6d6e2-109">-Name</span></span>
<span data-ttu-id="6d6e2-110">A webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-110">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d6e2-111">-DefaultProfile</span></span>
<span data-ttu-id="6d6e2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d6e2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d6e2-113">CommonParameters</span></span>
<span data-ttu-id="6d6e2-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d6e2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d6e2-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d6e2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d6e2-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d6e2-116">INPUTS</span></span>

## <span data-ttu-id="6d6e2-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d6e2-117">OUTPUTS</span></span>

## <span data-ttu-id="6d6e2-118">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d6e2-118">NOTES</span></span>

## <span data-ttu-id="6d6e2-119">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d6e2-119">RELATED LINKS</span></span>

[<span data-ttu-id="6d6e2-120">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="6d6e2-120">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="6d6e2-121">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="6d6e2-121">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
