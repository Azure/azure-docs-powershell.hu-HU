---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 29c996036705e3fc71f1c6a04ead16c24b1b3bca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918114"
---
# <span data-ttu-id="7719c-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7719c-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="7719c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7719c-102">SYNOPSIS</span></span>
<span data-ttu-id="7719c-103">Frissítse az Azure-webhely helyreállítási védelem tárolóleképezését.</span><span class="sxs-lookup"><span data-stu-id="7719c-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="7719c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7719c-104">SYNTAX</span></span>

### <span data-ttu-id="7719c-105">AzureToAzureEnableAutoUpdate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7719c-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7719c-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="7719c-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7719c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7719c-107">DESCRIPTION</span></span>
<span data-ttu-id="7719c-108">Az **Update-AzRecoveryServicesAsrProtectionContainerMapping** parancsmag frissíti a megadott Azure-webhely-helyreállításvédelmi tároló megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="7719c-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="7719c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7719c-109">EXAMPLES</span></span>

### <span data-ttu-id="7719c-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7719c-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="7719c-111">Indítsa el a műveletet a tároló automatikus frissítésének letiltásához.</span><span class="sxs-lookup"><span data-stu-id="7719c-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="7719c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7719c-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="7719c-113">Indítsa el a műveletet az automatikus frissítés engedélyezésének letiltásához a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="7719c-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="7719c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7719c-114">PARAMETERS</span></span>

### <span data-ttu-id="7719c-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="7719c-115">-AutomationAccountId</span></span>
<span data-ttu-id="7719c-116">Az automatikus udpate automatizálási fiókazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7719c-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="7719c-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7719c-117">-AzureToAzure</span></span>
<span data-ttu-id="7719c-118">Az Azure–Azure védelmi tároló megadása.</span><span class="sxs-lookup"><span data-stu-id="7719c-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="7719c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7719c-119">-DefaultProfile</span></span>
<span data-ttu-id="7719c-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7719c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7719c-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="7719c-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="7719c-122">Az automatikus frissítés letiltásához váltson paraméterre.</span><span class="sxs-lookup"><span data-stu-id="7719c-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="7719c-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="7719c-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="7719c-124">Paraméter váltása az automatikus frissítés engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="7719c-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="7719c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7719c-125">-InputObject</span></span>
<span data-ttu-id="7719c-126">Objektum a védelmi tároló megfeleltetéshez.</span><span class="sxs-lookup"><span data-stu-id="7719c-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="7719c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7719c-127">-Confirm</span></span>
<span data-ttu-id="7719c-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7719c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7719c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7719c-129">-WhatIf</span></span>
<span data-ttu-id="7719c-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7719c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7719c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7719c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7719c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7719c-132">CommonParameters</span></span>
<span data-ttu-id="7719c-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7719c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7719c-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7719c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7719c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7719c-135">INPUTS</span></span>

### <span data-ttu-id="7719c-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7719c-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="7719c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7719c-137">OUTPUTS</span></span>

### <span data-ttu-id="7719c-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="7719c-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7719c-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7719c-139">NOTES</span></span>

## <span data-ttu-id="7719c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7719c-140">RELATED LINKS</span></span>
