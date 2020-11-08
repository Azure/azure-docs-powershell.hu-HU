---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180874"
---
# <span data-ttu-id="29321-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="29321-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="29321-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29321-102">SYNOPSIS</span></span>
<span data-ttu-id="29321-103">Biztonsági beállítás frissítése az Azure biztonsági központban</span><span class="sxs-lookup"><span data-stu-id="29321-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="29321-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29321-104">SYNTAX</span></span>

### <span data-ttu-id="29321-105">GeneralScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29321-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29321-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="29321-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29321-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="29321-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29321-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="29321-108">DESCRIPTION</span></span>
<span data-ttu-id="29321-109">A Set-AzSecuritySetting parancsmag az Azure Security Center bizonyos biztonsági beállítását frissíti.</span><span class="sxs-lookup"><span data-stu-id="29321-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="29321-110">Példák</span><span class="sxs-lookup"><span data-stu-id="29321-110">EXAMPLES</span></span>

### <span data-ttu-id="29321-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29321-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="29321-112">MCAS-adatexportálási beállítás frissítése</span><span class="sxs-lookup"><span data-stu-id="29321-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="29321-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29321-113">PARAMETERS</span></span>

### <span data-ttu-id="29321-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29321-114">-DefaultProfile</span></span>
<span data-ttu-id="29321-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29321-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29321-116">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="29321-116">-Enabled</span></span>
<span data-ttu-id="29321-117">Engedélyezi a beállítást.</span><span class="sxs-lookup"><span data-stu-id="29321-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29321-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29321-118">-InputObject</span></span>
<span data-ttu-id="29321-119">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="29321-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29321-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="29321-120">-SettingKind</span></span>
<span data-ttu-id="29321-121">Beállítás típusa.</span><span class="sxs-lookup"><span data-stu-id="29321-121">Setting kind.</span></span> <span data-ttu-id="29321-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="29321-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29321-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="29321-123">-SettingName</span></span>
<span data-ttu-id="29321-124">Beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="29321-124">Setting name.</span></span> <span data-ttu-id="29321-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="29321-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29321-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29321-126">-Confirm</span></span>
<span data-ttu-id="29321-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29321-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29321-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29321-128">-WhatIf</span></span>
<span data-ttu-id="29321-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29321-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29321-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29321-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29321-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29321-131">CommonParameters</span></span>
<span data-ttu-id="29321-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29321-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29321-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="29321-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29321-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29321-134">INPUTS</span></span>

### <span data-ttu-id="29321-135">System. String</span><span class="sxs-lookup"><span data-stu-id="29321-135">System.String</span></span>
### <span data-ttu-id="29321-136">Microsoft. Azure. Command. Security. models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="29321-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="29321-137">Microsoft. Azure. Command. Security. models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="29321-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="29321-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29321-138">System.Boolean</span></span>

## <span data-ttu-id="29321-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29321-139">OUTPUTS</span></span>

### <span data-ttu-id="29321-140">Microsoft. Azure. Command. Security. models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="29321-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="29321-141">Microsoft. Azure. Command. Security. models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="29321-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="29321-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29321-142">NOTES</span></span>

## <span data-ttu-id="29321-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29321-143">RELATED LINKS</span></span>
