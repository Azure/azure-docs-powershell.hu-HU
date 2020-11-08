---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188000"
---
# <span data-ttu-id="86020-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="86020-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="86020-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86020-102">SYNOPSIS</span></span>
<span data-ttu-id="86020-103">Automatikus kiépítési beállítás frissítése</span><span class="sxs-lookup"><span data-stu-id="86020-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="86020-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86020-104">SYNTAX</span></span>

### <span data-ttu-id="86020-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86020-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86020-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="86020-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86020-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="86020-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86020-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="86020-108">DESCRIPTION</span></span>
<span data-ttu-id="86020-109">Az előfizetés automatikus kiépítési beállításainak bekapcsolása vagy kikapcsolása.</span><span class="sxs-lookup"><span data-stu-id="86020-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="86020-110">Az automatikus kiépítési beállítások segítségével eldöntheti, hogy az Azure Security Center automatikusan nyújt-e olyan biztonsági ügynököt, amely a VMs-eszközön lesz telepítve.</span><span class="sxs-lookup"><span data-stu-id="86020-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="86020-111">A biztonsági ügynök figyeli a VM-et biztonsági riasztások létrehozásához és a VM biztonsági megfelelőségének figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="86020-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="86020-112">Példák</span><span class="sxs-lookup"><span data-stu-id="86020-112">EXAMPLES</span></span>

### <span data-ttu-id="86020-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="86020-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="86020-114">Bekapcsolja az előfizetés automatikus kiépítési beállítását.</span><span class="sxs-lookup"><span data-stu-id="86020-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="86020-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="86020-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="86020-116">Kikapcsolja az előfizetés automatikus kiépítési beállítását.</span><span class="sxs-lookup"><span data-stu-id="86020-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="86020-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86020-117">PARAMETERS</span></span>

### <span data-ttu-id="86020-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86020-118">-DefaultProfile</span></span>
<span data-ttu-id="86020-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86020-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86020-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="86020-120">-EnableAutoProvision</span></span>
<span data-ttu-id="86020-121">Automatikus kiépítési.</span><span class="sxs-lookup"><span data-stu-id="86020-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="86020-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86020-122">-InputObject</span></span>
<span data-ttu-id="86020-123">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="86020-123">Input Object.</span></span>

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

### <span data-ttu-id="86020-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86020-124">-Name</span></span>
<span data-ttu-id="86020-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="86020-125">Resource name.</span></span>

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

### <span data-ttu-id="86020-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86020-126">-ResourceId</span></span>
<span data-ttu-id="86020-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="86020-127">Resource ID.</span></span>

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

### <span data-ttu-id="86020-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86020-128">-Confirm</span></span>
<span data-ttu-id="86020-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86020-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86020-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86020-130">-WhatIf</span></span>
<span data-ttu-id="86020-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86020-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86020-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86020-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86020-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86020-133">CommonParameters</span></span>
<span data-ttu-id="86020-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86020-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86020-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86020-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86020-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86020-136">INPUTS</span></span>

### <span data-ttu-id="86020-137">System. String</span><span class="sxs-lookup"><span data-stu-id="86020-137">System.String</span></span>

### <span data-ttu-id="86020-138">Microsoft. Azure. commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="86020-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="86020-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86020-139">OUTPUTS</span></span>

### <span data-ttu-id="86020-140">Microsoft. Azure. commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="86020-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="86020-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86020-141">NOTES</span></span>

## <span data-ttu-id="86020-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86020-142">RELATED LINKS</span></span>
