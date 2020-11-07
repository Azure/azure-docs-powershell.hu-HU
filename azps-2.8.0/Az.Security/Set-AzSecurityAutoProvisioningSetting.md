---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: d4741bc0456abfe99071f57d3224db8925bd1724
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838068"
---
# <span data-ttu-id="46a2a-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="46a2a-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="46a2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="46a2a-103">Automatikus kiépítési beállítás frissítése</span><span class="sxs-lookup"><span data-stu-id="46a2a-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="46a2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46a2a-104">SYNTAX</span></span>

### <span data-ttu-id="46a2a-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46a2a-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a2a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="46a2a-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a2a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="46a2a-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a2a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="46a2a-108">DESCRIPTION</span></span>
<span data-ttu-id="46a2a-109">Az előfizetés automatikus kiépítési beállításainak bekapcsolása vagy kikapcsolása.</span><span class="sxs-lookup"><span data-stu-id="46a2a-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="46a2a-110">Az automatikus kiépítési beállítások segítségével eldöntheti, hogy az Azure Security Center automatikusan nyújt-e olyan biztonsági ügynököt, amely a VMs-eszközön lesz telepítve.</span><span class="sxs-lookup"><span data-stu-id="46a2a-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="46a2a-111">A biztonsági ügynök figyeli a VM-et biztonsági riasztások létrehozásához és a VM biztonsági megfelelőségének figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="46a2a-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="46a2a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="46a2a-112">EXAMPLES</span></span>

### <span data-ttu-id="46a2a-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="46a2a-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="46a2a-114">Bekapcsolja az előfizetés automatikus kiépítési beállítását.</span><span class="sxs-lookup"><span data-stu-id="46a2a-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="46a2a-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="46a2a-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="46a2a-116">Kikapcsolja az előfizetés automatikus kiépítési beállítását.</span><span class="sxs-lookup"><span data-stu-id="46a2a-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="46a2a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46a2a-117">PARAMETERS</span></span>

### <span data-ttu-id="46a2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a2a-118">-DefaultProfile</span></span>
<span data-ttu-id="46a2a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46a2a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46a2a-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="46a2a-120">-EnableAutoProvision</span></span>
<span data-ttu-id="46a2a-121">Automatikus kiépítési.</span><span class="sxs-lookup"><span data-stu-id="46a2a-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="46a2a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46a2a-122">-InputObject</span></span>
<span data-ttu-id="46a2a-123">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="46a2a-123">Input Object.</span></span>

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

### <span data-ttu-id="46a2a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46a2a-124">-Name</span></span>
<span data-ttu-id="46a2a-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="46a2a-125">Resource name.</span></span>

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

### <span data-ttu-id="46a2a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46a2a-126">-ResourceId</span></span>
<span data-ttu-id="46a2a-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="46a2a-127">Resource ID.</span></span>

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

### <span data-ttu-id="46a2a-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46a2a-128">-Confirm</span></span>
<span data-ttu-id="46a2a-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46a2a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a2a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a2a-130">-WhatIf</span></span>
<span data-ttu-id="46a2a-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46a2a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46a2a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46a2a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a2a-133">CommonParameters</span></span>
<span data-ttu-id="46a2a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46a2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a2a-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a2a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a2a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46a2a-136">INPUTS</span></span>

### <span data-ttu-id="46a2a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="46a2a-137">System.String</span></span>

### <span data-ttu-id="46a2a-138">Microsoft. Azure. commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="46a2a-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="46a2a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46a2a-139">OUTPUTS</span></span>

### <span data-ttu-id="46a2a-140">Microsoft. Azure. commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="46a2a-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="46a2a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46a2a-141">NOTES</span></span>

## <span data-ttu-id="46a2a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46a2a-142">RELATED LINKS</span></span>
