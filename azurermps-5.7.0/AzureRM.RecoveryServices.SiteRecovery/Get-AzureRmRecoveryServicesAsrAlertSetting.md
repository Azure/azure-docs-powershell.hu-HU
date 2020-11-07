---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: d1da03455fad47d889269c0d961def70df6837e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678957"
---
# <span data-ttu-id="00167-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="00167-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="00167-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00167-102">SYNOPSIS</span></span>
<span data-ttu-id="00167-103">Beilleszti a beállított Azure-webhely helyreállítási értesítési beállításait a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="00167-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00167-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00167-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00167-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="00167-105">DESCRIPTION</span></span>
<span data-ttu-id="00167-106">A **Get-AzureRmRecoveryServicesAsrAlertSetting** parancsmag a beállított Azure-webhely helyreállítási értesítési beállításait kapja meg a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="00167-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="00167-107">Példák</span><span class="sxs-lookup"><span data-stu-id="00167-107">EXAMPLES</span></span>

### <span data-ttu-id="00167-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00167-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="00167-109">Értesítési/értesítési beállítás kérése az Azure webhely-helyreállításhoz.</span><span class="sxs-lookup"><span data-stu-id="00167-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="00167-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00167-110">PARAMETERS</span></span>

### <span data-ttu-id="00167-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00167-111">-DefaultProfile</span></span>
<span data-ttu-id="00167-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00167-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00167-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00167-113">CommonParameters</span></span>
<span data-ttu-id="00167-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00167-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00167-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00167-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00167-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00167-116">INPUTS</span></span>

### <span data-ttu-id="00167-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="00167-117">None</span></span>

## <span data-ttu-id="00167-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00167-118">OUTPUTS</span></span>

### <span data-ttu-id="00167-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="00167-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="00167-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00167-120">NOTES</span></span>

## <span data-ttu-id="00167-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00167-121">RELATED LINKS</span></span>
