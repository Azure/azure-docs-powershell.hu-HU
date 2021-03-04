---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 049e1667fec5aef4f12a9912a4b9669364095b0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942289"
---
# <span data-ttu-id="3cfe8-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="3cfe8-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="3cfe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cfe8-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfe8-103">Konfigurálja az Azure Site Recovery értesítési beállításait (e-mail-értesítés) a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="3cfe8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3cfe8-104">SYNTAX</span></span>

### <span data-ttu-id="3cfe8-105">Beállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3cfe8-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfe8-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3cfe8-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfe8-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3cfe8-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfe8-108">Letiltás</span><span class="sxs-lookup"><span data-stu-id="3cfe8-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cfe8-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3cfe8-109">DESCRIPTION</span></span>
<span data-ttu-id="3cfe8-110">A **Set-AzRecoveryServicesAsrNotificationSetting** parancsmag konfigurálja az Azure Site Recovery értesítési beállításait (e-mail-értesítés) a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="3cfe8-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3cfe8-111">EXAMPLES</span></span>

### <span data-ttu-id="3cfe8-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3cfe8-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="3cfe8-113">Értesítés letiltása.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-113">Disable notification.</span></span>

### <span data-ttu-id="3cfe8-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3cfe8-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="3cfe8-115">Értesítés beállítása az egyéni e-mail-címekhez és az előfizetés tulajdonosához.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="3cfe8-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="3cfe8-116">Example 3</span></span>

<span data-ttu-id="3cfe8-117">Konfigurálja az Azure Site Recovery értesítési beállításait (e-mail-értesítés) a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="3cfe8-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="3cfe8-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="3cfe8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cfe8-119">PARAMETERS</span></span>

### <span data-ttu-id="3cfe8-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3cfe8-120">-CustomEmailAddress</span></span>
<span data-ttu-id="3cfe8-121">E-mailekre küldött riasztás/értesítés.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="3cfe8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cfe8-122">-DefaultProfile</span></span>
<span data-ttu-id="3cfe8-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cfe8-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3cfe8-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="3cfe8-125">A Kapcsoló paraméter az előfizetés tulajdonosának szóló értesítés engedélyezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="3cfe8-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="3cfe8-126">-DisableNotification</span></span>
<span data-ttu-id="3cfe8-127">Megjelölés az összes értesítés letiltásához.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="3cfe8-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3cfe8-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="3cfe8-129">A Kapcsoló paraméter az előfizetés tulajdonosának szóló értesítés engedélyezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="3cfe8-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="3cfe8-130">-LocaleID</span></span>
<span data-ttu-id="3cfe8-131">A felhasználónak szóló értesítések és értesítések e-mail-nyelve(a Microsoft által támogatott kultúrkódok).</span><span class="sxs-lookup"><span data-stu-id="3cfe8-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="3cfe8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cfe8-132">-Confirm</span></span>
<span data-ttu-id="3cfe8-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cfe8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cfe8-134">-WhatIf</span></span>
<span data-ttu-id="3cfe8-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cfe8-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cfe8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfe8-137">CommonParameters</span></span>
<span data-ttu-id="3cfe8-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cfe8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfe8-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cfe8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfe8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cfe8-140">INPUTS</span></span>

### <span data-ttu-id="3cfe8-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="3cfe8-141">None</span></span>

## <span data-ttu-id="3cfe8-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cfe8-142">OUTPUTS</span></span>

### <span data-ttu-id="3cfe8-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="3cfe8-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="3cfe8-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3cfe8-144">NOTES</span></span>

## <span data-ttu-id="3cfe8-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cfe8-145">RELATED LINKS</span></span>
