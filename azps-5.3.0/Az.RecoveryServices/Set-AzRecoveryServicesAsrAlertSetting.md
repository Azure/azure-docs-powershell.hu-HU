---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466650"
---
# <span data-ttu-id="ef3dd-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ef3dd-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="ef3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ef3dd-103">Konfigurálja az Azure Site Recovery értesítési beállításait (e-mail-értesítés) a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ef3dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef3dd-104">SYNTAX</span></span>

### <span data-ttu-id="ef3dd-105">Beállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3dd-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ef3dd-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3dd-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ef3dd-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3dd-108">Letiltás</span><span class="sxs-lookup"><span data-stu-id="ef3dd-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef3dd-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef3dd-109">DESCRIPTION</span></span>
<span data-ttu-id="ef3dd-110">A **Set-AzRecoveryServicesAsrNotificationSetting** parancsmag konfigurálja az Azure Site Recovery értesítési beállításait (e-mail-értesítés) a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ef3dd-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef3dd-111">EXAMPLES</span></span>

### <span data-ttu-id="ef3dd-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="ef3dd-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="ef3dd-113">Értesítés letiltása.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-113">Disable notification.</span></span>

### <span data-ttu-id="ef3dd-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ef3dd-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="ef3dd-115">Értesítés beállítása az egyéni e-mail-címekhez és az előfizetés tulajdonosához.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="ef3dd-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="ef3dd-116">Example 3</span></span>

<span data-ttu-id="ef3dd-117">Konfigurálja az Azure Site Recovery értesítési beállításait (e-mail-értesítés) a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="ef3dd-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="ef3dd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef3dd-119">PARAMETERS</span></span>

### <span data-ttu-id="ef3dd-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ef3dd-120">-CustomEmailAddress</span></span>
<span data-ttu-id="ef3dd-121">E-mailekre küldött riasztás/értesítés.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="ef3dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef3dd-122">-DefaultProfile</span></span>
<span data-ttu-id="ef3dd-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef3dd-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ef3dd-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="ef3dd-125">A Kapcsoló paraméter az előfizetés tulajdonosának szóló értesítés engedélyezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="ef3dd-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="ef3dd-126">-DisableNotification</span></span>
<span data-ttu-id="ef3dd-127">Megjelölés az összes értesítés letiltásához.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="ef3dd-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ef3dd-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="ef3dd-129">A Kapcsoló paraméter az előfizetés tulajdonosának szóló értesítés engedélyezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="ef3dd-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="ef3dd-130">-LocaleID</span></span>
<span data-ttu-id="ef3dd-131">A felhasználónak szóló értesítések és értesítések e-mail-nyelve(a Microsoft által támogatott kulturális kódok).</span><span class="sxs-lookup"><span data-stu-id="ef3dd-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="ef3dd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef3dd-132">-Confirm</span></span>
<span data-ttu-id="ef3dd-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef3dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef3dd-134">-WhatIf</span></span>
<span data-ttu-id="ef3dd-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef3dd-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef3dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef3dd-137">CommonParameters</span></span>
<span data-ttu-id="ef3dd-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef3dd-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef3dd-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef3dd-140">INPUTS</span></span>

### <span data-ttu-id="ef3dd-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef3dd-141">None</span></span>

## <span data-ttu-id="ef3dd-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef3dd-142">OUTPUTS</span></span>

### <span data-ttu-id="ef3dd-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ef3dd-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="ef3dd-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef3dd-144">NOTES</span></span>

## <span data-ttu-id="ef3dd-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef3dd-145">RELATED LINKS</span></span>
