---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301250"
---
# <span data-ttu-id="9e68c-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9e68c-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="9e68c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e68c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e68c-103">Beilleszti a beállított Azure-webhely helyreállítási értesítési beállításait a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="9e68c-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="9e68c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e68c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e68c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e68c-105">DESCRIPTION</span></span>
<span data-ttu-id="9e68c-106">A **Get-AzRecoveryServicesAsrAlertSetting** parancsmag a beállított Azure-webhely helyreállítási értesítési beállításait kapja meg a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="9e68c-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="9e68c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e68c-107">EXAMPLES</span></span>

### <span data-ttu-id="9e68c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9e68c-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="9e68c-109">Értesítési/értesítési beállítás kérése az Azure webhely-helyreállításhoz.</span><span class="sxs-lookup"><span data-stu-id="9e68c-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="9e68c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e68c-110">PARAMETERS</span></span>

### <span data-ttu-id="9e68c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e68c-111">-DefaultProfile</span></span>
<span data-ttu-id="9e68c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e68c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e68c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e68c-113">CommonParameters</span></span>
<span data-ttu-id="9e68c-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e68c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e68c-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9e68c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e68c-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e68c-116">INPUTS</span></span>

### <span data-ttu-id="9e68c-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="9e68c-117">None</span></span>

## <span data-ttu-id="9e68c-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e68c-118">OUTPUTS</span></span>

### <span data-ttu-id="9e68c-119">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9e68c-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="9e68c-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e68c-120">NOTES</span></span>

## <span data-ttu-id="9e68c-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e68c-121">RELATED LINKS</span></span>
