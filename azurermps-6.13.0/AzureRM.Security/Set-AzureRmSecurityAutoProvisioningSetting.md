---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: e99ead17cad0a3c6c440967ec1b1852bb5568a26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672580"
---
# <span data-ttu-id="75585-101">Set-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="75585-101">Set-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="75585-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75585-102">SYNOPSIS</span></span>
<span data-ttu-id="75585-103">Automatikus kiépítési beállítás frissítése</span><span class="sxs-lookup"><span data-stu-id="75585-103">Updates automatic provisioning setting</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75585-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75585-104">SYNTAX</span></span>

### <span data-ttu-id="75585-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75585-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75585-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="75585-106">ResourceId</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75585-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="75585-107">InputObject</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75585-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="75585-108">DESCRIPTION</span></span>
<span data-ttu-id="75585-109">Az előfizetés automatikus kiépítési beállításainak bekapcsolása vagy kikapcsolása.</span><span class="sxs-lookup"><span data-stu-id="75585-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="75585-110">Az automatikus kiépítési beállítások segítségével eldöntheti, hogy az Azure Security Center automatikusan nyújt-e olyan biztonsági ügynököt, amely a VMs-eszközön lesz telepítve.</span><span class="sxs-lookup"><span data-stu-id="75585-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="75585-111">A biztonsági ügynök figyeli a VM-et biztonsági riasztások létrehozásához és a VM biztonsági megfelelőségének figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="75585-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="75585-112">Példák</span><span class="sxs-lookup"><span data-stu-id="75585-112">EXAMPLES</span></span>

### <span data-ttu-id="75585-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="75585-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="75585-114">Bekapcsolja az előfizetés automatikus kiépítési beállítását.</span><span class="sxs-lookup"><span data-stu-id="75585-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="75585-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="75585-115">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="75585-116">Kikapcsolja az előfizetés automatikus kiépítési beállítását.</span><span class="sxs-lookup"><span data-stu-id="75585-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="75585-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75585-117">PARAMETERS</span></span>

### <span data-ttu-id="75585-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75585-118">-DefaultProfile</span></span>
<span data-ttu-id="75585-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75585-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75585-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="75585-120">-EnableAutoProvision</span></span>
<span data-ttu-id="75585-121">Automatikus kiépítési.</span><span class="sxs-lookup"><span data-stu-id="75585-121">Automatic Provisioning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75585-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75585-122">-InputObject</span></span>
<span data-ttu-id="75585-123">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="75585-123">Input Object.</span></span>

```yaml
Type: PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75585-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75585-124">-Name</span></span>
<span data-ttu-id="75585-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="75585-125">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75585-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75585-126">-ResourceId</span></span>
<span data-ttu-id="75585-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="75585-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75585-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="75585-128">-Confirm</span></span>
<span data-ttu-id="75585-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="75585-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75585-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75585-130">-WhatIf</span></span>
<span data-ttu-id="75585-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="75585-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75585-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75585-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75585-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75585-133">CommonParameters</span></span>
<span data-ttu-id="75585-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75585-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75585-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75585-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75585-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75585-136">INPUTS</span></span>

### <span data-ttu-id="75585-137">System. String</span><span class="sxs-lookup"><span data-stu-id="75585-137">System.String</span></span>
<span data-ttu-id="75585-138">System. Management. Automation. SwitchParameter Microsoft. Azure. commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="75585-138">System.Management.Automation.SwitchParameter Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="75585-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75585-139">OUTPUTS</span></span>

### <span data-ttu-id="75585-140">Microsoft. Azure. commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="75585-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="75585-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75585-141">NOTES</span></span>

## <span data-ttu-id="75585-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75585-142">RELATED LINKS</span></span>
