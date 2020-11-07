---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 0a809f9ef3d3c89edc7571b9bb7b7cc2f03e043b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680501"
---
# <span data-ttu-id="4afe0-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="4afe0-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="4afe0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4afe0-102">SYNOPSIS</span></span>
<span data-ttu-id="4afe0-103">Megkapja az ASR-tároló beállításait a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="4afe0-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4afe0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4afe0-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [<CommonParameters>]
```

## <span data-ttu-id="4afe0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4afe0-105">DESCRIPTION</span></span>
<span data-ttu-id="4afe0-106">A **Get-AzureRmRecoveryServicesAsrVaultContext** PARANCSMAG az ASR Vault-beállításokkal kapcsolatos információkat kapja a helyreállítási szolgáltatások boltozatával kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="4afe0-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="4afe0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4afe0-107">EXAMPLES</span></span>

### <span data-ttu-id="4afe0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4afe0-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="4afe0-109">Beolvassa az ASR-tároló beállításait a jelenleg aktív (a PowerShell-munkamenetben) helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="4afe0-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="4afe0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4afe0-110">PARAMETERS</span></span>

### <span data-ttu-id="4afe0-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afe0-111">CommonParameters</span></span>
<span data-ttu-id="4afe0-112">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4afe0-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afe0-113">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4afe0-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afe0-114">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4afe0-114">INPUTS</span></span>

### <span data-ttu-id="4afe0-115">Nincs</span><span class="sxs-lookup"><span data-stu-id="4afe0-115">None</span></span>

## <span data-ttu-id="4afe0-116">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4afe0-116">OUTPUTS</span></span>

### <span data-ttu-id="4afe0-117">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="4afe0-117">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="4afe0-118">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4afe0-118">NOTES</span></span>

## <span data-ttu-id="4afe0-119">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4afe0-119">RELATED LINKS</span></span>

