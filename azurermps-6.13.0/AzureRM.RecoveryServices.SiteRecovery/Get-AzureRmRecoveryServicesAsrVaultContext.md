---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 52535af7a2e7e9282a94c07f62154e42fe807a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502923"
---
# <span data-ttu-id="3e59a-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="3e59a-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="3e59a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e59a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e59a-103">Megkapja az ASR-tároló beállításait a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="3e59a-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e59a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e59a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e59a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e59a-105">DESCRIPTION</span></span>
<span data-ttu-id="3e59a-106">A **Get-AzureRmRecoveryServicesAsrVaultContext** PARANCSMAG az ASR Vault-beállításokkal kapcsolatos információkat kapja a helyreállítási szolgáltatások boltozatával kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="3e59a-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="3e59a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3e59a-107">EXAMPLES</span></span>

### <span data-ttu-id="3e59a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3e59a-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="3e59a-109">Beolvassa az ASR-tároló beállításait a jelenleg aktív (a PowerShell-munkamenetben) helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="3e59a-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="3e59a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e59a-110">PARAMETERS</span></span>

### <span data-ttu-id="3e59a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e59a-111">-DefaultProfile</span></span>
<span data-ttu-id="3e59a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e59a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e59a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e59a-113">CommonParameters</span></span>
<span data-ttu-id="3e59a-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e59a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e59a-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e59a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e59a-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e59a-116">INPUTS</span></span>

### <span data-ttu-id="3e59a-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="3e59a-117">None</span></span>

## <span data-ttu-id="3e59a-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e59a-118">OUTPUTS</span></span>

### <span data-ttu-id="3e59a-119">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="3e59a-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="3e59a-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e59a-120">NOTES</span></span>

## <span data-ttu-id="3e59a-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e59a-121">RELATED LINKS</span></span>
