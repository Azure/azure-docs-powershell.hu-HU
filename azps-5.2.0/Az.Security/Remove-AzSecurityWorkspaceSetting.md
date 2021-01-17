---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339870"
---
# <span data-ttu-id="5a606-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="5a606-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="5a606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a606-102">SYNOPSIS</span></span>
<span data-ttu-id="5a606-103">Törli az előfizetés biztonsági munkaterületének beállítását.</span><span class="sxs-lookup"><span data-stu-id="5a606-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="5a606-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a606-104">SYNTAX</span></span>

### <span data-ttu-id="5a606-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a606-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a606-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a606-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a606-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a606-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a606-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a606-108">DESCRIPTION</span></span>
<span data-ttu-id="5a606-109">Törli az előfizetés biztonsági munkaterületének beállítását.</span><span class="sxs-lookup"><span data-stu-id="5a606-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="5a606-110">Ez a művelet lehetővé teszi az újonnan telepített biztonsági ügynököknek, hogy az előfizetés alapértelmezett munkaterületére jelentsen.</span><span class="sxs-lookup"><span data-stu-id="5a606-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="5a606-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a606-111">EXAMPLES</span></span>

### <span data-ttu-id="5a606-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="5a606-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="5a606-113">Törli az előfizetés biztonsági munkaterületének beállítását.</span><span class="sxs-lookup"><span data-stu-id="5a606-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="5a606-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a606-114">PARAMETERS</span></span>

### <span data-ttu-id="5a606-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a606-115">-DefaultProfile</span></span>
<span data-ttu-id="5a606-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a606-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a606-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a606-117">-InputObject</span></span>
<span data-ttu-id="5a606-118">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="5a606-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a606-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5a606-119">-Name</span></span>
<span data-ttu-id="5a606-120">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5a606-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a606-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a606-121">-PassThru</span></span>
<span data-ttu-id="5a606-122">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="5a606-122">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a606-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a606-123">-ResourceId</span></span>
<span data-ttu-id="5a606-124">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5a606-124">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a606-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a606-125">-Confirm</span></span>
<span data-ttu-id="5a606-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a606-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a606-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a606-127">-WhatIf</span></span>
<span data-ttu-id="5a606-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a606-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a606-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a606-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a606-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a606-130">CommonParameters</span></span>
<span data-ttu-id="5a606-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a606-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a606-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a606-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a606-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a606-133">INPUTS</span></span>

### <span data-ttu-id="5a606-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5a606-134">System.String</span></span>

### <span data-ttu-id="5a606-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="5a606-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="5a606-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a606-136">OUTPUTS</span></span>

### <span data-ttu-id="5a606-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a606-137">System.Boolean</span></span>

## <span data-ttu-id="5a606-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a606-138">NOTES</span></span>

## <span data-ttu-id="5a606-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a606-139">RELATED LINKS</span></span>
