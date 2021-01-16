---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 0555b86b6e5240adfc43bc52153bf14d7612be1b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382547"
---
# <span data-ttu-id="650d1-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="650d1-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="650d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="650d1-102">SYNOPSIS</span></span>
<span data-ttu-id="650d1-103">Biztonsági riasztás állapotának frissítése.</span><span class="sxs-lookup"><span data-stu-id="650d1-103">Updates a security alert state.</span></span>

## <span data-ttu-id="650d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="650d1-104">SYNTAX</span></span>

### <span data-ttu-id="650d1-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="650d1-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="650d1-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="650d1-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="650d1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="650d1-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="650d1-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="650d1-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="650d1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="650d1-109">DESCRIPTION</span></span>
<span data-ttu-id="650d1-110">Biztonsági riasztási állapotot állít be.</span><span class="sxs-lookup"><span data-stu-id="650d1-110">Sets a security alert state.</span></span>

## <span data-ttu-id="650d1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="650d1-111">EXAMPLES</span></span>

### <span data-ttu-id="650d1-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="650d1-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="650d1-113">A fel nem emelt biztonsági riasztás mellőzését.</span><span class="sxs-lookup"><span data-stu-id="650d1-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="650d1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="650d1-114">PARAMETERS</span></span>

### <span data-ttu-id="650d1-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="650d1-115">-ActionType</span></span>
<span data-ttu-id="650d1-116">Művelettípus.</span><span class="sxs-lookup"><span data-stu-id="650d1-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650d1-117">-DefaultProfile</span></span>
<span data-ttu-id="650d1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="650d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="650d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="650d1-119">-InputObject</span></span>
<span data-ttu-id="650d1-120">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="650d1-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="650d1-121">-Location</span><span class="sxs-lookup"><span data-stu-id="650d1-121">-Location</span></span>
<span data-ttu-id="650d1-122">Hely.</span><span class="sxs-lookup"><span data-stu-id="650d1-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650d1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="650d1-123">-Name</span></span>
<span data-ttu-id="650d1-124">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="650d1-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650d1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="650d1-125">-PassThru</span></span>
<span data-ttu-id="650d1-126">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="650d1-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="650d1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="650d1-127">-ResourceGroupName</span></span>
<span data-ttu-id="650d1-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="650d1-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="650d1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="650d1-129">-ResourceId</span></span>
<span data-ttu-id="650d1-130">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="650d1-130">Resource ID.</span></span>

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

### <span data-ttu-id="650d1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="650d1-131">-Confirm</span></span>
<span data-ttu-id="650d1-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="650d1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="650d1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="650d1-133">-WhatIf</span></span>
<span data-ttu-id="650d1-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="650d1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="650d1-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="650d1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="650d1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650d1-136">CommonParameters</span></span>
<span data-ttu-id="650d1-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650d1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650d1-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="650d1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650d1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="650d1-139">INPUTS</span></span>

### <span data-ttu-id="650d1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="650d1-140">System.String</span></span>

### <span data-ttu-id="650d1-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="650d1-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="650d1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="650d1-142">OUTPUTS</span></span>

### <span data-ttu-id="650d1-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="650d1-143">System.Boolean</span></span>

## <span data-ttu-id="650d1-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="650d1-144">NOTES</span></span>

## <span data-ttu-id="650d1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="650d1-145">RELATED LINKS</span></span>
