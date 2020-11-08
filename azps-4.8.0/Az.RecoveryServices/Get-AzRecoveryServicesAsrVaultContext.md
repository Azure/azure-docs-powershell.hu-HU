---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182191"
---
# <span data-ttu-id="d3da5-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="d3da5-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="d3da5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3da5-102">SYNOPSIS</span></span>
<span data-ttu-id="d3da5-103">Megkapja az ASR-tároló beállításait a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="d3da5-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="d3da5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3da5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3da5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3da5-105">DESCRIPTION</span></span>
<span data-ttu-id="d3da5-106">A **Get-AzRecoveryServicesAsrVaultContext** PARANCSMAG az ASR Vault-beállításokkal kapcsolatos információkat kapja a helyreállítási szolgáltatások boltozatával kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="d3da5-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="d3da5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d3da5-107">EXAMPLES</span></span>

### <span data-ttu-id="d3da5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3da5-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="d3da5-109">Beolvassa az ASR-tároló beállításait a jelenleg aktív (a PowerShell-munkamenetben) helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="d3da5-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="d3da5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3da5-110">PARAMETERS</span></span>

### <span data-ttu-id="d3da5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3da5-111">-DefaultProfile</span></span>
<span data-ttu-id="d3da5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3da5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3da5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3da5-113">CommonParameters</span></span>
<span data-ttu-id="d3da5-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3da5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3da5-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3da5-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3da5-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3da5-116">INPUTS</span></span>

### <span data-ttu-id="d3da5-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3da5-117">None</span></span>

## <span data-ttu-id="d3da5-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3da5-118">OUTPUTS</span></span>

### <span data-ttu-id="d3da5-119">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="d3da5-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="d3da5-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3da5-120">NOTES</span></span>

## <span data-ttu-id="d3da5-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3da5-121">RELATED LINKS</span></span>
