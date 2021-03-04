---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: b915be5c5014c278a2fbb12a6982890ed922ca60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936041"
---
# <span data-ttu-id="d2a07-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="d2a07-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d2a07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a07-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a07-103">Az automatikus kiépítési beállítás frissítése</span><span class="sxs-lookup"><span data-stu-id="d2a07-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="d2a07-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2a07-104">SYNTAX</span></span>

### <span data-ttu-id="d2a07-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2a07-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a07-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a07-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a07-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d2a07-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2a07-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2a07-108">DESCRIPTION</span></span>
<span data-ttu-id="d2a07-109">Az előfizetés automatikus kiépítési beállításainak be- és kikapcsolása.</span><span class="sxs-lookup"><span data-stu-id="d2a07-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="d2a07-110">Az automatikus kiépítési beállítások segítségével eldöntheti, hogy szeretné-e, hogy az Azure Biztonsági központ automatikusan kiépítsen egy biztonsági ügynököt, amely telepítve lesz a virtuális gépekre.</span><span class="sxs-lookup"><span data-stu-id="d2a07-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="d2a07-111">A biztonsági ügynök figyeli a vm-et, és biztonsági riasztásokat hoz létre, és figyeli a virtuális gép biztonsági megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="d2a07-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="d2a07-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2a07-112">EXAMPLES</span></span>

### <span data-ttu-id="d2a07-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="d2a07-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="d2a07-114">Bekapcsolja az automatikus kiépítési beállítást az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="d2a07-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="d2a07-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="d2a07-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="d2a07-116">Kikapcsolja az előfizetés automatikus kiépítési beállítását.</span><span class="sxs-lookup"><span data-stu-id="d2a07-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="d2a07-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2a07-117">PARAMETERS</span></span>

### <span data-ttu-id="d2a07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a07-118">-DefaultProfile</span></span>
<span data-ttu-id="d2a07-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2a07-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2a07-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="d2a07-120">-EnableAutoProvision</span></span>
<span data-ttu-id="d2a07-121">Automatikus kiépítés.</span><span class="sxs-lookup"><span data-stu-id="d2a07-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a07-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2a07-122">-InputObject</span></span>
<span data-ttu-id="d2a07-123">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="d2a07-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a07-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d2a07-124">-Name</span></span>
<span data-ttu-id="d2a07-125">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d2a07-125">Resource name.</span></span>

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

### <span data-ttu-id="d2a07-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a07-126">-ResourceId</span></span>
<span data-ttu-id="d2a07-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d2a07-127">Resource ID.</span></span>

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

### <span data-ttu-id="d2a07-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2a07-128">-Confirm</span></span>
<span data-ttu-id="d2a07-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d2a07-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2a07-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a07-130">-WhatIf</span></span>
<span data-ttu-id="d2a07-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d2a07-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2a07-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2a07-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2a07-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a07-133">CommonParameters</span></span>
<span data-ttu-id="d2a07-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a07-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a07-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2a07-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a07-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2a07-136">INPUTS</span></span>

### <span data-ttu-id="d2a07-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d2a07-137">System.String</span></span>

### <span data-ttu-id="d2a07-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="d2a07-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d2a07-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2a07-139">OUTPUTS</span></span>

### <span data-ttu-id="d2a07-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="d2a07-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d2a07-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2a07-141">NOTES</span></span>

## <span data-ttu-id="d2a07-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2a07-142">RELATED LINKS</span></span>
