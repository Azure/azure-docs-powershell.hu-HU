---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150811"
---
# <span data-ttu-id="b970e-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="b970e-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b970e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b970e-102">SYNOPSIS</span></span>
<span data-ttu-id="b970e-103">Az automatikus kiépítési beállítás frissítése</span><span class="sxs-lookup"><span data-stu-id="b970e-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="b970e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b970e-104">SYNTAX</span></span>

### <span data-ttu-id="b970e-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b970e-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b970e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b970e-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b970e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b970e-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b970e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b970e-108">DESCRIPTION</span></span>
<span data-ttu-id="b970e-109">Az előfizetés automatikus kiépítési beállításainak be- és kikapcsolása.</span><span class="sxs-lookup"><span data-stu-id="b970e-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="b970e-110">Az automatikus kiépítési beállítások segítségével eldöntheti, hogy szeretné-e, hogy az Azure Biztonsági központ automatikusan kiépítsen egy biztonsági ügynököt, amely telepítve lesz a virtuális gépekre.</span><span class="sxs-lookup"><span data-stu-id="b970e-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="b970e-111">A biztonsági ügynök figyeli a vm-et, és biztonsági riasztásokat hoz létre, és figyeli a virtuális gép biztonsági megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="b970e-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="b970e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b970e-112">EXAMPLES</span></span>

### <span data-ttu-id="b970e-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="b970e-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="b970e-114">Bekapcsolja az automatikus kiépítési beállítást az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="b970e-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="b970e-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="b970e-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="b970e-116">Kikapcsolja az előfizetés automatikus kiépítési beállítását.</span><span class="sxs-lookup"><span data-stu-id="b970e-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="b970e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b970e-117">PARAMETERS</span></span>

### <span data-ttu-id="b970e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b970e-118">-DefaultProfile</span></span>
<span data-ttu-id="b970e-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b970e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b970e-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="b970e-120">-EnableAutoProvision</span></span>
<span data-ttu-id="b970e-121">Automatikus kiépítés.</span><span class="sxs-lookup"><span data-stu-id="b970e-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="b970e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b970e-122">-InputObject</span></span>
<span data-ttu-id="b970e-123">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="b970e-123">Input Object.</span></span>

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

### <span data-ttu-id="b970e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b970e-124">-Name</span></span>
<span data-ttu-id="b970e-125">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b970e-125">Resource name.</span></span>

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

### <span data-ttu-id="b970e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b970e-126">-ResourceId</span></span>
<span data-ttu-id="b970e-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b970e-127">Resource ID.</span></span>

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

### <span data-ttu-id="b970e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b970e-128">-Confirm</span></span>
<span data-ttu-id="b970e-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b970e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b970e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b970e-130">-WhatIf</span></span>
<span data-ttu-id="b970e-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b970e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b970e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b970e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b970e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b970e-133">CommonParameters</span></span>
<span data-ttu-id="b970e-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b970e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b970e-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b970e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b970e-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b970e-136">INPUTS</span></span>

### <span data-ttu-id="b970e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b970e-137">System.String</span></span>

### <span data-ttu-id="b970e-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="b970e-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b970e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b970e-139">OUTPUTS</span></span>

### <span data-ttu-id="b970e-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="b970e-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b970e-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b970e-141">NOTES</span></span>

## <span data-ttu-id="b970e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b970e-142">RELATED LINKS</span></span>
