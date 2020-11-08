---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188010"
---
# <span data-ttu-id="cf111-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="cf111-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="cf111-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf111-102">SYNOPSIS</span></span>
<span data-ttu-id="cf111-103">Törli az előfizetés biztonsági munkaterület beállítását.</span><span class="sxs-lookup"><span data-stu-id="cf111-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="cf111-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf111-104">SYNTAX</span></span>

### <span data-ttu-id="cf111-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf111-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf111-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf111-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf111-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="cf111-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf111-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf111-108">DESCRIPTION</span></span>
<span data-ttu-id="cf111-109">Törli az előfizetés biztonsági munkaterület beállítását.</span><span class="sxs-lookup"><span data-stu-id="cf111-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="cf111-110">Ezzel a műveletsorral az újonnan telepített biztonsági ügynökök jelentést tesznek az előfizetés alapértelmezett munkaterületére.</span><span class="sxs-lookup"><span data-stu-id="cf111-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="cf111-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cf111-111">EXAMPLES</span></span>

### <span data-ttu-id="cf111-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf111-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="cf111-113">Törli az előfizetés biztonsági munkaterület beállítását.</span><span class="sxs-lookup"><span data-stu-id="cf111-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="cf111-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf111-114">PARAMETERS</span></span>

### <span data-ttu-id="cf111-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf111-115">-DefaultProfile</span></span>
<span data-ttu-id="cf111-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf111-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf111-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf111-117">-InputObject</span></span>
<span data-ttu-id="cf111-118">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="cf111-118">Input Object.</span></span>

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

### <span data-ttu-id="cf111-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf111-119">-Name</span></span>
<span data-ttu-id="cf111-120">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="cf111-120">Resource name.</span></span>

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

### <span data-ttu-id="cf111-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf111-121">-PassThru</span></span>
<span data-ttu-id="cf111-122">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="cf111-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="cf111-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf111-123">-ResourceId</span></span>
<span data-ttu-id="cf111-124">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="cf111-124">Resource ID.</span></span>

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

### <span data-ttu-id="cf111-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf111-125">-Confirm</span></span>
<span data-ttu-id="cf111-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf111-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf111-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf111-127">-WhatIf</span></span>
<span data-ttu-id="cf111-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf111-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf111-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf111-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf111-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf111-130">CommonParameters</span></span>
<span data-ttu-id="cf111-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf111-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf111-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf111-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf111-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf111-133">INPUTS</span></span>

### <span data-ttu-id="cf111-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cf111-134">System.String</span></span>

### <span data-ttu-id="cf111-135">Microsoft. Azure. commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="cf111-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="cf111-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf111-136">OUTPUTS</span></span>

### <span data-ttu-id="cf111-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf111-137">System.Boolean</span></span>

## <span data-ttu-id="cf111-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf111-138">NOTES</span></span>

## <span data-ttu-id="cf111-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf111-139">RELATED LINKS</span></span>