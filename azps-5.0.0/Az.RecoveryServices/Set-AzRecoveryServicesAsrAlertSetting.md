---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188219"
---
# <span data-ttu-id="d4b49-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="d4b49-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="d4b49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4b49-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b49-103">Az Azure webhely-helyreállítási értesítési beállításainak (értesítő e-mail-értesítés) beállítása a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="d4b49-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="d4b49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4b49-104">SYNTAX</span></span>

### <span data-ttu-id="d4b49-105">Set (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4b49-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b49-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="d4b49-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b49-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="d4b49-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b49-108">Megbénít</span><span class="sxs-lookup"><span data-stu-id="d4b49-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4b49-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4b49-109">DESCRIPTION</span></span>
<span data-ttu-id="d4b49-110">A **set-AzRecoveryServicesAsrNotificationSetting** parancsmag az Azure webhely-helyreállítási értesítési beállításait (e-mail-értesítést) állítja be a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="d4b49-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="d4b49-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d4b49-111">EXAMPLES</span></span>

### <span data-ttu-id="d4b49-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4b49-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="d4b49-113">Tiltsa le az értesítést.</span><span class="sxs-lookup"><span data-stu-id="d4b49-113">Disable notification.</span></span>

### <span data-ttu-id="d4b49-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4b49-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="d4b49-115">Az egyéni e-mail-cím (ek) és az előfizetéses tulajdonos értesítésének beállítása</span><span class="sxs-lookup"><span data-stu-id="d4b49-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="d4b49-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="d4b49-116">Example 3</span></span>

<span data-ttu-id="d4b49-117">Az Azure webhely-helyreállítási értesítési beállításainak (értesítő e-mail-értesítés) beállítása a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="d4b49-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="d4b49-118">autogenerated</span><span class="sxs-lookup"><span data-stu-id="d4b49-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="d4b49-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4b49-119">PARAMETERS</span></span>

### <span data-ttu-id="d4b49-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d4b49-120">-CustomEmailAddress</span></span>
<span data-ttu-id="d4b49-121">Értesítés/értesítés e-mailekhez.</span><span class="sxs-lookup"><span data-stu-id="d4b49-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="d4b49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b49-122">-DefaultProfile</span></span>
<span data-ttu-id="d4b49-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4b49-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4b49-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="d4b49-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="d4b49-125">Kapcsoló paraméter: Itt adhatja meg, hogy az előfizetés tulajdonosának engedélyezze az értesítést.</span><span class="sxs-lookup"><span data-stu-id="d4b49-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="d4b49-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="d4b49-126">-DisableNotification</span></span>
<span data-ttu-id="d4b49-127">Megjelölés az összes értesítés letiltásához.</span><span class="sxs-lookup"><span data-stu-id="d4b49-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="d4b49-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="d4b49-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="d4b49-129">Kapcsoló paraméter: Itt adhatja meg, hogy az előfizetés tulajdonosának engedélyezze az értesítést.</span><span class="sxs-lookup"><span data-stu-id="d4b49-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="d4b49-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="d4b49-130">-LocaleID</span></span>
<span data-ttu-id="d4b49-131">Az értesítési/Notification a felhasználó (támogatott kulturális kódok a Microsofttól) levelezési nyelve.</span><span class="sxs-lookup"><span data-stu-id="d4b49-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="d4b49-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4b49-132">-Confirm</span></span>
<span data-ttu-id="d4b49-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4b49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4b49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b49-134">-WhatIf</span></span>
<span data-ttu-id="d4b49-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4b49-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4b49-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4b49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4b49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b49-137">CommonParameters</span></span>
<span data-ttu-id="d4b49-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4b49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b49-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4b49-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b49-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4b49-140">INPUTS</span></span>

### <span data-ttu-id="d4b49-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="d4b49-141">None</span></span>

## <span data-ttu-id="d4b49-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4b49-142">OUTPUTS</span></span>

### <span data-ttu-id="d4b49-143">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="d4b49-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="d4b49-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4b49-144">NOTES</span></span>

## <span data-ttu-id="d4b49-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4b49-145">RELATED LINKS</span></span>
