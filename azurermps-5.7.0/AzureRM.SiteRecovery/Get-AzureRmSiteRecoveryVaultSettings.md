---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 56F63287-0247-4921-9C99-E581E075F4D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvaultsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: ef0ee9f4b2c068f5484932fa74da73e6f2a99585
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502387"
---
# <span data-ttu-id="3663e-101">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="3663e-101">Get-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="3663e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3663e-102">SYNOPSIS</span></span>
<span data-ttu-id="3663e-103">Az aktuális webhely-helyreállítási boltozat beállítási adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3663e-103">Gets settings information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3663e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3663e-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVaultSettings [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3663e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3663e-105">DESCRIPTION</span></span>
<span data-ttu-id="3663e-106">A **Get-AzureRmSiteRecoveryVaultSettings** parancsmag a jelenlegi Azure-webhely helyreállítási boltozatához kapcsolódó beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3663e-106">The **Get-AzureRmSiteRecoveryVaultSettings** cmdlet gets settings information related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="3663e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3663e-107">EXAMPLES</span></span>

## <span data-ttu-id="3663e-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3663e-108">PARAMETERS</span></span>

### <span data-ttu-id="3663e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3663e-109">-DefaultProfile</span></span>
<span data-ttu-id="3663e-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3663e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3663e-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3663e-111">CommonParameters</span></span>
<span data-ttu-id="3663e-112">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3663e-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3663e-113">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3663e-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3663e-114">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3663e-114">INPUTS</span></span>

### <span data-ttu-id="3663e-115">Nincs</span><span class="sxs-lookup"><span data-stu-id="3663e-115">None</span></span>
<span data-ttu-id="3663e-116">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3663e-116">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3663e-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3663e-117">OUTPUTS</span></span>

### <span data-ttu-id="3663e-118">Microsoft. Azure. Command. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="3663e-118">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="3663e-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3663e-119">NOTES</span></span>

## <span data-ttu-id="3663e-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3663e-120">RELATED LINKS</span></span>

[<span data-ttu-id="3663e-121">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="3663e-121">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)