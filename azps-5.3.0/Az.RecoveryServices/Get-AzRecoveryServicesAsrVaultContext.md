---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476733"
---
# <span data-ttu-id="60105-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="60105-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="60105-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60105-102">SYNOPSIS</span></span>
<span data-ttu-id="60105-103">A Helyreállítási szolgáltatások tárolóra vonatkozó ASR-tároló beállításainak adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="60105-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="60105-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60105-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60105-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60105-105">DESCRIPTION</span></span>
<span data-ttu-id="60105-106">A **Get-AzRecoveryServicesAsrVaultContext parancsmag** asr tárolóbeállítási információkat kap a Helyreállítási szolgáltatások tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="60105-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="60105-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60105-107">EXAMPLES</span></span>

### <span data-ttu-id="60105-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="60105-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="60105-109">Az aktuálisan aktív (a PowerShell-munkamenetben) helyreállítási szolgáltatások tárolója ASR-tárolóbeállítását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="60105-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="60105-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60105-110">PARAMETERS</span></span>

### <span data-ttu-id="60105-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60105-111">-DefaultProfile</span></span>
<span data-ttu-id="60105-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60105-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60105-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60105-113">CommonParameters</span></span>
<span data-ttu-id="60105-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60105-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60105-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60105-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60105-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60105-116">INPUTS</span></span>

### <span data-ttu-id="60105-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="60105-117">None</span></span>

## <span data-ttu-id="60105-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60105-118">OUTPUTS</span></span>

### <span data-ttu-id="60105-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="60105-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="60105-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60105-120">NOTES</span></span>

## <span data-ttu-id="60105-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60105-121">RELATED LINKS</span></span>
