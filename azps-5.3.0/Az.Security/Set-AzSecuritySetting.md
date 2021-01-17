---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479746"
---
# <span data-ttu-id="58cd5-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="58cd5-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="58cd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="58cd5-103">Biztonsági beállítás frissítése az Azure Biztonsági központban</span><span class="sxs-lookup"><span data-stu-id="58cd5-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="58cd5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58cd5-104">SYNTAX</span></span>

### <span data-ttu-id="58cd5-105">GeneralScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58cd5-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58cd5-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="58cd5-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58cd5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="58cd5-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58cd5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58cd5-108">DESCRIPTION</span></span>
<span data-ttu-id="58cd5-109">A Set-AzSecuritySetting parancsmag frissíti egy adott biztonsági beállítást az Azure Biztonsági központban.</span><span class="sxs-lookup"><span data-stu-id="58cd5-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="58cd5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58cd5-110">EXAMPLES</span></span>

### <span data-ttu-id="58cd5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="58cd5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="58cd5-112">McAS-adatexport beállítás frissítése</span><span class="sxs-lookup"><span data-stu-id="58cd5-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="58cd5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58cd5-113">PARAMETERS</span></span>

### <span data-ttu-id="58cd5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58cd5-114">-DefaultProfile</span></span>
<span data-ttu-id="58cd5-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58cd5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58cd5-116">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="58cd5-116">-Enabled</span></span>
<span data-ttu-id="58cd5-117">Engedélyezi a beállítást.</span><span class="sxs-lookup"><span data-stu-id="58cd5-117">Enables the setting.</span></span>

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

### <span data-ttu-id="58cd5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58cd5-118">-InputObject</span></span>
<span data-ttu-id="58cd5-119">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="58cd5-119">Input Object.</span></span>

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

### <span data-ttu-id="58cd5-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="58cd5-120">-SettingKind</span></span>
<span data-ttu-id="58cd5-121">Beállítási fajta.</span><span class="sxs-lookup"><span data-stu-id="58cd5-121">Setting kind.</span></span> <span data-ttu-id="58cd5-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="58cd5-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="58cd5-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="58cd5-123">-SettingName</span></span>
<span data-ttu-id="58cd5-124">Beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="58cd5-124">Setting name.</span></span> <span data-ttu-id="58cd5-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="58cd5-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="58cd5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58cd5-126">-Confirm</span></span>
<span data-ttu-id="58cd5-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="58cd5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58cd5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58cd5-128">-WhatIf</span></span>
<span data-ttu-id="58cd5-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="58cd5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58cd5-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58cd5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58cd5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58cd5-131">CommonParameters</span></span>
<span data-ttu-id="58cd5-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58cd5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58cd5-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58cd5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58cd5-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58cd5-134">INPUTS</span></span>

### <span data-ttu-id="58cd5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="58cd5-135">System.String</span></span>
### <span data-ttu-id="58cd5-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="58cd5-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="58cd5-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="58cd5-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="58cd5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58cd5-138">System.Boolean</span></span>

## <span data-ttu-id="58cd5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58cd5-139">OUTPUTS</span></span>

### <span data-ttu-id="58cd5-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="58cd5-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="58cd5-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="58cd5-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="58cd5-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58cd5-142">NOTES</span></span>

## <span data-ttu-id="58cd5-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58cd5-143">RELATED LINKS</span></span>
