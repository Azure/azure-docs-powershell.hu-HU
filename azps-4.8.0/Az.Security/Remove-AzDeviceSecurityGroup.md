---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183979"
---
# <span data-ttu-id="5540e-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5540e-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="5540e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5540e-102">SYNOPSIS</span></span>
<span data-ttu-id="5540e-103">Az eszköz biztonsági csoportjának törlése</span><span class="sxs-lookup"><span data-stu-id="5540e-103">Delete device security group</span></span>

## <span data-ttu-id="5540e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5540e-104">SYNTAX</span></span>

### <span data-ttu-id="5540e-105">ResourceIdLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5540e-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5540e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5540e-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5540e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5540e-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5540e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5540e-108">DESCRIPTION</span></span>
<span data-ttu-id="5540e-109">Az Remove-AzDeviceSecurityGroup parancsmag törli a IOT biztonsági megoldásban meghatározott eszközönkénti biztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="5540e-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="5540e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5540e-110">EXAMPLES</span></span>

### <span data-ttu-id="5540e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5540e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="5540e-112">A IOT hub "MySecurityGroup" eszköz biztonsági csoportjának törlése a "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" azonosítójú erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="5540e-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="5540e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5540e-113">PARAMETERS</span></span>

### <span data-ttu-id="5540e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5540e-114">-DefaultProfile</span></span>
<span data-ttu-id="5540e-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5540e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5540e-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="5540e-116">-HubResourceId</span></span>
<span data-ttu-id="5540e-117">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="5540e-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5540e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5540e-118">-InputObject</span></span>
<span data-ttu-id="5540e-119">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="5540e-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5540e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5540e-120">-Name</span></span>
<span data-ttu-id="5540e-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="5540e-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5540e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5540e-122">-PassThru</span></span>
<span data-ttu-id="5540e-123">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="5540e-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5540e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5540e-124">-ResourceId</span></span>
<span data-ttu-id="5540e-125">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="5540e-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5540e-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5540e-126">-Confirm</span></span>
<span data-ttu-id="5540e-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5540e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5540e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5540e-128">-WhatIf</span></span>
<span data-ttu-id="5540e-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5540e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5540e-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5540e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5540e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5540e-131">CommonParameters</span></span>
<span data-ttu-id="5540e-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5540e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5540e-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5540e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5540e-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5540e-134">INPUTS</span></span>

### <span data-ttu-id="5540e-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5540e-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="5540e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5540e-136">System.String</span></span>

## <span data-ttu-id="5540e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5540e-137">OUTPUTS</span></span>

### <span data-ttu-id="5540e-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5540e-138">System.Boolean</span></span>

## <span data-ttu-id="5540e-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5540e-139">NOTES</span></span>

## <span data-ttu-id="5540e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5540e-140">RELATED LINKS</span></span>
