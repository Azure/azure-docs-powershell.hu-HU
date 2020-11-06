---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 70816649b33cd91c7d378b3588b443e4dd5b8fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495751"
---
# <span data-ttu-id="e50ae-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="e50ae-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="e50ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e50ae-102">SYNOPSIS</span></span>
<span data-ttu-id="e50ae-103">Az Azure webhely-helyreállítási értesítési beállításainak (értesítő e-mail-értesítés) beállítása a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="e50ae-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e50ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e50ae-104">SYNTAX</span></span>

### <span data-ttu-id="e50ae-105">Set (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e50ae-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e50ae-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="e50ae-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e50ae-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="e50ae-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e50ae-108">Megbénít</span><span class="sxs-lookup"><span data-stu-id="e50ae-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e50ae-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e50ae-109">DESCRIPTION</span></span>
<span data-ttu-id="e50ae-110">A **set-AzureRmRecoveryServicesAsrNotificationSetting** parancsmag az Azure webhely-helyreállítási értesítési beállításait (e-mail-értesítést) állítja be a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="e50ae-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="e50ae-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e50ae-111">EXAMPLES</span></span>

### <span data-ttu-id="e50ae-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e50ae-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="e50ae-113">Tiltsa le az értesítést.</span><span class="sxs-lookup"><span data-stu-id="e50ae-113">Disable notification.</span></span>

### <span data-ttu-id="e50ae-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e50ae-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="e50ae-115">Az egyéni e-mail-cím (ek) és az előfizetéses tulajdonos értesítésének beállítása</span><span class="sxs-lookup"><span data-stu-id="e50ae-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="e50ae-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e50ae-116">PARAMETERS</span></span>

### <span data-ttu-id="e50ae-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e50ae-117">-CustomEmailAddress</span></span>
<span data-ttu-id="e50ae-118">Értesítés/értesítés e-mailekhez.</span><span class="sxs-lookup"><span data-stu-id="e50ae-118">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50ae-119">-DefaultProfile</span></span>
<span data-ttu-id="e50ae-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e50ae-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e50ae-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="e50ae-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="e50ae-122">Kapcsoló paraméter: Itt adhatja meg, hogy az előfizetés tulajdonosának engedélyezze az értesítést.</span><span class="sxs-lookup"><span data-stu-id="e50ae-122">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50ae-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="e50ae-123">-DisableNotification</span></span>
<span data-ttu-id="e50ae-124">Megjelölés az összes értesítés letiltásához.</span><span class="sxs-lookup"><span data-stu-id="e50ae-124">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50ae-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="e50ae-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="e50ae-126">Váltás a paraméter-ra: az értesítés engedélyezése az előfizetés tulajdonosának.</span><span class="sxs-lookup"><span data-stu-id="e50ae-126">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50ae-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="e50ae-127">-LocaleID</span></span>
<span data-ttu-id="e50ae-128">Az értesítési/notifcation a felhasználó (támogatott kulturális kódok a Microsofttól) levelezési nyelve.</span><span class="sxs-lookup"><span data-stu-id="e50ae-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50ae-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e50ae-129">-Confirm</span></span>
<span data-ttu-id="e50ae-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e50ae-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50ae-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e50ae-131">-WhatIf</span></span>
<span data-ttu-id="e50ae-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e50ae-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e50ae-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e50ae-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50ae-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50ae-134">CommonParameters</span></span>
<span data-ttu-id="e50ae-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e50ae-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50ae-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50ae-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50ae-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e50ae-137">INPUTS</span></span>

### <span data-ttu-id="e50ae-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="e50ae-138">None</span></span>

## <span data-ttu-id="e50ae-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e50ae-139">OUTPUTS</span></span>

### <span data-ttu-id="e50ae-140">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 0.1.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e50ae-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e50ae-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e50ae-141">NOTES</span></span>

## <span data-ttu-id="e50ae-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e50ae-142">RELATED LINKS</span></span>
