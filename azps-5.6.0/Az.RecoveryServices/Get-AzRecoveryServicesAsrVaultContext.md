---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 62f27b43158f8b01abc7be48cab93f4bb957258b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921657"
---
# <span data-ttu-id="7d2ea-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="7d2ea-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="7d2ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2ea-103">A Helyreállítási szolgáltatások tárolóra vonatkozó ASR-tároló beállításainak adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7d2ea-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="7d2ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7d2ea-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d2ea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7d2ea-105">DESCRIPTION</span></span>
<span data-ttu-id="7d2ea-106">A **Get-AzRecoveryServicesAsrVaultContext parancsmag** asr tárolóbeállítási információkat kap a Helyreállítási szolgáltatások tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="7d2ea-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="7d2ea-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7d2ea-107">EXAMPLES</span></span>

### <span data-ttu-id="7d2ea-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7d2ea-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="7d2ea-109">Az aktuálisan aktív (a PowerShell-munkamenetben) helyreállítási szolgáltatások tárolója ASR-tárolóbeállítását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7d2ea-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="7d2ea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d2ea-110">PARAMETERS</span></span>

### <span data-ttu-id="7d2ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2ea-111">-DefaultProfile</span></span>
<span data-ttu-id="7d2ea-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d2ea-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2ea-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2ea-113">CommonParameters</span></span>
<span data-ttu-id="7d2ea-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d2ea-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2ea-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d2ea-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2ea-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d2ea-116">INPUTS</span></span>

### <span data-ttu-id="7d2ea-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="7d2ea-117">None</span></span>

## <span data-ttu-id="7d2ea-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d2ea-118">OUTPUTS</span></span>

### <span data-ttu-id="7d2ea-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="7d2ea-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="7d2ea-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7d2ea-120">NOTES</span></span>

## <span data-ttu-id="7d2ea-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d2ea-121">RELATED LINKS</span></span>
