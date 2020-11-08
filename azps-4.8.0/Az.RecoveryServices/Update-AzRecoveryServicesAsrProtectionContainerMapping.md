---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184244"
---
# <span data-ttu-id="421fb-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="421fb-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="421fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="421fb-102">SYNOPSIS</span></span>
<span data-ttu-id="421fb-103">Frissítse az Azure site Recovery Protection Container megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="421fb-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="421fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="421fb-104">SYNTAX</span></span>

### <span data-ttu-id="421fb-105">AzureToAzureEnableAutoUpdate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="421fb-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="421fb-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="421fb-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="421fb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="421fb-107">DESCRIPTION</span></span>
<span data-ttu-id="421fb-108">Az **Update-AzRecoveryServicesAsrProtectionContainerMapping** parancsmag frissíti a megadott Azure-webhely-helyreállítási védelmi tárolók megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="421fb-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="421fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="421fb-109">EXAMPLES</span></span>

### <span data-ttu-id="421fb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="421fb-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="421fb-111">Indítsa el a műveletet a tároló automatikus frissítésének letiltásához.</span><span class="sxs-lookup"><span data-stu-id="421fb-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="421fb-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="421fb-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="421fb-113">A művelet indításához tiltsa le a tároló automatikus frissítésének engedélyezése jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="421fb-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="421fb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="421fb-114">PARAMETERS</span></span>

### <span data-ttu-id="421fb-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="421fb-115">-AutomationAccountId</span></span>
<span data-ttu-id="421fb-116">Az automatikus udpate használt automatizálási accountId adja meg.</span><span class="sxs-lookup"><span data-stu-id="421fb-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="421fb-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="421fb-117">-AzureToAzure</span></span>
<span data-ttu-id="421fb-118">Az Azure az Azure Protection tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="421fb-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="421fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="421fb-119">-DefaultProfile</span></span>
<span data-ttu-id="421fb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="421fb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="421fb-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="421fb-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="421fb-122">Váltson paramétert az automatikus frissítés letiltásához.</span><span class="sxs-lookup"><span data-stu-id="421fb-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="421fb-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="421fb-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="421fb-124">Váltson paramétert az automatikus frissítés engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="421fb-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="421fb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="421fb-125">-InputObject</span></span>
<span data-ttu-id="421fb-126">Objektum a védett tárolók megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="421fb-126">Object for protection container mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="421fb-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="421fb-127">-Confirm</span></span>
<span data-ttu-id="421fb-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="421fb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="421fb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="421fb-129">-WhatIf</span></span>
<span data-ttu-id="421fb-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="421fb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="421fb-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="421fb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="421fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421fb-132">CommonParameters</span></span>
<span data-ttu-id="421fb-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="421fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421fb-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="421fb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421fb-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="421fb-135">INPUTS</span></span>

### <span data-ttu-id="421fb-136">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="421fb-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="421fb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="421fb-137">OUTPUTS</span></span>

### <span data-ttu-id="421fb-138">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="421fb-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="421fb-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="421fb-139">NOTES</span></span>

## <span data-ttu-id="421fb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="421fb-140">RELATED LINKS</span></span>
