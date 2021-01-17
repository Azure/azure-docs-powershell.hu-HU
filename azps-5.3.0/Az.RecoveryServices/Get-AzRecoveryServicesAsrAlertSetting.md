---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384479"
---
# <span data-ttu-id="21ee8-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="21ee8-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="21ee8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="21ee8-103">Beállítja az Azure Site Recovery értesítési beállításait a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="21ee8-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="21ee8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21ee8-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21ee8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21ee8-105">DESCRIPTION</span></span>
<span data-ttu-id="21ee8-106">A **Get-AzRecoveryServicesAsrAlertSetting parancsmag** megkapja a tárolóhoz konfigurált Azure-webhely-helyreállítási értesítési beállításokat.</span><span class="sxs-lookup"><span data-stu-id="21ee8-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="21ee8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21ee8-107">EXAMPLES</span></span>

### <span data-ttu-id="21ee8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="21ee8-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="21ee8-109">Értesítési/értesítési beállítás az Azure-webhely-helyreállításhoz.</span><span class="sxs-lookup"><span data-stu-id="21ee8-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="21ee8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21ee8-110">PARAMETERS</span></span>

### <span data-ttu-id="21ee8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ee8-111">-DefaultProfile</span></span>
<span data-ttu-id="21ee8-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21ee8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21ee8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ee8-113">CommonParameters</span></span>
<span data-ttu-id="21ee8-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ee8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ee8-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21ee8-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ee8-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21ee8-116">INPUTS</span></span>

### <span data-ttu-id="21ee8-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="21ee8-117">None</span></span>

## <span data-ttu-id="21ee8-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21ee8-118">OUTPUTS</span></span>

### <span data-ttu-id="21ee8-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="21ee8-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="21ee8-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21ee8-120">NOTES</span></span>

## <span data-ttu-id="21ee8-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21ee8-121">RELATED LINKS</span></span>
