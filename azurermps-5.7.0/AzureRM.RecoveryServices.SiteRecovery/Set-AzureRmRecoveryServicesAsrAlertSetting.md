---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 4e51cd90e490442c36b5864e53b4bb7a36e41e80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495298"
---
# <span data-ttu-id="8338d-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="8338d-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="8338d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8338d-102">SYNOPSIS</span></span>
<span data-ttu-id="8338d-103">Az Azure webhely-helyreállítási értesítési beállításainak (értesítő e-mail-értesítés) beállítása a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="8338d-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8338d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8338d-104">SYNTAX</span></span>

### <span data-ttu-id="8338d-105">Set (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8338d-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8338d-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="8338d-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8338d-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="8338d-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8338d-108">Megbénít</span><span class="sxs-lookup"><span data-stu-id="8338d-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8338d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="8338d-109">DESCRIPTION</span></span>
<span data-ttu-id="8338d-110">A **set-AzureRmRecoveryServicesAsrNotificationSetting** parancsmag az Azure webhely-helyreállítási értesítési beállításait (e-mail-értesítést) állítja be a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="8338d-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="8338d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8338d-111">EXAMPLES</span></span>

### <span data-ttu-id="8338d-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8338d-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="8338d-113">Tiltsa le az értesítést.</span><span class="sxs-lookup"><span data-stu-id="8338d-113">Disable notification.</span></span>

### <span data-ttu-id="8338d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="8338d-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="8338d-115">Az egyéni e-mail-cím (ek) és az előfizetéses tulajdonos értesítésének beállítása</span><span class="sxs-lookup"><span data-stu-id="8338d-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="8338d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8338d-116">PARAMETERS</span></span>

### <span data-ttu-id="8338d-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8338d-117">-Confirm</span></span>
<span data-ttu-id="8338d-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8338d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8338d-119">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8338d-119">-CustomEmailAddress</span></span>
<span data-ttu-id="8338d-120">Értesítés/értesítés e-mailekhez.</span><span class="sxs-lookup"><span data-stu-id="8338d-120">Alert / Notification sent to emails.</span></span>

```yaml
Type: String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8338d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8338d-121">-DefaultProfile</span></span>
<span data-ttu-id="8338d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8338d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8338d-123">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="8338d-123">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="8338d-124">Kapcsoló paraméter: Itt adhatja meg, hogy az előfizetés tulajdonosának engedélyezze az értesítést.</span><span class="sxs-lookup"><span data-stu-id="8338d-124">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8338d-125">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="8338d-125">-DisableNotification</span></span>
<span data-ttu-id="8338d-126">Megjelölés az összes értesítés letiltásához.</span><span class="sxs-lookup"><span data-stu-id="8338d-126">Flag to disable all notification.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8338d-127">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="8338d-127">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="8338d-128">Váltás a paraméter-ra: az értesítés engedélyezése az előfizetés tulajdonosának.</span><span class="sxs-lookup"><span data-stu-id="8338d-128">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8338d-129">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="8338d-129">-LocaleID</span></span>
<span data-ttu-id="8338d-130">Az értesítési/notifcation a felhasználó (támogatott kulturális kódok a Microsofttól) levelezési nyelve.</span><span class="sxs-lookup"><span data-stu-id="8338d-130">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8338d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8338d-131">-WhatIf</span></span>
<span data-ttu-id="8338d-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8338d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8338d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8338d-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8338d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8338d-134">CommonParameters</span></span>
<span data-ttu-id="8338d-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8338d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8338d-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8338d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8338d-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8338d-137">INPUTS</span></span>

### <span data-ttu-id="8338d-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="8338d-138">None</span></span>

## <span data-ttu-id="8338d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8338d-139">OUTPUTS</span></span>

### <span data-ttu-id="8338d-140">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 0.1.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8338d-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8338d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8338d-141">NOTES</span></span>

## <span data-ttu-id="8338d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8338d-142">RELATED LINKS</span></span>
