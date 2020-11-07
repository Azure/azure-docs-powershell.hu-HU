---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 21106b2c5a8e36f58b6593049fccf28994b0af46
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838539"
---
# <span data-ttu-id="39de5-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="39de5-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="39de5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39de5-102">SYNOPSIS</span></span>
<span data-ttu-id="39de5-103">Az Azure webhely-helyreállítási értesítési beállításainak (értesítő e-mail-értesítés) beállítása a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="39de5-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="39de5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39de5-104">SYNTAX</span></span>

### <span data-ttu-id="39de5-105">Set (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39de5-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39de5-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="39de5-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39de5-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="39de5-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39de5-108">Megbénít</span><span class="sxs-lookup"><span data-stu-id="39de5-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39de5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="39de5-109">DESCRIPTION</span></span>
<span data-ttu-id="39de5-110">A **set-AzRecoveryServicesAsrNotificationSetting** parancsmag az Azure webhely-helyreállítási értesítési beállításait (e-mail-értesítést) állítja be a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="39de5-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="39de5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="39de5-111">EXAMPLES</span></span>

### <span data-ttu-id="39de5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="39de5-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="39de5-113">Tiltsa le az értesítést.</span><span class="sxs-lookup"><span data-stu-id="39de5-113">Disable notification.</span></span>

### <span data-ttu-id="39de5-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="39de5-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="39de5-115">Az egyéni e-mail-cím (ek) és az előfizetéses tulajdonos értesítésének beállítása</span><span class="sxs-lookup"><span data-stu-id="39de5-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="39de5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39de5-116">PARAMETERS</span></span>

### <span data-ttu-id="39de5-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="39de5-117">-CustomEmailAddress</span></span>
<span data-ttu-id="39de5-118">Értesítés/értesítés e-mailekhez.</span><span class="sxs-lookup"><span data-stu-id="39de5-118">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="39de5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39de5-119">-DefaultProfile</span></span>
<span data-ttu-id="39de5-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39de5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39de5-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="39de5-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="39de5-122">Kapcsoló paraméter: Itt adhatja meg, hogy az előfizetés tulajdonosának engedélyezze az értesítést.</span><span class="sxs-lookup"><span data-stu-id="39de5-122">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="39de5-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="39de5-123">-DisableNotification</span></span>
<span data-ttu-id="39de5-124">Megjelölés az összes értesítés letiltásához.</span><span class="sxs-lookup"><span data-stu-id="39de5-124">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="39de5-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="39de5-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="39de5-126">Kapcsoló paraméter: Itt adhatja meg, hogy az előfizetés tulajdonosának engedélyezze az értesítést.</span><span class="sxs-lookup"><span data-stu-id="39de5-126">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="39de5-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="39de5-127">-LocaleID</span></span>
<span data-ttu-id="39de5-128">Az értesítési/Notification a felhasználó (támogatott kulturális kódok a Microsofttól) levelezési nyelve.</span><span class="sxs-lookup"><span data-stu-id="39de5-128">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="39de5-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39de5-129">-Confirm</span></span>
<span data-ttu-id="39de5-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39de5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39de5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39de5-131">-WhatIf</span></span>
<span data-ttu-id="39de5-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39de5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39de5-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39de5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39de5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39de5-134">CommonParameters</span></span>
<span data-ttu-id="39de5-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39de5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39de5-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39de5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39de5-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39de5-137">INPUTS</span></span>

### <span data-ttu-id="39de5-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="39de5-138">None</span></span>

## <span data-ttu-id="39de5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39de5-139">OUTPUTS</span></span>

### <span data-ttu-id="39de5-140">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="39de5-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="39de5-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39de5-141">NOTES</span></span>

## <span data-ttu-id="39de5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39de5-142">RELATED LINKS</span></span>
